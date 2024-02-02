# Walkthrough



## Question 1

```splunk-spl
index="botsv2" amber sourcetype="pan:traffic"
```

&#x20;<mark style="color:blue;">**`IP ADDRESS 10.0.2.101`**</mark>

<figure><img src="https://camo.githubusercontent.com/4caa1d958d37d94bc13bcb4b1f5ac0df4034d08c904569b5c7501f0dc900cdd7/68747470733a2f2f692e696d6775722e636f6d2f356547793255542e706e67" alt=""><figcaption></figcaption></figure>

```splunk-spl
index="botsv2" src_ip="10.0.2.101" sourcetype="stream:http" 
| dedup  site
| table site
```

Remember

In this exercise, you assume the persona of Alice Bluebird, the analyst who successfully assisted Wayne Enterprises and was recommended to Grace Hoppy at Frothly (_a beer company_) to assist them with their recent issues.

```splunk-spl
index="botsv2" src_ip="10.0.2.101" sourcetype="stream:http" *beer*
| dedup  site
| table site
```



## Questions 2-7

```splunk-spl
index="botsv2" src_ip="10.0.2.101" sourcetype="stream:http" site="www.berkbeer.com"
```

```splunk-spl
index="botsv2" src_ip="10.0.2.101" sourcetype="stream:http"  site="www.berkbeer.com" 
| table uri_path
```

```splunk-spl
index="botsv2" sourcetype="stream:smtp" index="botsv2" sourcetype="stream:smtp" *aturing@froth.ly*  *berkbeer*
```



\
Amber Turing was hoping for Frothly to be acquired by a potential competitor which fell through, but visited their website to find contact information for their executive team. What is the website domain that she visited?

```splunk-spl
index="botsv2" src_ip="10.0.2.101" sourcetype="stream:http" *beer*
| dedup  site
| table site
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/4b55922a5f68ac777cc503e1f0fbe31a2b87ab0bbb5bf52b57f563111fa13149/68747470733a2f2f692e696d6775722e636f6d2f7a4238346e30522e706e67" alt=""><figcaption></figcaption></figure>

Amber found the executive contact information and sent him an email. What image file displayed the executive's contact information? Answer example: /path/image.ext

```splunk-spl
index="botsv2" src_ip="10.0.2.101" sourcetype="stream:http"  site="www.berkbeer.com" 
| table uri_path
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/dd9485c3bb139ad0350d8e91974ad4c99e54e664c7063b90e290bb4ae1d43386/68747470733a2f2f692e696d6775722e636f6d2f68796b707754382e706e67" alt=""><figcaption></figcaption></figure>

What is the CEO's name? Provide the first and last name.\


```splunk-spl
index="botsv2" sourcetype="stream:smtp" index="botsv2" sourcetype="stream:smtp" *aturing@froth.ly*  *berkbeer*
```

<figure><img src="https://camo.githubusercontent.com/7e8f550d771c0b29b1825c0aecb15dc46e32ae400b73b17ba183f8554a6fbd36/68747470733a2f2f692e696d6775722e636f6d2f3172796e4e34682e706e67" alt=""><figcaption></figcaption></figure>

What is the CEO's email address?

We can see it in the previous image



After the initial contact with the CEO, Amber contacted another employee at this competitor. What is that employee's email address?

Scrolling down to see some emails we can find something interesting&#x20;

```splunk-spl
index="botsv2" sourcetype="stream:smtp" index="botsv2" sourcetype="stream:smtp" *aturing@froth.ly*  *berkbeer*
```

What is the name of the file attachment that Amber sent to a contact at the competitor?\
&#x20;

<figure><img src="https://camo.githubusercontent.com/095c978f2318e170f290d0a08400b0e50964d6c23adbe4327276d7d2df315972/68747470733a2f2f692e696d6775722e636f6d2f307557386344632e706e67" alt=""><figcaption></figcaption></figure>



What is Amber's personal email address?

&#x20;

<figure><img src="https://camo.githubusercontent.com/bf6a6ae862334337cda1350fb57c9c3977f4e0b87ea25e2eeaec4a8790339e0f/68747470733a2f2f692e696d6775722e636f6d2f506e374f6636512e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/faf77efe862d70bb239b89671a308350b63744e56608502888a673e639ee07e4/68747470733a2f2f692e696d6775722e636f6d2f674837364e54432e706e67" alt=""><figcaption></figcaption></figure>

