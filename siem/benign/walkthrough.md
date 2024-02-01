# Walkthrough

\
How many logs are ingested from the month of March, 2022?

&#x20;

<figure><img src="https://camo.githubusercontent.com/aafd03d860b418cdbab26657648159ca33fb9449f4102802b40c451549d1bf6c/68747470733a2f2f692e696d6775722e636f6d2f30537a32564c732e706e67" alt=""><figcaption></figcaption></figure>

Imposter Alert: There seems to be an imposter account observed in the logs, what is the name of that user?

```splunk-spl
index=win_eventlogs 
| stats count by UserName
```

<figure><img src="https://camo.githubusercontent.com/115f983a578f50f053e2523f6635d77147af9b659c0d973032fceb6781a0efe0/68747470733a2f2f692e696d6775722e636f6d2f47734a3455686a2e706e67" alt=""><figcaption></figcaption></figure>

Which user from the HR department was observed to be running scheduled tasks?

```splunk-spl
#1
index=win_eventlogs UserName"haroon" OR UserName="Chris.fort" OR Username="Daina"
#2
I added | stats count by ProcessName
Then I looked for something that seemed to be a task

```

<figure><img src="https://camo.githubusercontent.com/423427cf947d3b9fef63de32f52f1d04f9b3e1e36cf491db37e543afd57cb01b/68747470733a2f2f692e696d6775722e636f6d2f554b4d6634326d2e706e67" alt=""><figcaption></figcaption></figure>

Which user from the HR department executed a system process (LOLBIN) to download a payload from a file-sharing host.

```splunk-spl
index=win_eventlogs (UserName="haroon" OR UserName="Chris.fort" OR UserName="Daina") 
| stats count by ProcessName
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/bc4896a3e480029f36d94f221eaa535322f545ec7d122b75fa5c4374d58cae89/68747470733a2f2f692e696d6775722e636f6d2f48656e4c6a4e372e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/f5e82b859033e7c0f08334320719bccfb20bce92220993a6c10b07c7e3e12330/68747470733a2f2f692e696d6775722e636f6d2f4275754c5559792e706e67" alt=""><figcaption></figcaption></figure>

To bypass the security controls, which system process (lolbin) was used to download a payload from the internet?

&#x20;

<figure><img src="https://camo.githubusercontent.com/8013b6fbfbd793ae6e00668a9729a076d5ff750a6733e601386538830865f3a7/68747470733a2f2f692e696d6775722e636f6d2f674471325966642e706e67" alt=""><figcaption></figcaption></figure>

<figure><img src="https://camo.githubusercontent.com/733a83f08b93137849a73fd93ab9184c0dddcd56ba4e37c5f608dfe8f989cd29/68747470733a2f2f692e696d6775722e636f6d2f637434786639512e706e67" alt=""><figcaption></figcaption></figure>

What was the date that this binary was executed by the infected host? format (YYYY-MM-DD)

<figure><img src="https://camo.githubusercontent.com/94aadef76bc215ada6de14906aa9ff788cfbe9cf1422ec68f2d09ae547aeb25a/68747470733a2f2f692e696d6775722e636f6d2f3363744f6b6f782e706e67" alt=""><figcaption></figcaption></figure>

Which third-party site was accessed to download the malicious payload?

<figure><img src="https://camo.githubusercontent.com/7545c4a6837bacb1461db6c2fd754feb99315bae0768d71d5b11352683c5460d/68747470733a2f2f692e696d6775722e636f6d2f585a61746c44332e706e67" alt=""><figcaption></figcaption></figure>

What is the name of the file that was saved on the host machine from the C2 server during the post-exploitation phase?

&#x20;We can see it in some of the screenshots, benign.exe

The suspicious file downloaded from the C2 server contained malicious content with the pattern THM{..........}; what is that pattern?

<figure><img src="https://camo.githubusercontent.com/87f5073f527436cf5b138d36d39ee7e6569a012e1a56fa070b5468e4ae5809ab/68747470733a2f2f692e696d6775722e636f6d2f436a77457079582e706e67" alt=""><figcaption></figcaption></figure>

What is the URL that the infected host connected to?

&#x20;

<figure><img src="https://camo.githubusercontent.com/c4d1dc61c4ba8d5ab2849888d452fb31e3276a3b0e58bb019ad591843df39e1d/68747470733a2f2f692e696d6775722e636f6d2f304e71596842702e706e67" alt=""><figcaption></figcaption></figure>
