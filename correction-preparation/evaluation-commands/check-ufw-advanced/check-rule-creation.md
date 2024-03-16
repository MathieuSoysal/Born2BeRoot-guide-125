# ✅ Check rule creation

18. Create a new rule for port 8080. Verify that it has been added to the active rules and then you can delete it.

```sh
sudo ufw allow 8080
```

<figure><img src="../../../.gitbook/assets/image (224).png" alt=""><figcaption></figcaption></figure>

```sh
sudo ufw status numbered
```

<figure><img src="../../../.gitbook/assets/image (225).png" alt=""><figcaption></figcaption></figure>

To delete the rule, we must use the command:

```sh
sudo ufw delete num_rule
```

We check that it has been deleted

```sh
sudo ufw status numbered
```

&#x20;and we see the number of the next rule that needs to be deleted..

<figure><img src="../../../.gitbook/assets/image (226).png" alt=""><figcaption></figcaption></figure>

Delete the new rule.

```sh
sudo ufw delete 5
```

We check that only the required rules in the subject remain:

```sh
sudo ufw status numbered
```
