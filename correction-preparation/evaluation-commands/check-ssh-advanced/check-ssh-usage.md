# ✅ Check SSH usage

20. &#x20;Use ssh to log in with the newly created user. Make sure that you cannot use ssh with the root user.

We try to connect over ssh with the root user but we do not have permission.

```sh
ssh root@localhost -p 4241
```

We connect via ssh with the new user using the command:

```sh
ssh newuser@localhost -p 4241
```
