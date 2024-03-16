# 🔑 password policy 🔑

1. First step will be editing the login.defs file:

```sh
nano /etc/login.defs
```

2. Once we are done editing the file, we will set the next parameters:

> PASS\_MAX\_DAYS 99999 -> PASS\_MAX\_DAYS 30

> PASS\_MIN\_DAYS 0 -> PASS\_MIN\_DAYS 2

<figure><img src="../.gitbook/assets/image (164).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
<mark style="color:green;">PASS\_MAX\_DAYS</mark>: It's the max days till password expiration.

<mark style="color:green;">PASS\_MIN\_DAYS</mark>: It's the min days till password change.

<mark style="color:green;">PASS\_WARN\_AGE</mark>: It's the days till password warning.
{% endhint %}

3. For continuing the installation we must install the next packages to enforce the password quality with the following command:

```sh
sudo apt install libpam-pwquality
```

then we wrute `Y` so we can continue; we wait till it finish.

<figure><img src="../.gitbook/assets/image (165).png" alt=""><figcaption></figcaption></figure>

4. Next thing we must do is is edit a file and change itś content. We will use

```sh
nano /etc/pam.d/common-password
```

<figure><img src="../.gitbook/assets/image (166).png" alt=""><figcaption></figcaption></figure>

5. Below **retry=3** we must add the following commands:

```
minlen=10 ucredit=-1 dcredit=-1 lcredit=-1 maxrepeat=3 reject_username difok=7 enforce_for_root
```

This is how the line must be↙️

<figure><img src="../.gitbook/assets/image (167).png" alt=""><figcaption></figcaption></figure>

This is how the file must look ↙️

<figure><img src="../.gitbook/assets/image (168).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
<mark style="color:green;">minlen=10</mark> ➤ The minimun characters a password must contain.

<mark style="color:green;">ucredit=-1</mark> ➤ The password at least have to contain a capital letter. We must write it with a - sign, as is how it knows that's refering to minumum caracters; if we put a + sign it will refer to maximum characters.

<mark style="color:green;">dcredit=-1</mark> ➤ The passworld at least have to containt a digit.

<mark style="color:green;">lcredit=-1</mark> ➤ The password at least have to contain a lowercase letter.

<mark style="color:green;">maxrepeat=3</mark> ➤ The password can not have the same character repited three contiusly times.

<mark style="color:green;">reject\_username</mark> ➤ The password can not contain the username inside itself.

<mark style="color:green;">difok=7</mark> ➤ The password it have to containt at least seven diferent characters from the last password ussed.

<mark style="color:green;">enforce\_for\_root</mark> ➤ We will implement this password policy to root.
{% endhint %}
