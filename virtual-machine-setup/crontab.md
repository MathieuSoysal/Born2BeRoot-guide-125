# ⏰ Crontab

{% hint style="info" %}
<mark style="color:green;">crontab</mark>: is a background process manager. The specified processes will be executed at the time you specify in the crontab file.
{% endhint %}

1. To properly configure crontab, we must edit the crontab file with the following command:

```sh
sudo crontab -u root -e
```

2. In the file, we must add the following command for the script to execute every 10 minutes `*/10 * * * * sh /path_to_file.sh`.

<figure><img src="../.gitbook/assets/image (174).png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
To well know how crontab works you can go to this site: [https://crontab.guru/](https://crontab.guru/)
{% endhint %}

{% embed url="https://crontab.guru/" %}
To improve your crontab skills
{% endembed %}
