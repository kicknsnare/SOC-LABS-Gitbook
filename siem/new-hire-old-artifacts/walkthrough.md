# Walkthrough

\
A Web Browser Password Viewer executed on the infected machine. What is the name of the binary? Enter the full path.

```splunk-spl
index="main" password viewer
```



What is listed as the company name?\
&#x20;

<figure><img src="https://camo.githubusercontent.com/640cdac7729cbab0cab6d16dd001f7100e0443ad7e436776672704d32ddd7d19/68747470733a2f2f692e696d6775722e636f6d2f786c704c706c492e706e67" alt=""><figcaption></figcaption></figure>



Another suspicious binary running from the same folder was executed on the workstation. What was the name of the binary? What is listed as its original filename? (format: file.xyz,file.xyz)\
&#x20;

<figure><img src="https://camo.githubusercontent.com/3682b5398a1a8e2e12078e6af0b7b4a3cf45c3016ddfcfcb2d992803795b0325/68747470733a2f2f692e696d6775722e636f6d2f546b324f6d48312e706e67" alt=""><figcaption></figcaption></figure>

<figure><img src="https://camo.githubusercontent.com/5db548402b6a417b3d3793ae7e08cd2d747e7fcde3d18bd4188a20a9138e07a0/68747470733a2f2f692e696d6775722e636f6d2f657a6c456a31742e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/aeac72ae7773a063413a390d6a9488253c6aa5bc40b694276be617c33c7e51cf/68747470733a2f2f692e696d6775722e636f6d2f613070545a536c2e706e67" alt=""><figcaption></figcaption></figure>

The binary from the previous question made two outbound connections to a malicious IP address. What was the IP address? Enter the answer in a defang format.\


Check images from above&#x20;

The same binary made some change to a registry key. What was the key path?\


```splunk-spl
index="main" IonicLarge.exe HKLM EventType=SetValue
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/dd8a9d4dd4d5709e081372c27eb04c65707e502a8c964709561803318d46d3a9/68747470733a2f2f692e696d6775722e636f6d2f6869754b7251422e706e67" alt=""><figcaption></figcaption></figure>

Some processes were killed and the associated binaries were deleted. What were the names of the two binaries? (format: file.xyz,file.xyz)\


```splunk-spl
index="main" taskkill /im cmd
| dedup ParentCommandLine
| table ParentCommandLine
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/4263eda3915047c0efeb4399f77b3ba55e8cbdd49a5be16564c255987bc61c3f/68747470733a2f2f692e696d6775722e636f6d2f5a4a51453868372e706e67" alt=""><figcaption></figcaption></figure>

The attacker ran several commands within a PowerShell session to change the behaviour of Windows Defender. What was the last command executed in the series of similar commands?\


```splunk-spl
index="main" powershell windows defender ParentCommandLine
```



Based on the previous answer, what were the four IDs set by the attacker? Enter the answer in order of execution. (format: 1st,2nd,3rd,4th)\


```splunk-spl
index="main" powershell windows defender ParentCommandLine
| dedup ParentCommandLine 
| table ParentCommandLine
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/4282f0b50f979a7ab208387953ffe7b9f46c31f49026b6a7c050199c87daa407/68747470733a2f2f692e696d6775722e636f6d2f6230764a4c74462e706e67" alt=""><figcaption></figcaption></figure>

Another malicious binary was executed on the infected workstation from another AppData location. What was the full path to the binary?\


<figure><img src="https://camo.githubusercontent.com/75f6a1494bcafc7f6ad694867fa3642177322be2b254e03797c53245e3d61ce8/68747470733a2f2f692e696d6775722e636f6d2f506d54774f6c482e706e67" alt=""><figcaption></figcaption></figure>

What were the DLLs that were loaded from the binary from the previous question? Enter the answers in alphabetical order. (format: file1.dll,file2.dll,file3.dll)

```splunk-spl
index="main" *C:\\Users\\Finance01\\AppData\\Roaming\\EasyCalc\\EasyCalc.exe* *dll RuleName="technique_id=T1073,technique_name=DLL Side-Loading"
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/6e6da2f96fb82bde261bc5e491b4ca3eaf3d434e112a6b61a4f4c8ca95da988a/68747470733a2f2f692e696d6775722e636f6d2f4f61556f3138632e706e67" alt=""><figcaption></figcaption></figure>
