---
description: >-
  Begining with this section, we will create a file in /etc/sudoerd.d/. The file
  will serve the purpouse of storing our sudo policy.
---

# 🔐 sudo policies

1. The command that we will use will be&#x20;

```sh
touch /etc/sudoers.d/sudo_config
```

<figure><img src="../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

2. Then we must create a directory as is asked in the subject in _/var/log/_ because each commands need to be logged, the input and output. We will use:

```sh
mkdir /var/log/sudo
```

<figure><img src="../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

3. We must edit the file that we created in the first step of this section. Use any text editor, but for this guide as is in every screenshot we will use nano. Use:

```sh
nano /etc/sudoers.d/sudo_config
```

<figure><img src="../.gitbook/assets/image (162).png" alt=""><figcaption></figcaption></figure>

4. Once we are editing the file we must set it up with the following commands:

```
Defaults  passwd_tries=3
Defaults  badpass_message="Mensaje de error personalizado"
Defaults  logfile="/var/log/sudo/sudo_config"
Defaults  log_input, log_output
Defaults  iolog_dir="/var/log/sudo"
Defaults  requiretty
Defaults  secure_path="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin"
```

As it should be on the file:\
![](<../.gitbook/assets/image (163).png>)



{% hint style="info" %}
<mark style="color:green;">passwd\_tries=3</mark>: Total tries for entering the sudo password.
{% endhint %}

{% hint style="info" %}
<mark style="color:green;">badpass\_message="message"</mark>: The message that will show when the password failed.
{% endhint %}

{% hint style="info" %}
<mark style="color:green;">logfile="/var/log/sudo/sudo\_config"</mark>: Path where will the sudo logs will be stored.
{% endhint %}

{% hint style="info" %}
<mark style="color:green;">log\_input, log\_output</mark>: What will be logged.
{% endhint %}

{% hint style="info" %}
<mark style="color:green;">iolog\_dir="/var/log/sudo"</mark>: What will be logged.
{% endhint %}

{% hint style="info" %}
<mark style="color:green;">requiretty</mark>: TTY become required
{% endhint %}

{% hint style="info" %}
<mark style="color:green;">secure\_path="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin"</mark>: Folders that will be excluded of sudo
{% endhint %}
