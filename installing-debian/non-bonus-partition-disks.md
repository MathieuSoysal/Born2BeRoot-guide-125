# 💾 non-BONUS: Partition disks

{% hint style="warning" %}
**If you want to do the bonus click on BONUS: Partition Disks**
{% endhint %}

{% content-ref url="bonus-partition-disks/" %}
[bonus-partition-disks](bonus-partition-disks/)
{% endcontent-ref %}

1.  Select `Guided - use entire disk and set up encrypted LVM`. ⚠️❗️ **If you want to do the bonus select `Manual` and then** [**click here**](bonus-partition-disks/)❗️⚠️

    <figure><img src="../.gitbook/assets/image (44).png" alt="Partitions disk configuration on Debian"><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


2.  We choose the disk which we wish to create the partition (it only have to show one disk).

    <figure><img src="../.gitbook/assets/image (45).png" alt="Partitions disk configuration on Debian"><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


3.  Once we choosed the disk we must make the partition as is in the subject. To do it properly we select the second option `Separate /home partition`.

    <figure><img src="../.gitbook/assets/image (46).png" alt="Partitions disk configuration on Debian"><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


4.  We choose option `Yes` so the changes will be writen in the disk and so we can set the logical volume manager (LVM).

    <figure><img src="../.gitbook/assets/image (47).png" alt="Partitions disk configuration on Debian"><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


5.  We click on `Cancel`; the erasing of the data is not required.

    <figure><img src="../.gitbook/assets/image (48).png" alt="Partitions disk configuration on Debian"><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


6.  Again, we must choose desired password for the LVM encrypt. As is mention before we must repite the process and I advice you to write it down.

    <figure><img src="../.gitbook/assets/image (49).png" alt="Partitions disk configuration on Debian"><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


7.  In this step we must input the required amount of volume group to use during the guided partitioning. We can write down `max` or the total avalaible memory, in this case being `12.4 GB`.

    <figure><img src="../.gitbook/assets/image (50).png" alt="Partitions disk configuration on Debian"><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


8.  To wrap the partitioning and write the changes in the disk we choose the option `Finish partitioning and write changes to disk`.

    <figure><img src="../.gitbook/assets/image (51).png" alt="Partitions disk configuration on Debian"><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


9.  We choose the option `Yes` and then we confirm that we do not want more changes.

    <figure><img src="../.gitbook/assets/image (52).png" alt="Partitions disk configuration on Debian"><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>



If your are not doing the bonus click on **Configure the package manager**

{% content-ref url="configure-the-package-manager.md" %}
[configure-the-package-manager.md](configure-the-package-manager.md)
{% endcontent-ref %}

