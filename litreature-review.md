# LITERATURE REVIEW

When electronic computers were first introduced in the 1940's they were created without any operating systems. All programming language was done is absolute machine language and is generally used for making simple math operation. The first operating system was introduced in the early 1950's, it was called GMOS and was created by General Motors for IBM's machine the 701. Operating systems in the 1950's were called single-stream batch processing systems because the data was submitted in groups. By the late 1960's operating systems designers were able to develop the system of multiprogramming in which a computer program will be able to perform multiple jobs at the same time. The fourth generation of operating systems saw the creation of personal computing. Although these computers were very similar to the minicomputers developed in the third generation, personal computers cost a very small fraction of what minicomputers cost although a personal computer was so affordable that it made it possible for a single individual could be able to own one for personal use while minicomputers where still at such a high price that only corporations could afford to have them. One of the major factors in the creation of personal computing was the birth of Microsoft and the Windows operating system. The windows Operating System was created in 1975 when Paul Allen and Bill Gates had a vision to take personal computing to the next level. They introduced the MS-DOS in 1981 although it was effective it created much difficulty for people who tried to understand its cryptic commands. Windows went on to become the largest operating system used in technology today with releases of Windows 95, Windows 98, Windows XP (Which is currently the most used operating system to this day), and their newest operating system Windows 7. Along with Microsoft, Apple is the other major operating system created in the 1980's. Steve Jobs, co- founder of Apple, created the Apple Macintosh which was a huge success due to the fact that it was so user friendly. Windows development throughout the later years were influenced by the Macintosh and it created a strong competition between the two companies. Today all of our electronic devices run off of operating systems, from our computers and smartphones, to ATM machines and motor vehicles. And as technology advances, so do operating systems.

## Observations

Below are the observations of the average boot time of different operating systems images. These observations are under a certain environment:
* MacOS – 3.3 sec
* Windows 10 – 4 sec
* Windows 98 – 55 sec
* Ubuntu – 40 to 45 sec
* CentOS – 40 sec
* CirrOS – 2.5 to 3 sec
* SolusOS – 1.5 sec [on SSD] & 4 to 5 sec

## Problems in existing system (Major Objectives)

![Image of processes at boot time](https://raw.githubusercontent.com/Ashutoshcoder/operating-system/master/images/os_services.PNG)

![2nd Image of processes at boot time](https://raw.githubusercontent.com/Ashutoshcoder/operating-system/master/images/os_services_2.PNG)

* *<ins>Remove some startup programs:</ins>*
If you experience slowness between logging in and actually getting to use your computer, too many startup programs could be the culprit. A lot of software sets itself to automatically run at startup. If dozens of apps are loading as soon as you log in, this can really bog your system down right away increasing in the boot time. [19]

* *<ins>Updates:</ins>*
Upgraded Ubuntu 18.04 suddenly boots slowly.

* *<ins>Missing OS address spaces:</ins>*
When system abruptly shuts down so it affects the processes which can also affect the boot files (i.e. it abruptly writes into the memory which can lead to missing address space).

## Processes

* *<ins>Tweak the BIOS:</ins>*
When you first set up your computer, your BIOS is set up to make things a bit more convenient for you, but once you’re all set up, those things can be disabled. For Instance, on startup computers perform a lengthy power-on self-test (POST), though it's no longer necessary. If your computer happens to run a memory check or something similar, you can disable BIOS entry labeled 'power-on self-test', 'startup diagnostic'. Similarly, you can Overclock the processor or setting your CPU and memory to run at speeds higher than their official speed grade to enhance the execution of processes.

* *<ins>Clean out programs that launch at startup:</ins>*
Depending on your setup, Windows startup might load some apps, a bunch of apps, or even no apps at all. The more apps that load this way, the longer will be your PC’s startup time. Although many apps might place themselves in the startup queue, there are very few that must run when Windows boots. In fact, Windows can boot without anything in the startup queue. A “clean boot” starts the operating system with a minimal set of drivers and startup programs, (Using clean boot we can clean out the programs that launch at startup) so one can determine whether a background program is interfering with the game or program.  This is similar to starting Windows in Safe Mode, but provides you more control over which services and programs run at startup to help you isolate the cause of a problem.

* *<ins>Delayed windows services:</ins>*
A service marked as Automatic (Delayed Start) will start shortly after all other services designated as Automatic have been started, this means that the services are started 1-2 seconds after the computer boots. There are some services that are not required at the time of boot for ex Network managers, Bluetooth support etc. those services can be started later when the operating system had finished booting, hence saving the memory consumed by those services and providing memory just for the boot processes. The setting is most useful in lessening the "mad rush" for resources when a machine boot.

## Methodologies

*Disabling unneeded daemons*

The operating Systems when booting usually starts a lot of daemons which results in a long waiting state before a user can get to work after powering on their system. Some of those daemons are rarely used (or even not all) by the majority of users. Hence, disabling unused or rarely used daemons at startup can result in faster boot sequences and less CPU load. Although one needs to be cautious while disabling daemons as disabling an important daemon can have serious consequences. Most distributions feature some kind of tool which allows you to manage daemons that are started on your computer when booting. The most common one is chkconfig, which features a command line interface. There is also a GUI for daemon startup configuration. A well-known one is serviceconf.
This is a bit more advanced, so best not to do it if you don't know what this means. Install bum, and start it with root privileges. Then just untick the boxes in front of the daemons you are sure you don't need. For instance, when you don't have a scanner, you can disable scanner services. And if you never use Bluetooth, you can disable Bluetooth as well. When you're done, hit the Apply those changes to effect.

**How to make Linux boot faster?**

Any productive machine needs to be up and running as soon as possible, and a sluggish boot can hinder your efforts – which is why boot times were the first thing we thought about improving. There could be several reasons for the system for getting slower over time. For instance, the system may be equipped with basic configuration, there might be several applications installed which are eating up resources at boot time or many unnecessary services which are launched at startup. Many improvements have been made to Linux distributions' boot time. Modern init systems deal well with doing things concurrently and on-demand. On a modern system, once the kernel starts executing, it can take very few seconds to get to a login prompt.

If we can reduce the hardware's boot time, these teams can become more productive, and end users may be grateful when they're setting up systems or rebooting to install firmware or OS updates.

*<ins>Remove the timeout</ins>*

You may notice that each time you boot there's a small count-down from three to zero. This was introduced originally to ensure that older hardware loaded modules in time for the kernel to boot. The boot menu time-out determines how long the boot menu is displayed before the default boot entry is loaded. It is done in seconds. If extra time is needed to choose the operating system that loads on your computer, you can extend the time-out value. Or, you can shorten the time-out value so that the default operating system starts faster.

In a dual boot configuration, a list of all installed operating systems will be displayed by the modern boot loader for 30 seconds. After this period of time, if the user has not touched the keyboard, the default operating system will be started. As the system goes to a waiting state until the choice is made, so you might want to change this timeout to some other minimum value. As this is not necessary for modern systems, and can be removed by opening /boot/grub/menu.lst in a text editor with root permissions and finding the line showing:

timeout=3

Once you've found it, change the value to zero. Save and exit then reboot and you should notice you have just knocked three seconds off your boot time. /boot is an important folder in Linux. /boot folder contains all the boot related info files and folders such as grub.conf, vmlinuz image aka kernel. We need to reduce the processes starting at the boot in order to reduce the boot time.

**Terminal**

FASTER BOOTS: You could edit a text file and restart your machine to profile your system, or just click a few buttons in Grub.

*<ins>Run boot processes in parallel</ins>*

Parallelism can lead to big performance boosts, because running two processes at once will take half the time of running them sequentially (at least in theory). You can take advantage of this technique in Grub by firing up /etc/init.d/rc in a text editor with root permissions and finding the following line:

CONCURRENCY=none

You would then replace none with shell before saving and closing your text editor. When you reboot you should see a noticeable decrease in your boot times (around one or two seconds in most cases). If you don't see an increase, this is because this tweak is aimed primarily at systems with multi-core processors. If you have a solo-core processor you could actually increase your boot time if you use this tweak, which was the case with our test system where we saw a 2.4-second increase.

In particular, the data accessed during initialization (hereinafter “necessary data”) is loaded into a non-volatile cache and marked or “pinned” to prevent eviction. Accordingly, the necessary data Would be resident in the cache for fast access during system initialization even following an unexpected system shutdown, thereby avoiding accesses to the disk.[17]
