# 300 Series Questions



## Questions 1 & 2



```splunk-spl
index="botsv2" mallory host="MACLORY-AIR13"
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/db9c206b317108f40d62900474ec7c411851cd579072ccf1c22a489cfcada9fc/68747470733a2f2f692e696d6775722e636f6d2f50713352444a442e706e67" alt=""><figcaption></figcaption></figure>

```splunk-spl
index="botsv2" mallory host="MACLORY-AIR13" (*.ppt OR *.pptx)
```

```splunk-spl
index="botsv2" host="MACLORY-AIR13"  *.crypt sourcetype=ps
```

## Questions 3 & 7

```splunk-spl
index="botsv2" kutekitten "\\/Users\\/mkraeusen\\/Downloads"
```

```splunk-spl
index="botsv2" kutekitten usb vendor
```



## Walkthrough

\
Mallory's critical PowerPoint presentation on her MacBook gets encrypted by ransomware on August 18. What is the name of this file after it was encrypted?

```splunk-spl
index="botsv2" mallory host="MACLORY-AIR13" (*.ppt OR *.pptx)
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/666bce2a9126ba622f2da0343d994191bea0bd7fef76f871b97cf4736576ac63/68747470733a2f2f692e696d6775722e636f6d2f6c58356f4644322e706e67" alt=""><figcaption></figcaption></figure>

There is a Games of Thrones movie file that was encrypted as well. What season and episode is it?&#x20;

```splunk-spl
index="botsv2" host="MACLORY-AIR13"  *.crypt sourcetype=ps
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/a59336fec6251c558db4c84969a2b6b65115647cf6b0866c5be8503e87241a46/68747470733a2f2f692e696d6775722e636f6d2f665162316e47482e706e67" alt=""><figcaption></figcaption></figure>

Kevin Lagerfield used a USB drive to move malware onto kutekitten, Mallory's personal MacBook. She ran the malware, which obfuscates itself during execution. Provide the vendor name of the USB drive Kevin likely used. Answer Guidance: Use time correlation to identify the USB drive.\


<figure><img src="https://camo.githubusercontent.com/24fd8b5c6e6780543df72367df14ac3e9cfcf4b74b07ea5e72d3c69162ab043f/68747470733a2f2f692e696d6775722e636f6d2f494470473655492e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/b86cdfde5ba263aada05798327f9b29acc198c06a9532130b8683d7bc7224ba2/68747470733a2f2f692e696d6775722e636f6d2f766e514a4938572e706e67" alt=""><figcaption></figcaption></figure>

What programming language is at least part of the malware from the question above written in?\


&#x20;

<figure><img src="https://camo.githubusercontent.com/d4a5f46759abb9d61279fc85daacd6dde982087b833b7d8b3ebc8fb3b539de61/68747470733a2f2f692e696d6775722e636f6d2f4e6349536530332e706e67" alt=""><figcaption></figcaption></figure>

We have the path, I assume that she downloaded the malware and it went to the Downloads folder

```splunk-spl
index="botsv2" kutekitten "\\/Users\\/mkraeusen\\/Downloads"
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/33a710cd1c0bad09e519fac68fa0ec74d72b298abf7d0c00f39c773250ac29cd/68747470733a2f2f692e696d6775722e636f6d2f78686d756a67702e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/a5bd1ff88b03f1219a4e1fe51a61b1a65ef1d7c324d4f1735e626d1acbfd0631/68747470733a2f2f692e696d6775722e636f6d2f39316a784d4a552e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/cdb9b7f1b4b03d455663f294d53be69a0efc08eea38e887b3a8b1834adc16f49/68747470733a2f2f692e696d6775722e636f6d2f746450584335512e706e67" alt=""><figcaption></figcaption></figure>

When was this malware first seen in the wild? Answer Guidance: YYYY-MM-DD\
&#x20;

<figure><img src="https://camo.githubusercontent.com/c34b20aa87f549e250c8a0af920191f02758e97f09b889321a1c89f502e23789/68747470733a2f2f692e696d6775722e636f6d2f6b587769426f452e706e67" alt=""><figcaption></figcaption></figure>



The malware infecting kutekitten uses dynamic DNS destinations to communicate with two C\&C servers shortly after installation. What is the fully-qualified domain name (FQDN) of the first (alphabetically) of these destinations?\
&#x20;

<figure><img src="https://camo.githubusercontent.com/fb01d327af9d8c60e838987f8e23061b5840b9d7ba0166e2130446c4fed2db49/68747470733a2f2f692e696d6775722e636f6d2f3833476144434e2e706e67" alt=""><figcaption></figcaption></figure>

From the question above, what is the fully-qualified domain name (FQDN) of the second (alphabetically) contacted C\&C server?

Look the second result in the image from above
