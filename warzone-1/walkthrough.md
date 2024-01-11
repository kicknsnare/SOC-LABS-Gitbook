# Walkthrough

What was the alert signature for Malware Command and Control Activity Detected?

<mark style="color:green;">ET Malware MirrorBlast CnC Activity M3</mark>

<figure><img src="https://camo.githubusercontent.com/24e19650c44fcf6b3b19b36f9b31037b16ce0baf02ec7f769beadd98fea322ad/68747470733a2f2f692e696d6775722e636f6d2f6b3164457578322e706e67" alt=""><figcaption></figcaption></figure>

What is the source IP address? Enter your answer in a defanged format.&#x20;

&#x20;<mark style="color:green;">172\[.]16\[.]1\[.]102</mark>

<figure><img src="https://camo.githubusercontent.com/a3ddf0bea588acb98e6f4d426f9e32ea5c37e2656362705d122fe0b09bdf7e77/68747470733a2f2f692e696d6775722e636f6d2f655757765356362e706e67" alt=""><figcaption></figcaption></figure>

What IP address was the destination IP in the alert? Enter your answer in a defanged format.&#x20;

&#x20;<mark style="color:green;">169\[.]239\[.]128\[.]11</mark>

<figure><img src="https://camo.githubusercontent.com/8eaa39b189d396cc39133eb3d96bcd242bc7ed8ba4d51bd335740dfb826b81b1/68747470733a2f2f692e696d6775722e636f6d2f5563496f4265412e706e67" alt=""><figcaption></figcaption></figure>

Inspect the IP address in VirsusTotal. Under Relations > Passive DNS Replication, which domain has the most detections? Enter your answer in a defanged format.&#x20;

&#x20;<mark style="color:green;">fidufagios\[.]com</mark>

<figure><img src="https://camo.githubusercontent.com/58cc88ff415ef74616f839a94310e72b4d44399c35d140fb5b74a642bf7602fa/68747470733a2f2f692e696d6775722e636f6d2f71496635376b542e706e67" alt=""><figcaption></figcaption></figure>

Still in VirusTotal, under Community, what threat group is attributed to this IP address?

&#x20;<mark style="color:green;">TA505</mark>

<figure><img src="https://camo.githubusercontent.com/6f97736de1a64f4de839650e4529409d442ad4d9e557d10c022bd955a1fc73f7/68747470733a2f2f692e696d6775722e636f6d2f6f62654835686c2e706e67" alt=""><figcaption></figcaption></figure>

What is the malware family?

&#x20;<mark style="color:green;">MirrorBlast</mark>

<figure><img src="https://camo.githubusercontent.com/8817dd18dcea5e4cb130e19222f67178afbeffcf3eb6139b4f0d7cdcdee4aa56/68747470733a2f2f692e696d6775722e636f6d2f536253353753522e706e67" alt=""><figcaption></figcaption></figure>

Do a search in VirusTotal for the domain from question 4. What was the majority file type listed under Communicating Files?

&#x20;<mark style="color:green;">Windows Installer</mark>

<figure><img src="https://camo.githubusercontent.com/9aa4de495313c6f371816c408d532a19cfb0feea967e5d1555dbbf54009bab9e/68747470733a2f2f692e696d6775722e636f6d2f5075357a5256772e706e67" alt=""><figcaption></figcaption></figure>

Inspect the web traffic for the flagged IP address; what is the user-agent in the traffic?

&#x20;<mark style="color:green;">REBOL View 2.7.8.3.1</mark>

<figure><img src="https://camo.githubusercontent.com/301eb71e1e319081b2957ebf88d38825a3d6d221d7e7740c07d2dfcff1d599c5/68747470733a2f2f692e696d6775722e636f6d2f614438437277542e706e67" alt=""><figcaption></figcaption></figure>

Retrace the attack; there were multiple IP addresses associated with this attack. What were two other IP addresses? Enter the IP addressed defanged and in numerical order. (format: IPADDR,IPADDR)

<mark style="color:green;">185\[.]10\[.]68\[.]235,192\[.]36\[.]27\[.]92</mark>

From my analysis and information gathering with VirusTotal I found 3 IP addresses, but answer wise there were only 2

&#x20;

<figure><img src="https://camo.githubusercontent.com/7467c255e4007cde04d5bcc5aaa730639660d810628b861a0d371be5330eda1d/68747470733a2f2f692e696d6775722e636f6d2f516551445551312e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/09857959dc6ddb0822e25483c822654ba4ee32a7ee078e6c51dc7666ece50117/68747470733a2f2f692e696d6775722e636f6d2f336d6970766d6c2e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/98acd9217596a46ee51fc5be4c3ee54121267d7405c65f359536835823a61159/68747470733a2f2f692e696d6775722e636f6d2f79314f766949762e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/3a6ab530502a90757870ca65acafc927ffdcf3aefd3eb7f6dbdf3dec049e4cc8/68747470733a2f2f692e696d6775722e636f6d2f37366f4d4a79492e706e67" alt=""><figcaption></figcaption></figure>



What were the file names of the downloaded files? Enter the answer in the order to the IP addresses from the previous question. (format: file.xyz,file.xyz)

<mark style="color:green;">filter.msi,10opd3r\_load.msi</mark>

&#x20;**`We know the IP addresses but as we can see there is missing file name, What I did is export the file with shark and check the hash and go to VirusTotal to find the name`**

<figure><img src="https://camo.githubusercontent.com/2d23d2521c74828a0ea4ee17802c2ec6333b053049a8c56adb174f3ab9568546/68747470733a2f2f692e696d6775722e636f6d2f59557163596d692e706e67" alt=""><figcaption></figcaption></figure>

<figure><img src="https://camo.githubusercontent.com/f94feba89e7d76ccb1583a46bef5961759d4a9ec2b4acaae2c94c244786afb57/68747470733a2f2f692e696d6775722e636f6d2f6c7646353370342e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/a451d21089c26742138266468fe64bd8f9f54dbc51447b7b58775b7c43ef2716/68747470733a2f2f692e696d6775722e636f6d2f306a72324d46672e706e67" alt=""><figcaption></figcaption></figure>

Inspect the traffic for the first downloaded file from the previous question. Two files will be saved to the same directory. What is the full file path of the directory and the name of the two files? (format: C:\path\file.xyz,C:\path\file.xyz)

&#x20;<mark style="color:green;">C:\ProgramData\001\arab.bin,C:\ProgramData\001\arab.exe</mark>

<figure><img src="https://camo.githubusercontent.com/901827c3f0e209f9f385c35e99f41ccdc28a0349d914f467da9cca4f36104214/68747470733a2f2f692e696d6775722e636f6d2f316873725561762e706e67" alt=""><figcaption></figcaption></figure>

Now do the same and inspect the traffic from the second downloaded file. Two files will be saved to the same directory. What is the full file path of the directory and the name of the two files? (format: C:\path\file.xyz,C:\path\file.xyz)

<mark style="color:green;">C:\ProgramData\Local\Google\rebol-view-278-3-1.exe,C:\ProgramData\Local\Google\exemple.exe</mark>

&#x20;

<figure><img src="https://camo.githubusercontent.com/e67b6aae8d9dcab91cf8dca35dcb011881db5880f2c86f024bb6a68a0307c514/68747470733a2f2f692e696d6775722e636f6d2f65557a587754482e706e67" alt=""><figcaption></figcaption></figure>
