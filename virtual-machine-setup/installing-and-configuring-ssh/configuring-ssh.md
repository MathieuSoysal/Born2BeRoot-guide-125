# 📶 Configuring SSH

Going on, some files have been created and we need to configure them.

For that we will use [Nano](https://en.wikipedia.org/wiki/GNU\_Nano) or [VIM](https://en.wikipedia.org/wiki/Vim\_\(text\_editor\)) (we will need to install vim since it's not preinstalled using `sudo apt install vim`) or any other text editor.

1. First file that we will edit will be `/etc/ssh/sshd_config`. If you are not on root you will not be able to edit the file; as you know, for switching to root we use `su`

```sh
su
nano /etc/ssh/sshd_config
```

2. The `#` means that line it is commented; the lines that we will be edit have to be uncommented. Once we are editing the file we need to update the following lines:

> \#Port 22 -> Port 4242

<figure><img src="../../.gitbook/assets/image (152).png" alt=""><figcaption></figcaption></figure>

> \#PermitRootLogin prohibit-password -> PermitRootLogin no

<figure><img src="../../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>

When finish we have to save the changes and leave the file.

3. Now with the file `/etc/ssh/ssh_config`. (not `sshd_config`)

```sh
nano /etc/ssh/ssh_config
```

> \#Port 22 -> Port 4242

<figure><img src="../../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>



4. Finally we must restart the ssh service so it can be updated. For that purpuse we will use:

```sh
sudo service ssh restart
```

and once it is done we will check the service state with:

```sh
sudo service ssh status
```

and confirm that everything is alright.

![](<../../.gitbook/assets/image (155).png>)\
