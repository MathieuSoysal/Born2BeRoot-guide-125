# ✒️ Signature.txt

To obtain the signature, the first thing we must do is shut down the virtual machine, since once you turn it on or modify something, the signature will change.

{% hint style="warning" %}
Since once you turn it on or modify something, the signature will change.
{% endhint %}

1. The next step will be to locate ourselves in the path where we have the .vdi of our virtual machine. From our physical machine.

<figure><img src="../.gitbook/assets/image (175).png" alt=""><figcaption></figcaption></figure>

We had choose the path [here](../installing-the-virtual-machine/virtualbox.md)

2. Finally, we will run `shasum machinename.vdi` and this will give us the signature. The result of this signature is what we will need to add to our signature.txt file and subsequently upload the file to the intra repository. It is very important not to reopen the machine since the signature will be modified. For corrections, remember to clone the machine so you can turn it on without fear of changing the signature.

```sh
shasum machinename.vdi
```

{% hint style="info" %}
<mark style="color:green;">shasum</mark>: It is a command that allows you to identify the integrity of a file using the SHA-1 hash check sum of a file.
{% endhint %}

{% hint style="danger" %}
It is very important not to reopen the machine since the signature will be modified. For corrections, remember to clone the machine so you can turn it on without fear of changing the signature.
{% endhint %}
