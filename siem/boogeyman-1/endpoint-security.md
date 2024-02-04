# \[Endpoint Security]

Based on the initial findings, we discovered how the malicious attachment compromised Julianne's workstation:

* A PowerShell command was executed.
* Decoding the payload reveals the starting point of endpoint activities.&#x20;

Investigation Guide\


With the following discoveries, we should now proceed with analysing the PowerShell logs to uncover the potential impact of the attack:

* Using the previous findings, we can start our analysis by searching the execution of the initial payload in the PowerShell logs.
* Since the given data is JSON, we can parse it in CLI using the `jq` command.
* Note that some logs are redundant and do not contain any critical information; hence can be ignored.

JQ Cheatsheet

﻿jq is a lightweight and flexible command-line JSON processor. This tool can be used in conjunction with other text-processing commands.&#x20;

You may use the following table as a guide in parsing the logs in this task.

Note: You must be familiar with the existing fields in a single log.

| Parse all JSON into beautified output                                         | <p><code>cat powershell.json | jq</code> <br></p>                                            |
| ----------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| Print all values from a specific field without printing the field             | <p><code>cat powershell.json | jq '.Field1'</code><br></p>                                   |
| <p>Print all values from a specific field<br></p>                             | <p><code>cat powershell.json | jq '{Field1}'</code><br></p>                                  |
| Print values from multiple fields                                             | <p><code>cat powershell.json | jq '{Field1, Field2}'</code><br></p>                          |
| Sort logs based on their Timestamp                                            | <p><code>cat powershell.json | jq -s -c 'sort_by(.Timestamp) | .[]'</code><br></p>           |
| <p>Sort logs based on their Timestamp and print multiple field values<br></p> | <p><code>cat powershell.json | jq -s -c 'sort_by(.Timestamp) | .[] | {Field}'</code><br></p> |

You may continue learning this tool via its [documentation](https://stedolan.github.io/jq/manual/).\


Answer the questions belowWhat are the domains used by the attacker for file hosting and C2? Provide the domains in alphabetical order. (e.g. a.domain.com,b.domain.com)&#x20;

&#x20;

```bash
cat powershell.json | jq -s -c 'sort_by(.Timestamp) | .[] | {ScriptBlockText}' 
```

&#x20;

<figure><img src="https://camo.githubusercontent.com/8773249db15ed95fde24a0287b14bcc97f9c0a6b2e497c9f56f122b1a4c1f3c5/68747470733a2f2f692e696d6775722e636f6d2f4d76627a376e642e706e67" alt=""><figcaption></figcaption></figure>

What is the name of the enumeration tool downloaded by the attacker?\
&#x20;

<figure><img src="https://camo.githubusercontent.com/aea9973b6b6bc0717d13289c13ec02c4df6b1684b1fae619c03fb5aed62999f8/68747470733a2f2f692e696d6775722e636f6d2f456148424e57762e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/7fc8bc0bf57a64c8a95665798adfb1756c15297d469692fb6b88b09647b76787/68747470733a2f2f692e696d6775722e636f6d2f6d7944774d694a2e706e67" alt=""><figcaption></figcaption></figure>

What is the file accessed by the attacker using the downloaded sq3.exe binary? Provide the full file path with escaped backslashes. Submit Hint

&#x20;

<figure><img src="https://camo.githubusercontent.com/3c40785c12e9eb0d83c370b5543386c766f0563f5fa59fc8b6eb8cb8e2cd2595/68747470733a2f2f692e696d6775722e636f6d2f5767364e4d5a792e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/b4417bff52e9eda2b13a5a55c6eee7c7450f7094928d01bb7b4c6c538b000ad7/68747470733a2f2f692e696d6775722e636f6d2f36506d413558512e706e67" alt=""><figcaption></figcaption></figure>

What is the software that uses the file in Q3?

Look the image from the previous question

What is the name of the exfiltrated file?\


&#x20;

<figure><img src="https://camo.githubusercontent.com/326e1e639cfd249f46a3f3175e1dd20c850f06889f825b9ff857c0a28ffbafb0/68747470733a2f2f692e696d6775722e636f6d2f355464373954672e706e67" alt=""><figcaption><p>For the following 3 questions</p></figcaption></figure>

What type of file uses the .kdbx file extension?

&#x20;

<figure><img src="https://camo.githubusercontent.com/3ff199712545a6732afa17bd90870c6d8a18de756189621a83692c9b0d1879dd/68747470733a2f2f692e696d6775722e636f6d2f4343307a6664642e706e67" alt=""><figcaption></figcaption></figure>

What is the encoding used during the exfiltration attempt of the sensitive file?\


Look the other questions

What is the tool used for exfiltration?\


Look the other questions\
