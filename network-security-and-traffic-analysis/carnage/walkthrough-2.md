# Walkthrough 2

\
What are the two IP addresses of the Cobalt Strike servers? Use VirusTotal (the Community tab) to confirm if IPs are identified as Cobalt Strike C2 servers. (answer format: enter the IP addresses in sequential order)&#x20;

&#x20;<mark style="color:green;">185.125.204.174, 185.106.96.158</mark>

<figure><img src="https://camo.githubusercontent.com/ad41b472129092737f6d33b1c8339388bb5aea1a126bcd7ba61a55b038c45312/68747470733a2f2f692e696d6775722e636f6d2f4b327162556e422e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/f7962d5ed65af8294b1ee36ecfc59c2810693ef8e6fc41c938b6f1dc0ab40336/68747470733a2f2f692e696d6775722e636f6d2f6c334f383062442e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/1653bb27f83fa0e1f2cf3639496f362a8211d129d80860b68f41286c83eefd31/68747470733a2f2f692e696d6775722e636f6d2f6e66726445394f2e706e67" alt=""><figcaption></figcaption></figure>

What is the Host header for the first Cobalt Strike IP address from the previous question?

&#x20; <mark style="color:green;">ocsp.verisign.com</mark>

<figure><img src="https://camo.githubusercontent.com/dcbf179f9cad0cff34d22d966f283272079bdc03c50427554328c573136debdf/68747470733a2f2f692e696d6775722e636f6d2f387467726639512e706e67" alt=""><figcaption></figcaption></figure>

\
What is the domain name for the first IP address of the Cobalt Strike server? You may use VirusTotal to confirm if it's the Cobalt Strike server (check the Community tab).&#x20;

&#x20;<mark style="color:green;">survmeter.live</mark>

<figure><img src="https://camo.githubusercontent.com/00adcda2eb256e39083831c845ea6c265e94c19c4b86fffd2a4fa771a611589d/68747470733a2f2f692e696d6775722e636f6d2f4653356e7230512e706e67" alt=""><figcaption></figcaption></figure>

What is the domain name of the second Cobalt Strike server IP?  You may use VirusTotal to confirm if it's the Cobalt Strike server (check the Community tab).&#x20;

<mark style="color:green;">securitybusinpuff.com</mark>

<figure><img src="https://camo.githubusercontent.com/1c1b4301aea1f2dcb0ba56c126cb4d8df9d556aca9dae5458076ebc43b3f0104/68747470733a2f2f692e696d6775722e636f6d2f3451584b4a54332e706e67" alt=""><figcaption></figcaption></figure>

What is the domain name of the post-infection traffic?

&#x20;<mark style="color:green;">maldivehost.net</mark>

<figure><img src="https://camo.githubusercontent.com/fa4746e2fddc1c795f7d14e5625cf3d10de9030c4c5e1ba62787722216090226/68747470733a2f2f692e696d6775722e636f6d2f414b7a564252782e706e67" alt=""><figcaption></figcaption></figure>



What are the first eleven characters that the victim host sends out to the malicious domain involved in the post-infection traffic?

<mark style="color:green;">zLIisQRWZI9</mark>

<figure><img src="https://camo.githubusercontent.com/5f9b7d03065b63e0eec0bb871a3b896b62f79e692cb114871938c19c7107e0ff/68747470733a2f2f692e696d6775722e636f6d2f656a4b666931372e706e67" alt=""><figcaption></figcaption></figure>

What was the length for the first packet sent out to the C2 server?&#x20;

&#x20;<mark style="color:green;">281</mark>

<figure><img src="https://camo.githubusercontent.com/0891c88ad279046690b6ada1ecaaed2c55a9169be3dfa7b3a70e5daa4356badf/68747470733a2f2f692e696d6775722e636f6d2f354d363177474b2e706e67" alt=""><figcaption></figcaption></figure>



What was the Server header for the malicious domain from the previous question?

&#x20;<mark style="color:green;">Apache/2.4.49 (cPanel) OpenSSL/1.1.1l mod\_bwlimited/1.4</mark>

<figure><img src="https://camo.githubusercontent.com/3c19675756ee703f9d1401a7e8cd1587463539706a379777695642a293ee43e1/68747470733a2f2f692e696d6775722e636f6d2f6442344348786e2e706e67" alt=""><figcaption></figcaption></figure>

The malware used an API to check for the IP address of the victim’s machine. What was the date and time when the DNS query for the IP check domain occurred? (answer format: yyyy-mm-dd hh:mm:ss UTC)

&#x20;<mark style="color:green;">2021-09-24 17:00:04</mark>

<figure><img src="https://camo.githubusercontent.com/1da5bd2d216389cc4fd22239d6b87a49d065dc03e7277749074b7d1bdb15309a/68747470733a2f2f692e696d6775722e636f6d2f615261736e71462e706e67" alt=""><figcaption></figcaption></figure>

What was the domain in the DNS query from the previous question?

Check Last Image

<mark style="color:green;">api.ipify.org</mark>

Looks like there was some malicious spam (malspam) activity going on. What was the first MAIL FROM address observed in the traffic? Submit

&#x20;<mark style="color:green;">farshin@mailfa.com</mark>

<figure><img src="https://camo.githubusercontent.com/4217c4392b2121edb79a9a1b357a933e8d6b007786152874a9e7ceb3e80359ea/68747470733a2f2f692e696d6775722e636f6d2f6d44556463434d2e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/45c108381dca7ee8a57e1a05b907d17541cfc4d152588865b615d75885b3b7cc/68747470733a2f2f692e696d6775722e636f6d2f753747634544312e706e67" alt=""><figcaption></figcaption></figure>

How many packets were observed for the SMTP traffic?

&#x20;<mark style="color:green;">1439</mark>

<figure><img src="https://camo.githubusercontent.com/bdeb8a0270bfd3bbc25024f246e933a9ff0b89773a9bad6533abc7e590ecd9c7/68747470733a2f2f692e696d6775722e636f6d2f34357a355a79662e706e67" alt=""><figcaption></figcaption></figure>
