# 💾 BONUS: file system of all logical volumes

1.  Now we can see how in the section where it shows us all our partitions and free space, all the logical partitions that we just created are already appearing. Good, we must configure all of them to select the file system that we want and the mount point indicated in the subject. Again we will go in order and select the first one that appears, which is `home`.

    <figure><img src="../../.gitbook/assets/image (102).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


2.  Show us the configuration of the partition. We must choose a file system as it currently does not have one.

    <figure><img src="../../.gitbook/assets/image (103).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


3.  Choose the Ext4 file system, it is the most commonly used file system in Linux distributions.

    <figure><img src="../../.gitbook/assets/image (104).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


4.  Now we need to select the mount point.

    <figure><img src="../../.gitbook/assets/image (105).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


5.  We select `home` as indicated in the subject.

    <figure><img src="../../.gitbook/assets/image (106).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


6.  Once we have selected it, we will finish the configuration of the partition.

    <figure><img src="../../.gitbook/assets/image (107).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


7.  Again, these steps can become very repetitive so I won't comment much. We repeat everything the same way (except for the mount point) for `root`.

    <figure><img src="../../.gitbook/assets/image (108).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


8.

    <figure><img src="../../.gitbook/assets/image (109).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


9.

    <figure><img src="../../.gitbook/assets/image (110).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


10.

    <figure><img src="../../.gitbook/assets/image (111).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


11.

    <figure><img src="../../.gitbook/assets/image (112).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


12. Repeat the process for `srv` and change the mount point.

    <figure><img src="../../.gitbook/assets/image (113).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


13.

    <figure><img src="../../.gitbook/assets/image (114).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


14.

    <figure><img src="../../.gitbook/assets/image (115).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


15.

    <figure><img src="../../.gitbook/assets/image (116).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


16.

    <figure><img src="../../.gitbook/assets/image (117).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


17.

    <figure><img src="../../.gitbook/assets/image (118).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


18. For `swap`, we will make an exception because the file system will be different. We select `swap`.

    <figure><img src="../../.gitbook/assets/image (119).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


19.

    <figure><img src="../../.gitbook/assets/image (120).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


20. Once the previous step is completed, we will finish the partition configuration.

    <figure><img src="../../.gitbook/assets/image (121).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


21.

    <figure><img src="../../.gitbook/assets/image (122).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


22. Now we will do the same thing as before, but now we will do it with `tmp` and changing the mount point.

    <figure><img src="../../.gitbook/assets/image (123).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


23.

    <figure><img src="../../.gitbook/assets/image (124).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


24.

    <figure><img src="../../.gitbook/assets/image (125).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


25.

    <figure><img src="../../.gitbook/assets/image (126).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


26.

    <figure><img src="../../.gitbook/assets/image (127).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


27. We repeat the process again for `var`, changing the mount point.

    <figure><img src="../../.gitbook/assets/image (128).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


28.

    <figure><img src="../../.gitbook/assets/image (129).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


29.

    <figure><img src="../../.gitbook/assets/image (130).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


30.

    <figure><img src="../../.gitbook/assets/image (131).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


31.

    <figure><img src="../../.gitbook/assets/image (132).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


32.

    <figure><img src="../../.gitbook/assets/image (133).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


33.

    <figure><img src="../../.gitbook/assets/image (134).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


34.

    <figure><img src="../../.gitbook/assets/image (135).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


35.

    <figure><img src="../../.gitbook/assets/image (136).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


36.

    <figure><img src="../../.gitbook/assets/image (138).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


37.

    <figure><img src="../../.gitbook/assets/image (139).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


38.

    <figure><img src="../../.gitbook/assets/image (140).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


39.

    <figure><img src="../../.gitbook/assets/image (141).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


40. Once we have completed all of the previous steps, we are almost finished. We must click 'finish partitioning' to save all of the changes to the disk.

    <figure><img src="../../.gitbook/assets/image (142).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>


41. We accept the message and the changes will be saved. Make sure that all of the partitions look the same as in the screenshot.

    <figure><img src="../../.gitbook/assets/image (143).png" alt="Partition disks configuration on Debian"><figcaption></figcaption></figure>

