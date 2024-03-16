# 📰 WordPress configuration

1. Access the /var/www/html directory with the command:

```sh
cd /var/www/html
```

2. Copy the file wp-config-sample.php and rename it wp-config.php:

```sh
cp wp-config-sample.php wp-config.php
```

3. Once we have renamed it we will edit the file wp-config.php:

```sh
nano wp-config.php
```

4. modify the following values:

<figure><img src="../.gitbook/assets/image (180).png" alt=""><figcaption></figcaption></figure>

You have to replace them with the values that we have previously set when we created the database and the user so that WordPress can connect and make use of it.

<figure><img src="../.gitbook/assets/image (181).png" alt=""><figcaption></figcaption></figure>

5. We enabled the fastcgi-php module in Lighttpd to improve the performance and speed of web applications on the server:

```sh
sudo lighty-enable-mod fastcgi
```

6. We enabled the fastcgi-php module in Lighttpd to improve the performance and speed of PHP-based web applications on the server:

```sh
sudo lighty-enable-mod fastcgi-php
```

7. We update and apply the changes in the configuration with the command:

```sh
sudo service lighttpd force-reload
```

8. Once we have completed the previous steps we can go back to our browser and type `localhost`. You should see the following:

<figure><img src="../.gitbook/assets/image (182).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
If it don't work you can try http://localhost:81
{% endhint %}

9. We must fill in all the fields. In my case I have put the following:

<figure><img src="../.gitbook/assets/image (184).png" alt=""><figcaption></figcaption></figure>

10. Once we have filled in all the fields we must click on `Install WordPress` and we will have finished the installation. You will see the next tab. Now WordPress can create the tables and dump all the data it needs to work in the database we have assigned to it.

<figure><img src="../.gitbook/assets/image (185).png" alt=""><figcaption></figcaption></figure>

11. If we access again to our localhost from the browser we can see our functional page.

<figure><img src="../.gitbook/assets/image (186).png" alt=""><figcaption></figcaption></figure>

