# 📰 WordPress

{% hint style="info" %}
<mark style="color:green;">WordPress</mark>: It is a content management system focused on the creation of any type of website.
{% endhint %}

1. To install the latest version of WordPress we must first install wget and zip. To do this we will use the following command:

```sh
sudo apt install wget zip
```

{% hint style="info" %}
<mark style="color:green;">wget</mark>: It is a command line tool used to download files from the web.
{% endhint %}

{% hint style="info" %}
<mark style="color:green;">zip</mark>: It is a command line utility for compressing and decompressing files in ZIP format.
{% endhint %}

2. Once we have installed the packages we must locate ourselves in the folder /var/www/ with the command cd we will access it:

```sh
cd /var/www/
```

3. Once we are in the path /var/www/ we must download the latest version of WordPress. As my native language is Spanish I will select the latest version in Spanish. We will use the following command:

```sh
sudo wget https://es.wordpress.org/latest-es_ES.zip
```

{% hint style="warning" %}
I could be https://fr.wordpress.org/latest-fr\_FR.zip
{% endhint %}

4. Unzip the file you just downloaded with the command:

```sh
sudo unzip latest-en_US.zip
```

5. We will rename the folder html and call it html\_old:

```sh
sudo mv html/ html_old/
```

6. Now we will rename the wordpress folder and call it html:

```sh
sudo mv wordpress/ html
```

7. Finally we will set these permissions on the html folder. We will use the command `sudo chmod -R 755 html`. The number 7 indicates that the owner has read, write and execute permissions. The number 5 indicates that the group and others only have read and execute permissions.

```sh
sudo chmod -R 755 html
```

