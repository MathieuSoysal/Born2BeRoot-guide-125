# 🔥 Installing & configuring UFW 🔥🧱 Firewall

{% hint style="info" %}
[UFW](https://en.wikipedia.org/wiki/Uncomplicated\_Firewall): It is a [firewall](https://en.wikipedia.org/wiki/Firewall\_\(computing\)) which use the command line for setting up [iptables](https://en.wikipedia.org/wiki/Iptables) using a small number of easy commands.
{% endhint %}

1. First things first, we need to install the packages for UFW, for that we will use:

```sh
sudo apt install ufw
```

then when we are asked for confirmation type `y` and the installation will proceed.

<figure><img src="../../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>

2. When we are done with it, we want to start it using the command:

```sh
sudo ufw enable
```

and then it have to show us the the _firewall is ative._
