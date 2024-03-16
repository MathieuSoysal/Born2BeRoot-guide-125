# 🧾 Script 🚨

Going into this part, you need to take special attention to everything, as is important to learn all that is here.&#x20;

{% hint style="danger" %}
**Do not cheat this part!** You will be asked how the script works during the evaluation, or as the evaluator sees.
{% endhint %}

{% hint style="info" %}
<mark style="color:green;">script</mark>:  is a sequence of commands stored in a file that when executed will do the function of each command.
{% endhint %}

## Architecture

For the architecture of the SO to be shown, you will use the command `uname -a` ("-a" == "--all"). What this command does is print all information, except if the CPU is unknow or the platform hardware.

{% hint style="info" %}
`uname -a` to get `CPU architecture`
{% endhint %}

## Physical Cores

For the number of fisical cores to be shown we will use the file /proc/cpuinfo, which give us information about the CPU: its type, brand, model, performance, etc. We will use `grep "physical id" /proc/cpuinfo | wc -l` with the command grep looking inside the file "physical id" and with wc -l to count the line of the grep output.

{% hint style="info" %}
`grep "physical id" /proc/cpuinfo | wc -l` to get number of physical cores
{% endhint %}

## Virtual Cores

To show the number of virtual cores is very similar to the previous one. We will again use the file /proc/cpuinfo, but in this case we will use the command `grep processor /proc/cpuinfo | wc -l`. The usage is practically the same as before, only that instead of counting the lines of "physical id" we will do it with "processor". We do it this way for the same reason as before, the way of quantifying marks 0 if there is a processor.

{% hint style="info" %}
`grep processor /proc/cpuinfo | wc -l` to get number of virtual cores
{% endhint %}

## RAM

To show the RAM memory we will use the command `free` to see at the moment information about the RAM, the used part, free, reserved for other resources, etc. For more info about the command we will put free --help. We will use free --mega since that unit of measure appears in the subject.

<figure><img src="../.gitbook/assets/image (229).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
`free --mega | awk '$1 == "Mem:" {print $3}'` to get number mb of used memoir&#x20;
{% endhint %}

{% hint style="info" %}
`free --mega | awk '$1 == "Mem:" {print $2}'` to get number of total mb memoire
{% endhint %}

{% hint style="info" %}
`free --mega | awk '$1 == "Mem:" {printf("(%.2f%%)\n", $3/$2*100)}'` to get pourcent of used memory
{% endhint %}

## Disk memory

To view the occupied and available memory of the disk, we will use the `df` command, which stands for "disk filesystem", it is used to get a complete summary of the use of disk space. As indicated in the subject, the used memory is shown in MB, so we will then use the -m flag. Next, we will do a grep to only show us the lines that contain "/dev/" and then we will do another grep with the -v flag to exclude lines that contain "/boot". Finally, we will use the awk command and sum the value of the third word of each line to once all the lines are summed, print the final result of the sum. The entire command is as follows: `df -m | grep "/dev/" | grep -v "/boot" | awk '{memory_use += $3} END {print memory_use}'`.

{% hint style="info" %}
`df -m | grep "/dev/" | grep -v "/boot" | awk '{use += $3} {total += $2} END {printf("(%d%%)\n"), use/total*100}'` to get number of occuped disk memory
{% endhint %}

## CPU usage percentage

To view the percentage of CPU usage, we will use the `vmstat` command, which shows system statistics, allowing us to obtain a general detail of the processes, memory usage, CPU activity, system status, etc. We could put no option but in my case I will put an interval of seconds from 1 to 4. We will also use the `tail -1` command, which will allow us to produce the output only on the last line, so of the 4 generated, only the last one will be printed. Finally, we will only print word 15, which is the available memory usage. The entire command is as follows: `vmstat 1 4 | tail -1 | awk '{print $15}'`. The result of this command is only part of the final result since there is still some operation to be done in the script for it to be correct. What should be done is to subtract the amount returned by our command from 100, the result of this operation will be printed with one decimal and a % at the end and the operation would be finished.

{% hint style="info" %}
`vmstat 1 4 | tail -1 | awk '{print $15}'` to get cpu usage.
{% endhint %}

## Last reboot

To see the date and time of our last restart, we will use the `who` command with the `-b` flag, as this flag will display the time of the last system boot on the screen. As has happened to us before, it shows us more information than we want, so we will filter it and only show what we are interested in, for this we will use the awk command and compare if the first word of a line is "system", the third word of that line will be printed on the screen, a space, and the fourth word. The entire command would be as follows: `who -b | awk '$1 == "system" {print $3 " " $4}'`.

{% hint style="info" %}
`who -b | awk '$1 == "system" {print $3 " " $4}'` to get date and time of last reboot.
{% endhint %}

## LVM active

To check if LVM is active or not, we will use the `lsblk` command, which shows us information about all block devices (hard drives, SSDs, memories, etc) among all the information it provides, we can see lvm in the type of manager. For this command we will do an if because we will print Yes or No. Basically, the condition we are looking for will be to count the number of lines in which "lvm" appears and if there are more than 0 we will print Yes, if there are 0 we will print No. The entire command would be: `if [ $(lsblk | grep "lvm" | wc -l) -gt 0 ]; then echo yes; else echo no; fi`.

{% hint style="info" %}
`if [ $(lsblk | grep "lvm" | wc -l) -gt 0 ]; then echo yes; else echo no; fi` to know if LVM is active or not.
{% endhint %}

## TCP connections

To check the number of established TCP connections, we will use the `ss` command replacing the now obsolete netstat. We will filter with the `-ta` flag so that only TCP connections are shown. Finally, we will do a grep to see those that are established as there are also only listening and close with wc -l to count the number of lines. The command is as follows: `ss -ta | grep ESTAB | wc -l`.

{% hint style="info" %}
`ss -ta | grep ESTAB | wc -l` to get number of tcp connections
{% endhint %}

## Number of users

We will use the `users` command which will show us the names of the users there are, knowing this, we will put `wc -w` to count the number of words in the command output. The entire command is as follows: `users | wc -w`.

{% hint style="info" %}
`users | wc -w` to get number of users&#x20;
{% endhint %}

## IP adress & MAC

To obtain the host address, we will use the `hostname -I` command and to obtain the MAC, we will use the `ip link` command which is used to show or modify the network interfaces. As more than one interface, IP's etc. appear, we will use the grep command to search for what we want and thus be able to print only what is requested. To do this, we will put `ip link | grep "link/ether" | awk '{print $2}'` and in this way we will only print the MAC.

{% hint style="info" %}
`ip link | grep "link/ether" | awk '{print $2}'` to get addressemac
{% endhint %}

## Number of commands executed with sudo

To obtain the number of commands executed with sudo, we will use the `journaclctl` command, which is a tool that is responsible for collecting and managing the system logs. Next, we will put `_COMM=sudo` in order to filter the entries by specifying its path. In our case we put `_COMM` because it refers to an executable script. Once we have filtered the search and only the sudo logs appear, we still need to filter a bit more as when you start or close the root session it also appears in the log, so to finish filtering we will put a `grep COMMAND` and this will only show the command lines. Finally, we will put `wc -l` so that the lines are numbered. The entire command is as follows: `journalctl _COMM=sudo | grep COMMAND | wc -l)`. To check that it works correctly, we can run the command in the terminal, put a command that includes sudo and run the command again and it should increase the number of sudo executions.

{% hint style="info" %}
`journalctl _COMM=sudo | grep COMMAND | wc -l` to get number of executed command
{% endhint %}

## Total result of the script

{% hint style="danger" %}
⚠️ Remember not to copy and paste if you do not know the function of each command. ⚠️
{% endhint %}

```sh
#!/bin/bash

# ARCH
arch=$(uname -a)

# CPU PHYSICAL
cpuf=$(grep "physical id" /proc/cpuinfo | wc -l)

# CPU VIRTUAL
cpuv=$(grep "processor" /proc/cpuinfo | wc -l)

# RAM
ram_total=$(free --mega | awk '$1 == "Mem:" {print $2}')
ram_use=$(free --mega | awk '$1 == "Mem:" {print $3}')
ram_percent=$(free --mega | awk '$1 == "Mem:" {printf("%.2f"), $3/$2*100}')

# DISK
disk_total=$(df -m | grep "/dev/" | grep -v "/boot" | awk '{disk_t += $2} END {printf ("%.1fGb\n"), disk_t/1024}')
disk_use=$(df -m | grep "/dev/" | grep -v "/boot" | awk '{disk_u += $3} END {print disk_u}')
disk_percent=$(df -m | grep "/dev/" | grep -v "/boot" | awk '{disk_u += $3} {disk_t+= $2} END {printf("%d"), disk_u/disk_t*100}')

# CPU LOAD
cpul=$(vmstat 1 2 | tail -1 | awk '{printf $15}')
cpu_op=$(expr 100 - $cpul)
cpu_fin=$(printf "%.1f" $cpu_op)

# LAST BOOT
lb=$(who -b | awk '$1 == "system" {print $3 " " $4}')

# LVM USE
lvmu=$(if [ $(lsblk | grep "lvm" | wc -l) -gt 0 ]; then echo yes; else echo no; fi)

# TCP CONNEXIONS
tcpc=$(ss -ta | grep ESTAB | wc -l)

# USER LOG
ulog=$(users | wc -w)

# NETWORK
ip=$(hostname -I)
mac=$(ip link | grep "link/ether" | awk '{print $2}')

# SUDO
cmnd=$(journalctl _COMM=sudo | grep COMMAND | wc -l)

wall "	Architecture: $arch
	CPU physical: $cpuf
	vCPU: $cpuv
	Memory Usage: $ram_use/${ram_total}MB ($ram_percent%)
	Disk Usage: $disk_use/${disk_total} ($disk_percent%)
	CPU load: $cpu_fin%
	Last boot: $lb
	LVM use: $lvmu
	Connections TCP: $tcpc ESTABLISHED
	User log: $ulog
	Network: IP $ip ($mac)
	Sudo: $cmnd cmd"
```

### Result after executing the script ↙️

<figure><img src="../.gitbook/assets/image (173).png" alt=""><figcaption></figcaption></figure>

