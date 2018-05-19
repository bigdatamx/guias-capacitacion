---
title: Hard Drives
---
## Hard Drives

Hard drives are permenant storages for computers. There are several types of hard drives, traditional magnetic disks, new generation solid state disks or hybrid disks which contains both SSD and magnetic storage.

Traditional hard disk uses magnetic needles and rotating magnetized platters to store data. Because of these moving parts, hard drives are easily damaged by drops or shocks. The motor that rotates the platters also consumes a lot of power, but no other storage method is as affordable for large volumes of storage.

Hard drives come in various sizes, some up to even 10TB (10 trillion bytes). Typical computers come with between 256GB (256 billion bytes) to 1TB. Laptops usually use Solid State Drives (SSDs) because they are faster, lighter, more power efficient, and contain no moving parts, making them less likely to fail due to impact. For the same amount of storage, SSDs are generally more expensive than hard drives.

Magnetic heads are responsible for reading and writing data, which is physically stored on a set of magnetically coated discs stacked above one another referred to as a platter. The heads are located at the end of an armature. The interior discs of the platter have two heads on a single arm. This allows data to be accessed from both the disc beneath and above the arm. The top and bottom discs of the platter only have one head at the end of an arm. On the opposite end of the end on the arm is an actuator. It provides the movement of the arm to travel from the center of the platter called the spindle to the outermost regions of the platter. The amount of time it takes to place the head in the correct concentric location is referred to as the seek time. Once the head is in the correct concentric spatial location more time is spent waiting for the disc to rotate such that the sector with the requested data is beneath the head.  This amount of time is referred to as latency.   

The heads are positioned only a few nanometers away from the rotating discs. The heads are said to "fly" above the platter and as such the distance between head and platter is referred to as the 'flying height'.  The heads are designed to never touch the locations of the platters that store data and are magnetically coated. Should the head 'touch down' on a platter, both the head and sectors of the platters may be destroyed resulting in data loss (hence the phrase "a hard drive crash" or "head crash").

Hard drives retrieve and store data from program applications at the request of the CPU. This is referred to as input/output operations or IO for short. When a running program requires a certain piece of data, the CPU dispatches an instruction for the data to be fetched from the hard drive.  Reading this piece of data is an input operation (from the CPU's perspective).  The program may then perform a computation on the data, resulting in it being changed and the results need to be stored back out to the hard drive. The CPU requests the data be written back out to the drive.  This would be an example of an output operation (again, from the CPU's perspective). 

Hard drive performance is measured primarily by two key metrics 1) response time, which is how long it takes a read or write operation to complete and 2) IOPS which is an acronym for 'Input / Output Operations per Second'.  As the name would suggest, IOPS is a measurement of the maximum IO operations in one second.  The primary factor in achieving maximum IOPS at the lowest response time is the hard drive's rotational speed measured in revolutions per minute (RPM). Common rotational speeds are 5,400 RPM, 7,200 RPM, 10,000 RPM and 15,000 RPM (commonly notated as 5.4K, 7.2K, 10K and 15K). Hard drives with higher rotational rates RPM's) will have more platter real estate pass beneath the heads for IO operations (reads and writes).  Hard drives with lower RPM rotational rates will have much higher mechanical latencies, as less real estate passes beneath the heads.

Hard drives tend to be categorized by use case (capacity or performance). Home PC's and general use office workstations tend to use slower rotating hard drives (5.4K and 7.2K) which is fine for storing pictures and office files.  However large databases that support online banking transactions for instance, use the faster 10K and 15K RPM hard drives as they'll be components in an enterprise server or storage array. There's a tradeoff between a hard drive's performance and capacity.  For instance, the largest capacity 15K hard drive available today is only 600 GB, whereas the largest capacity hard drive for the both 5.4K and 7.2K RPM is 10 TB. The 600 GB 15K drive is capable of 250 IOPS @ 3 ms response time (averages).  Whereas the 10 TB 7.2K TB drive does not measure IOPS at a given response time, as it's not optimized nor intended for IOPS centric performance use cases. There are also other tradeoffs in price per GB, energy consumed and physical size (2.5" vs 3.5" inches).

Computers store data and files on hard drives for later use. Because hard drives have moving parts, it takes much longer to read a file from a hard drive than from RAM or cache memory on the CPU.  You can think of a hard drive as a filing cabinet: a place to store things that we aren't using right now, but need later. You don't have enough room on your desk for all your papers, so you store things you aren't using right now in the filing cabinet. A computer does just this. It keeps files it is using right now in RAM, and files it might need later stay on the hard drive.  Though RAM has access and response times that are two orders of magnitude faster compared to hard drives, they typical capacity is 1 - 2 orders of magnitude less that a typical hard drive.  You can fit reams of paper in the filing cabinet but only a few on your desk.

Data stored in RAM is said to be ephemeral whereas data written out to a hard drive is persistent. Meaning if the power suddenly goes out, any data that was in RAM is lost and will not be there after power is restored and the computer is booted back up.  However data that was written to the hard drive will be there when power is restored. For this reason, modern operating systems and applications will periodically write session and application related data that's currently in RAM out to the hard drive.  This way if the power goes out, only 10 minutes of data entered in a newly created spreadsheet that was being worked on for 3 hours preceding the power outage and not yet saved to the hard drive.  These files are usually denoted with a tilde~ and can be found in a temporary or temp directory or possibly located in a 'blind directory' whose contents are referred to as hidden files. 

#### More Information:
<!-- Please add any articles you think might be helpful to read before writing the article -->

<a href='https://en.wikipedia.org/wiki/Computer_data_storage' target='_blank' rel='nofollow'>Computer data storage (Wikipedia)</a>

<a href='https://en.wikipedia.org/wiki/Flying_height' target='_blank' rel='nofollow'>Flying Height (Wikipedia)</a>

<a href='https://en.wikipedia.org/wiki/Hard_disk_drive' target='_blank' rel='nofollow'>Hard disk drive (Wikipedia)</a>

<a href='https://www.pcmag.com/article2/0,2817,2404258,00.asp' target='_blank' rel='nofollow'>Hard drives vs SSDs</a>