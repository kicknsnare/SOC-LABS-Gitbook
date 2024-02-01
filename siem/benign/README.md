---
description: Challenge room to investigate a compromised host.
---

# 🐞 Benign

{% embed url="https://tryhackme.com/room/benign" %}

One of the client’s IDS indicated a potentially suspicious process execution indicating one of the hosts from the HR department was compromised. Some tools related to network information gathering / scheduled tasks were executed which confirmed the suspicion. Due to limited resources, we could only pull the process execution logs with Event ID: 4688 and ingested them into Splunk with the index win\_eventlogs for further investigation.\


About the Network Information

The network is divided into three logical segments. It will help in the investigation.\


**IT Department**\


* James
* Moin
* Katrina

**HR department**\


* Haroon
* Chris
* Diana

**Marketing department**

* Bell
* Amelia
* Deepak
