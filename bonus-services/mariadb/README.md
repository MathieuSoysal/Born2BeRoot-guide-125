# 🐬 Mariadb

{% hint style="info" %}
<mark style="color:green;">MariaDB</mark>: It is a database. It is used for various purposes, such as data warehousing, e-commerce, enterprise-level functions, and logging applications.
{% endhint %}

1. We will install the packages with the command:

```sh
sudo apt install mariadb-server
```

2. Because the default configuration leaves your MariaDB installation unsecure, we will use a script provided by the mariadb-server package to restrict access to the server and remove unused accounts. We will run the script with the following command:

```sh
sudo mysql_secure_installation
```

It will ask if we want to switch to Unix socket authentication. Since we already have a protected root account we will type `N`.

> Switch to unix\_socket autentication? → N \
> Change the root password? → N\
> Remove anonymous users? → Y \
> Disallow root login remotely? → Y \
> Remove test database and access to it? → Y \
> Reload privilege tables now? → Y

<details>

<summary>Explanation</summary>

Switch to unix\_socket authentication? We choose `N` because we don't want it to switch to Unix socket authentication because we already have a protected root account.

Change the root password? We choose `N`. We do not want to change the root password. By default we have no password but in mariadb he is not really root as we must give him administrator permissions.

Remove anonymous users? We choose `Y`. By default when you install mariadb it has an anonymous user, which allows anyone to log into mariadb without having to create their own user account. This is designed for testing purposes and to make the installation smoother. When we leave the development environment and want to move to a production environment we must remove the anonymous users.

Disallow root login remotely? Choose `Y`. Disabling root login remotely will prevent anyone from guessing the root password. We will only be able to connect to root from localhost.

Remove test database and access to it? Choose `Y`. This will remove the test database and any users who have access to it.

Reaload privilege tables now? Choose `Y`. This will reload the MySQL permission tables so that the changes to the security settings will take effect immediately.

</details>

