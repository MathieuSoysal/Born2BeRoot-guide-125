# 📶 Installing & configuring SSH

{% hint style="info" %}
<mark style="color:green;">SSH</mark>: The acronym SSH stands for "<mark style="color:green;">S</mark>ecure <mark style="color:green;">Sh</mark>ell." The SSH protocol was designed as a secure alternative to unsecured remote shell protocols. It utilizes a client-server paradigm, in which clients and servers communicate via a secure channel.
{% endhint %}

1. First thing, we should update the system using

```sh
sudo apt update
```

2. Following up we will install the main tool for remote access with the SSH protocol, using <mark style="color:green;">OpenSSH</mark>. The installation requieres the package:

```sh
sudo apt install openssh-server
```

When we are asked for confirmation we will write `y`, and just then the installation will proceed.

<figure><img src="../../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>

4. Anywan curious that the installation have been realices without problems we can use:

```sh
sudo service ssh status
```

and it will show how is the state of it. **Active** must be show to continue.\
\
![](<../../.gitbook/assets/image (151).png>)
