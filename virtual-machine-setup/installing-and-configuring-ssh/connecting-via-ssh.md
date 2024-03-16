# 👬 Connecting via SSH

1. If we want to connect via SSH we must close the machine and go to settings.

<figure><img src="../../.gitbook/assets/image (169).png" alt=""><figcaption></figcaption></figure>

2. Once there we will click on `Network`, click on `Advanced` so it shows more options, then we click on `Port fowarding`.

<figure><img src="../../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

3. Click on the emoji for adding a new rule.

<figure><img src="../../.gitbook/assets/image (171).png" alt=""><figcaption></figcaption></figure>

4. Lastly we will add the `4242` port to host and client. The IP's are not required. We will click accept so changes can be saved.

<figure><img src="../../.gitbook/assets/image (172).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Sometimes its could happen a connection issue if the ports are same. it could be nice if is like 4241 : 4242
{% endhint %}

5. To connect via ssh **from our machine** to the virstual machine using and the use the command

```sh
ssh <user>@localhost -p 4241
```

It will ask for the **password of the user** that we are trying to log in. Once the password is introduced it will show or login in green, that will mean that the connections has been successfully.
