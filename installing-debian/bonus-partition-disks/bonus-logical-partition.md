# 💾 BONUS: logical partition

{% hint style="info" %}
**Logical partition**: It occupies a portion of the primary/extended partition or the whole of it, which has been formatted with a specific type of file system (in our case we will use ext4) and has been assigned a unit, so the operating system recognizes the logical partitions or its file system. There can be a maximum of 23 logical partitions in an extended partition, however, Linux, the OS we are currently working with, reduces it to 15, more than enough for this project.
{% endhint %}

We will start creating this:

<figure><img src="../../.gitbook/assets/image (231).png" alt=""><figcaption></figcaption></figure>

1.  Once we have completed the previous step, the partition should already appear. Now we must create a logical partition with all the available space on the disk, which has no mount point and is encrypted. To do this, we select the free space where we want to create it.

    <figure><img src="../../.gitbook/assets/image (230).png" alt=""><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


2.  We create a new partition.

    <figure><img src="../../.gitbook/assets/image (232).png" alt=""><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


3.  We select the maximum size.

    <figure><img src="../../.gitbook/assets/image (233).png" alt=""><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


4.  We select the type of partition, in this case logical.

    <figure><img src="../../.gitbook/assets/image (234).png" alt=""><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


5.  We will modify the mount point.

    <figure><img src="../../.gitbook/assets/image (235).png" alt=""><figcaption><p>Partition disks configuration on Debian</p></figcaption></figure>


6.  We will choose the option not to mount it.

    <figure><img src="../../.gitbook/assets/image (236).png" alt=""><figcaption><p>Partition disks configuration on Debian</p></figcaption></figure>


7.  We finish configuring the current partition.

    <figure><img src="../../.gitbook/assets/image (237).png" alt=""><figcaption><p>Partition disks configuration on Debian</p></figcaption></figure>


8.  We accept the confirmation message.

    <figure><img src="../../.gitbook/assets/image (239).png" alt=""><figcaption><p>Partition disks configuration on Debian</p></figcaption></figure>


9.  We create the encrypted volumes.

    <figure><img src="../../.gitbook/assets/image (240).png" alt=""><figcaption><p>Partition disks configuration on Debian</p></figcaption></figure>


10. We select which partition we want to encrypt.

    <figure><img src="../../.gitbook/assets/image (241).png" alt=""><figcaption><p>Partition disks configuration on Debian</p></figcaption></figure>


11. We finish configuring the current partition.

    <figure><img src="../../.gitbook/assets/image (242).png" alt=""><figcaption><p>Partition disks configuration on Debian</p></figcaption></figure>


12.
