# \[Email Analysis]

The Boogeyman is here!\


Julianne, a finance employee working for Quick Logistics LLC, received a follow-up email regarding an unpaid invoice from their business partner, B Packaging Inc. Unbeknownst to her, the attached document was malicious and compromised her workstation.

\


<figure><img src="https://tryhackme-images.s3.amazonaws.com/user-uploads/5dbea226085ab6182a2ee0f7/room-content/28bbc4ff07b8ad16da155894ca3d2d73.png" alt=""><figcaption></figcaption></figure>

The security team was able to flag the suspicious execution of the attachment, in addition to the phishing reports received from the other finance department employees, making it seem to be a targeted attack on the finance team. Upon checking the latest trends, the initial TTP used for the malicious attachment is attributed to the new threat group named Boogeyman, known for targeting the logistics sector.

You are tasked to analyse and assess the impact of the compromise.





&#x20;What is the email address used to send the phishing email?

<figure><img src="https://camo.githubusercontent.com/27350f2cf765217073527cf425716a3c618280a5f18dade2e7503c6ff9835645/68747470733a2f2f692e696d6775722e636f6d2f393556385635682e706e67" alt=""><figcaption></figcaption></figure>

What is the email address of the victim?

Take a look at the image from the last question

What is the name of the third-party mail relay service used by the attacker based on the DKIM-Signature and List-Unsubscribe headers?\


<figure><img src="https://camo.githubusercontent.com/1b83caa904fed65d0e4541af20c2ccfc7d4bc5194c5a86897b39d15225487c50/68747470733a2f2f692e696d6775722e636f6d2f33397a77536b6f2e706e67" alt=""><figcaption></figcaption></figure>

What is the name of the file inside the encrypted attachment?\


<figure><img src="https://camo.githubusercontent.com/7d0116fca5ec7939e8d6731bfc2273cf351ea98986eab7f112b75cd46007f99b/68747470733a2f2f692e696d6775722e636f6d2f57554f51464e412e706e67" alt=""><figcaption></figcaption></figure>

What is the password of the encrypted attachment?

<figure><img src="https://camo.githubusercontent.com/b7dff445f208cfbe746897b232a48aaa16c08e5ae1cf4521d3ba12cc20ac8193/68747470733a2f2f692e696d6775722e636f6d2f74483058644b6b2e706e67" alt=""><figcaption></figcaption></figure>

Based on the result of the lnkparse tool, what is the encoded payload found in the Command Line Arguments field?

```bash
lnkparse Invoice_20230103.lnk 
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/c66f4fe8057502b360e2abef9c614976ccc2315e499d4171e0a0ca6ccf449e0e/68747470733a2f2f692e696d6775722e636f6d2f417a764c3659632e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/d43622e98578088358e000a09f986cf19dd060793433b332024336bd10caafe3/68747470733a2f2f692e696d6775722e636f6d2f614c49326d65542e706e67" alt=""><figcaption></figcaption></figure>
