# 🫂 Adding a user to a group

1. With `adduser` we can add user to a group like this:

```sh
sudo adduser <user> <groupname>
```

We can include a user to a group. We must include out user in the groups `sudo` and `user42` in my case:

```sh
sudo gemartin user42
```

```sh
sudo gemartin sudo
```

2. Once we are done with that we can check it using `getent group <groupname>`  ; the groups `sudo` and `user42` must be present with our user:

```sh
getent group sudo user42
```

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>
