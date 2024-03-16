# 🔥 Allow a port to firewall

1. we must allow our firewall to accept the connections that will happens in the 4242 port. What we will do is use:

```sh
sudo ufw allow 4242
```

<figure><img src="../../.gitbook/assets/image (158).png" alt=""><figcaption></figcaption></figure>

2. Lastly we will check if everything done here is correct checking the actual state of our firewall. For that we will use:

```sh
sudo ufw status
```

<figure><img src="../../.gitbook/assets/image (159).png" alt=""><figcaption></figcaption></figure>
