# 👥 Creating a group

1. We will create a new group called `user42`. For that we must use:

```sh
sudo addgroup user42
```

It will show this:

<figure><img src="../../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
🧠 What is <mark style="color:green;">GID</mark>❓ It's the group identifier, in short, Group 🆔.
{% endhint %}

2. 🤔 Was the group created without problems? Truth is that there is no sign of one, still we can check it using with:

<pre class="language-sh"><code class="lang-sh"><strong>getent group &#x3C;groupname>
</strong></code></pre>

And see all groups and the users in any of them.
