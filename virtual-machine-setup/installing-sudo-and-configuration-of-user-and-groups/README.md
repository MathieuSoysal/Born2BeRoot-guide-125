# 👤 Installing sudo & configuration of user and groups

{% hint style="info" %}
<mark style="color:green;">**sudo**</mark> is a [program](https://en.wikipedia.org/wiki/Computer\_program) for [Unix-like](https://en.wikipedia.org/wiki/Unix-like) computer [operating systems](https://en.wikipedia.org/wiki/Operating\_system) that enables users to run programs with the security privileges of another user, by default the [superuser](https://en.wikipedia.org/wiki/Superuser). It originally stood for "superuser do", as that was all it did, and it is its most common usage; however, the official Sudo project page lists it as "su 'do' ".
{% endhint %}



1. The beginning of the installation starts with changing user to root so we can install sudo, for this purpouse we write:

```bash
su
```

&#x20;`su` in the bash prompt and introduce the root password, in my case `Hola42bcn`.&#x20;



2. Once we are done we write down the command :&#x20;

```sh
apt install sudo
```

So the package manager install the required packages for sudo.



3. We must reboot machine so the changes can be applied. For that porpouse we will use the commando:

```shell
sudo reboot
```



4. Once the machine is rebooted we have to input the encryptation password and the login again. To check if sudo have been installed correctly we must switch to root user:

```sh
su
```

and then use the command:

```sh
sudo -V
```

