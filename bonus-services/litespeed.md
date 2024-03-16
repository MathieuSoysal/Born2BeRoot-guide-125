# ⚡ LiteSpeed

{% hint style="info" %}
<mark style="color:green;">LiteSpeed</mark>: It is a proprietary web server software. It is the fourth most popular web server, and is estimated to be used by 10% of websites.
{% endhint %}

1. Before installing any software, it is important to ensure that the system is up to date:

```sh
sudo apt update
```

2. and upgrade:

```sh
sudo apt upgrade
```

3. By default, OpenLiteSpeed is available in the Debian 11 base repository. So, you must run the following command to add the OpenLiteSpeed repository to your Debian system:

```sh
wget -O - https://repo.litespeed.sh | sudo bash
```

4. Again, we update the packages and install OpenLiteSpeed:

```sh
sudo apt update
sudo apt install openlitespeed
```

5. The default password for OpenLiteSpeed is 123456. We will change the password to something more secure with the following command:

```sh
sudo /usr/local/lsws/admin/misc/admpass.sh
```

6. We configure the firewall to allow connections through ports 8088 and 7080. We then add the rules in the port forwarding:

```sh
sudo ufw allow 8088/tcp
sudo ufw allow 7080/tcp
sudo ufw reload
```

7. Port forwarding rules:

<figure><img src="../.gitbook/assets/image (187).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
It could be better if the port are not equals like 7081 : 7080 or 8089 : 8088
{% endhint %}

8. Once we have completed the previous step we can connect. We will put in the search engine of our browser `localhost:7081` we provide our login credentials and we will have access to everything.

<figure><img src="../.gitbook/assets/image (188).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (189).png" alt=""><figcaption></figcaption></figure>
