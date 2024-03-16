# 💾 BONUS: primary partition

{% hint style="info" %}
**Primary partition**: The only partition on which an OS can be installed. There can only be 4 primary partitions per hard drive or 3 primary and one extended.
{% endhint %}

{% hint style="info" %}
**Secondary/Extended partition**: It was designed to break the 4 primary partition limitation on a single physical disk. There can only be one partition of this type per disk, and it only serves to contain logical partitions.
{% endhint %}

We will start by creating this:

<figure><img src="../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

1.  We will create a new partition.

    <figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


2.  As the subject indicates, the size of the partition must be 500 megabytes.

    <figure><img src="../../.gitbook/assets/image (65).png" alt=""><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


3.  We choose the type of partition. We choose primary because it will be the partition where the Operating System will be installed.

    <figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


4.  We will select beginning because we want the new partition to be created at the beginning of the available space.

    <figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


5.  In the following screenshot it shows the details of the partition. We will modify the mount point as specified in the subject.

    <figure><img src="../../.gitbook/assets/image (68).png" alt=""><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


6.  We choose boot as the mount point for our partition.

    <figure><img src="../../.gitbook/assets/image (69).png" alt=""><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>


7.  We finish configuring the current partition.

    <figure><img src="../../.gitbook/assets/image (70).png" alt=""><figcaption><p>Partitions disk configuration on Debian</p></figcaption></figure>



