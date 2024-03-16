# 💡 Lighttpd

{% hint style="info" %}
<mark style="color:green;">Lighttpd</mark>: is a web server designed to be fast, secure, flexible, and standards-compliant. It is optimized for environments where speed is a top priority because it consumes less CPU and RAM than other servers.
{% endhint %}

1. Installation of Lighttpd packages.

```sh
sudo apt install lighttpd
```

<figure><img src="../.gitbook/assets/image (176).png" alt=""><figcaption></figcaption></figure>

2. We allow connections through port 80 with the command:

```sh
sudo ufw allow 80
```

3. We check that we have actually allowed it. Port 80 and allow should appear:

```sh
sudo ufw status
```

4. We add the rule that includes port 80. If you don't remember how to add rules in port forwarding. Machine configuration → Network → Port forwarding → Replicate the capture

<figure><img src="../.gitbook/assets/image (179).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
It could be nice if the port are not equals like 81 : 80
{% endhint %}

