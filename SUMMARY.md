# Table of contents

* [📘 Born2BeRoot](README.md)

## 🛠️ Installing the virtual machine

* [💿 Virtual machine ISO](installing-the-virtual-machine/virtual-machine-iso.md)
* [🖥️ VirtualBox](installing-the-virtual-machine/virtualbox.md)
* [💿 Attaching ISO to VirtualBox](installing-the-virtual-machine/attaching-iso-to-virtualbox.md)

## 🌀 Installing Debian

* [🌍 Configure locals](installing-debian/configure-locals.md)
* [📶 Configure the network](installing-debian/configure-the-network.md)
* [🔐 Set up users and passwords](installing-debian/set-up-users-and-passwords.md)
* [🕚 Configure the clock](installing-debian/configure-the-clock.md)
* [💾 non-BONUS: Partition disks](installing-debian/non-bonus-partition-disks.md)
* [💾 BONUS: Partition Disks](installing-debian/bonus-partition-disks/README.md)
  * [💾 BONUS: primary partition](installing-debian/bonus-partition-disks/bonus-primary-partition.md)
  * [💾 BONUS: logical partition](installing-debian/bonus-partition-disks/bonus-logical-partition.md)
  * [💾 BONUS: encrypt logical partition](installing-debian/bonus-partition-disks/bonus-encrypt-logical-partition.md)
  * [💾 BONUS: logical volume manager](installing-debian/bonus-partition-disks/bonus-logical-volume-manager.md)
  * [💾 BONUS: logical volume group](installing-debian/bonus-partition-disks/bonus-logical-volume-group.md)
  * [💾 BONUS: logical volume root](installing-debian/bonus-partition-disks/bonus-logical-volume-root.md)
  * [💾 BONUS: logical volume swap](installing-debian/bonus-partition-disks/bonus-logical-volume-swap.md)
  * [💾 BONUS: logical volume home](installing-debian/bonus-partition-disks/bonus-logical-volume-home.md)
  * [💾 BONUS: logical volume var](installing-debian/bonus-partition-disks/bonus-logical-volume-var.md)
  * [💾 BONUS: logical volume srv](installing-debian/bonus-partition-disks/bonus-logical-volume-srv.md)
  * [💾 BONUS: logical volume tmp](installing-debian/bonus-partition-disks/bonus-logical-volume-tmp.md)
  * [💾 BONUS: logical volume var-log](installing-debian/bonus-partition-disks/bonus-logical-volume-var-log.md)
  * [💾 BONUS: file system of all logical volumes](installing-debian/bonus-partition-disks/bonus-file-system-of-all-logical-volumes.md)
* [📦 Configure the package manager](installing-debian/configure-the-package-manager.md)
* [🖥️ Install the GRUB boot loader](installing-debian/install-the-grub-boot-loader.md)
* [🎉 Finish installation](installing-debian/finish-installation.md)

## ⚙️ Virtual machine setup

* [⚙️ First connection](virtual-machine-setup/first-connection.md)
* [👤 Installing sudo & configuration of user and groups](virtual-machine-setup/installing-sudo-and-configuration-of-user-and-groups/README.md)
  * [👤 Creating a user](virtual-machine-setup/installing-sudo-and-configuration-of-user-and-groups/creating-a-user.md)
  * [👥 Creating a group](virtual-machine-setup/installing-sudo-and-configuration-of-user-and-groups/creating-a-group.md)
  * [🫂 Adding a user to a group](virtual-machine-setup/installing-sudo-and-configuration-of-user-and-groups/adding-a-user-to-a-group.md)
* [📶 Installing & configuring SSH](virtual-machine-setup/installing-and-configuring-ssh/README.md)
  * [📶 Configuring SSH](virtual-machine-setup/installing-and-configuring-ssh/configuring-ssh.md)
  * [👬 Connecting via SSH](virtual-machine-setup/installing-and-configuring-ssh/connecting-via-ssh.md)
* [🔥 Installing & configuring UFW 🔥🧱 Firewall](virtual-machine-setup/installing-and-configuring-ufw-firewall/README.md)
  * [🔥 Allow a port to firewall](virtual-machine-setup/installing-and-configuring-ufw-firewall/allow-a-port-to-firewall.md)
* [🔐 sudo policies](virtual-machine-setup/sudo-policies.md)
* [🔑 password policy 🔑](virtual-machine-setup/password-policy.md)
* [🧾 Script 🚨](virtual-machine-setup/script.md)
* [⏰ Crontab](virtual-machine-setup/crontab.md)
* [✒️ Signature.txt](virtual-machine-setup/signature.txt.md)

## 😊 BONUS Services&#x20;

* [💡 Lighttpd](bonus-services/lighttpd.md)
* [📰 WordPress](bonus-services/wordpress.md)
* [🐬 Mariadb](bonus-services/mariadb/README.md)
  * [🐬 Create database on Mariadb](bonus-services/mariadb/create-database-on-mariadb.md)
* [🐘 PHP](bonus-services/php.md)
* [📰 WordPress configuration](bonus-services/wordpress-configuration.md)
* [⚡ LiteSpeed](bonus-services/litespeed.md)

## ✅ Correction preparation

* [✅ Correction sheet](correction-preparation/correction-sheet.md)
* [❤️‍🩹 Evaluation answer](correction-preparation/evaluation-answer.md)
* [⌨️ Evaluation commands](correction-preparation/evaluation-commands/README.md)
  * [✅ Check no graphical interface](correction-preparation/evaluation-commands/check-no-graphical-interface.md)
  * [✅ Check UFW](correction-preparation/evaluation-commands/check-ufw.md)
  * [✅ Check SSH service](correction-preparation/evaluation-commands/check-ssh-service.md)
  * [✅ Check OS](correction-preparation/evaluation-commands/check-os.md)
  * [✅ Check user and group](correction-preparation/evaluation-commands/check-user-and-group/README.md)
    * [✅ Add user and check password policy](correction-preparation/evaluation-commands/check-user-and-group/add-user-and-check-password-policy.md)
    * [✅ Check group creation](correction-preparation/evaluation-commands/check-user-and-group/check-group-creation.md)
    * [✅ Check adding to group](correction-preparation/evaluation-commands/check-user-and-group/check-adding-to-group.md)
  * [✅ Check hostname](correction-preparation/evaluation-commands/check-hostname/README.md)
    * [✅ Check change hostname](correction-preparation/evaluation-commands/check-hostname/check-change-hostname.md)
  * [✅ Check all partitions](correction-preparation/evaluation-commands/check-all-partitions.md)
  * [✅ Check sudo](correction-preparation/evaluation-commands/check-sudo/README.md)
    * [✅ Check add user to sudo group](correction-preparation/evaluation-commands/check-sudo/check-add-user-to-sudo-group.md)
    * [✅ Check sudo rules](correction-preparation/evaluation-commands/check-sudo/check-sudo-rules.md)
    * [✅ Check sudo logs](correction-preparation/evaluation-commands/check-sudo/check-sudo-logs.md)
  * [✅ Check UFW advanced](correction-preparation/evaluation-commands/check-ufw-advanced/README.md)
    * [✅ Check UFW active rules](correction-preparation/evaluation-commands/check-ufw-advanced/check-ufw-active-rules.md)
    * [✅ Check rule creation](correction-preparation/evaluation-commands/check-ufw-advanced/check-rule-creation.md)
  * [✅ Check SSH advanced](correction-preparation/evaluation-commands/check-ssh-advanced/README.md)
    * [✅ Check SSH usage](correction-preparation/evaluation-commands/check-ssh-advanced/check-ssh-usage.md)
  * [✅ Check crontab of script](correction-preparation/evaluation-commands/check-crontab-of-script.md)
  * [🎉 Finish !](correction-preparation/evaluation-commands/finish.md)