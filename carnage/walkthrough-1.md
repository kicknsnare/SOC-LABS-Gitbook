# Walkthrough 1

\
What was the date and time for the first HTTP connection to the malicious IP?

(answer format: yyyy-mm-dd hh:mm:ss)

&#x20;<mark style="color:green;">2021-09-24 16:44:38</mark>

<figure><img src="https://camo.githubusercontent.com/3c7f5f8f241d4016177aa895ce6c9aa0130f96c2fcdfb32543f8bcd9f9bc830d/68747470733a2f2f692e696d6775722e636f6d2f5473613543705a2e706e67" alt=""><figcaption></figcaption></figure>

What is the name of the zip file that was downloaded?\
&#x20;<mark style="color:green;">documents.zip</mark>

<figure><img src="https://camo.githubusercontent.com/e4f027b2c67c6686f55815e76afc022c2de4b0bc59a03bdaa7a427388c51e580/68747470733a2f2f692e696d6775722e636f6d2f744259777773752e706e67" alt=""><figcaption></figcaption></figure>

What was the domain hosting the malicious zip file?\
&#x20;<mark style="color:green;">attirenepal.com</mark>

<figure><img src="https://camo.githubusercontent.com/e17b6f2929de044c4c5ead2ed27ab80f272c7b3a1a3a85f3312133f052265a09/68747470733a2f2f692e696d6775722e636f6d2f703972706a56672e706e67" alt=""><figcaption></figcaption></figure>

Without downloading the file, what is the name of the file in the zip file?\


&#x20;<mark style="color:green;">chart-1530076591.xls</mark>

<figure><img src="https://camo.githubusercontent.com/2ad0b76652c219f0470c9f9191f284f37f29bc05b009cd46dfa554aa55188d6b/68747470733a2f2f692e696d6775722e636f6d2f5a6475696947442e706e67" alt=""><figcaption></figcaption></figure>

What is the name of the webserver of the malicious IP from which the zip file was downloaded?\
<mark style="color:green;">LiteSpeed</mark>

&#x20;

<figure><img src="https://camo.githubusercontent.com/714cbd1521813bfc926eb91940e282f3ab425951f742f331f28bd2ad84fd6c0f/68747470733a2f2f692e696d6775722e636f6d2f4e615972634e492e706e67" alt=""><figcaption></figcaption></figure>

What is the version of the webserver from the previous question?\
<mark style="color:green;">PHP/7.2.34</mark>

&#x20;

<figure><img src="https://camo.githubusercontent.com/50e7b6d8eda636c347b9a51d0ead2ca5a7eb9da20aca4b7fe4f50c58111360bb/68747470733a2f2f692e696d6775722e636f6d2f6c306275695a7a2e706e67" alt=""><figcaption></figcaption></figure>

Malicious files were downloaded to the victim host from multiple domains. What were the three domains involved with this activity?

HINT: Check HTTPS traffic. Narrow down the timeframe from 16:45:11 to 16:45:30.

&#x20;<mark style="color:green;">finejewels.com.au, thietbiagt.com, new.americold.com</mark>

<figure><img src="https://camo.githubusercontent.com/c7e875cabd74227fb21fdd0de63b89cf42a9e971d1a049959cad480c73525156/68747470733a2f2f692e696d6775722e636f6d2f7641654c5254552e706e67" alt=""><figcaption></figcaption></figure>

Which certificate authority issued the SSL certificate to the first domain from the previous question?

<mark style="color:green;">GoDaddy</mark>

<figure><img src="https://camo.githubusercontent.com/407a3b8f20ae1852f1fd77fc6a4a82f2451eceed87c73b3627922a815e762092/68747470733a2f2f692e696d6775722e636f6d2f6353534f4139492e706e67" alt=""><figcaption></figcaption></figure>
