# 200 Series Questions



## Question 1

```splunk-spl
index="botsv2" amber tor install
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/a27e7bf8360c4c02f8871ab2e9922555045324a5336406323f8143a409c5e3e5/68747470733a2f2f692e696d6775722e636f6d2f6f4370335736702e706e67" alt=""><figcaption></figcaption></figure>

## Question 2 & 3

Public IP address:

```splunk-spl
index="botsv2" brewertalk.com
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/a47b76da7628313170c962f57e01851eff979d91b37ed9ef1e71eeaf34136487/68747470733a2f2f692e696d6775722e636f6d2f4d6a68476f52752e706e67" alt=""><figcaption></figcaption></figure>

IP web scan:

```splunk-spl
index="botsv2" tor brewertalk.com
```

<figure><img src="https://camo.githubusercontent.com/dad6b6345fcb1224b991fcb2ddf80a11202714ea9a9be4136c194765bee828bf/68747470733a2f2f692e696d6775722e636f6d2f55713734394d322e706e67" alt=""><figcaption></figcaption></figure>

45.77.65.211



## Question 4 & 5

```splunk-spl
index="botsv2" src_ip="45.77.65.211" uri_path="/member.php"
```

## Questions 6 & 7

```splunk-spl
index="botsv2" 1bc3eab741900ab25c98eee86bf20feb
```



## Walkthrough

\
What version of TOR Browser did Amber install to obfuscate her web browsing? Answer guidance: Numeric with one or more delimiter.

&#x20;

<figure><img src="https://camo.githubusercontent.com/a27e7bf8360c4c02f8871ab2e9922555045324a5336406323f8143a409c5e3e5/68747470733a2f2f692e696d6775722e636f6d2f6f4370335736702e706e67" alt=""><figcaption></figcaption></figure>

What is the public IPv4 address of the server running www.brewertalk.com?\


Public IP address:

```splunk-spl
index="botsv2" brewertalk.com
```

<figure><img src="https://camo.githubusercontent.com/a47b76da7628313170c962f57e01851eff979d91b37ed9ef1e71eeaf34136487/68747470733a2f2f692e696d6775722e636f6d2f4d6a68476f52752e706e67" alt=""><figcaption></figcaption></figure>

Provide the IP address of the system used to run a web vulnerability scan against www.brewertalk.com.\


```splunk-spl
index="botsv2" tor brewertalk.com
```

<figure><img src="https://camo.githubusercontent.com/dad6b6345fcb1224b991fcb2ddf80a11202714ea9a9be4136c194765bee828bf/68747470733a2f2f692e696d6775722e636f6d2f55713734394d322e706e67" alt=""><figcaption></figcaption></figure>

The IP address from Q#2 is also being used by a likely different piece of software to attack a URI path. What is the URI path? Answer guidance: Include the leading forward slash in your answer. Do not include the query string or other parts of the URI. Answer example: /phpinfo.php

<figure><img src="https://camo.githubusercontent.com/ae01d9002db6a11573af8dd3e5aa49edd96c3679997e7f8548772c04b0866c9c/68747470733a2f2f692e696d6775722e636f6d2f4e386f344e51772e706e67" alt=""><figcaption></figcaption></figure>

What SQL function is being abused on the URI path from the previous question?

```splunk-spl
index="botsv2" src_ip="45.77.65.211" uri_path="/member.php" 
| dedup form_data 
| table form_data
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/6099b75551404e1a29cc5e0842fc3dd9fa2d397b04687f6503b81dd2ffa679ca/68747470733a2f2f692e696d6775722e636f6d2f4e716d57616d442e706e67" alt=""><figcaption></figcaption></figure>

What was the value of the cookie that Kevin's browser transmitted to the malicious URL as part of an XSS attack? Answer guidance: All digits. Not the cookie name or symbols like an equal sign.\


```splunk-spl
index="botsv2" kevin sourcetype="stream:http" brewertalk.com *java*
```

<figure><img src="https://camo.githubusercontent.com/8f4f494f37b8f2f54689bf067685d36224b00631d8da9044c0afe61373a425c9/68747470733a2f2f692e696d6775722e636f6d2f6c5437753734492e706e67" alt=""><figcaption></figcaption></figure>

What brewertalk.com username was maliciously created by a spear phishing attack?\


```splunk-spl
index="botsv2" 1bc3eab741900ab25c98eee86bf20feb
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/c2528c9be23f5b795a49e69bf5f6241a65f5dedd226819520014a2a91e8d9c7c/68747470733a2f2f692e696d6775722e636f6d2f4d4b6b6f656d452e706e67" alt=""><figcaption></figcaption></figure>
