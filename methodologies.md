# Methodologies 

- Disabling unneeded daemons: 
The operating Systems when booting usually starts a lot of daemons which results in a long waiting state before a user can get to work after powering on their system. Some of those daemons are rarely used (or even not all) by the majority of users. Hence, Disabling unused or rarely used daemons at startup can result in faster boot sequences and less CPU load. Although one needs to be cautious while disabling daemons as disabling an important daemon can have serious consequences.Most distributions feature some kind of tool which allows you to manage daemons that are started on your computer when booting. The most common one is chkconfig, which features a command line interface.There is also a GUI for daemon startup configuration. A well-known one is serviceconf.
This is a bit more advanced, so best not to do it if you don't know what this means. Install bum, and start it with root privileges. Then just untick the boxes in front of the daemons you are sure you don't need. For instance, when you don't have a scanner, you can disable scanner services. And if you never use bluetooth, you can disable bluetooth as well.When you're done, hit the Apply those changes to effect.

- How to make Linux boot faster :
Any productive machine needs to be up and running as soon as possible, and a sluggish boot can hinder your efforts – which is why boot times were the first thing we thought about improving. There could be several reasons for the system for getting slower over time. For instance, the system may be equipped with basic configuration, there might be several applications installed which are eating up resources at boot time or many unnecessary services which are launched at startup.
Many improvements have been made to Linux distributions' boot time. Modern init systems deal well with doing things concurrently and on-demand. On a modern system, once the kernel starts executing, it can take very few seconds to get to a login prompt.
If we can reduce the hardware's boot time, these teams can become more productive, and end users may be grateful when they're setting up systems or rebooting to install firmware or OS updates.

- Remove the timeout : 
You may notice that each time you boot there's a small count-down from three to zero. This was introduced originally to ensure that older hardware loaded modules in time for the kernel to boot. The boot menu time-out determines how long the boot menu is displayed before the default boot entry is loaded. It is done in seconds.If extra time is needed to choose the operating system that loads on your computer, you can extend the time-out value. Or, you can shorten the time-out value so that the default operating system starts faster.
In a dual boot configuration, a list of all installed operating systems will be displayed by the modern boot loader for 30 seconds. After this period of time, if the user has not touched the keyboard, the default operating system will be started. As the system goes to a waiting state until the choice is made, So you might want to change this timeout to some other minimum value. 
As this is not necessary for modern systems, and can be removed by opening /boot/grub/menu.lst in a text editor with root permissions and finding the line showing :
timeout=3.
Once you've found it, change the value to zero. Save and exit then reboot and you should notice you have just knocked three seconds off your boot time. /boot is an important folder in Linux. /boot folder contains all the boot related info files and folders such as grub.conf, vmlinuz image aka kernel. We need to reduce the processes starting at the boot in order to reduce the boot time.


- Terminal
FASTER BOOTS: You could edit a text file and restart your machine to profile your system, or just click a few buttons in Grub

- Run boot processes in parallel
Parallelism can lead to big performance boosts, because running two processes at once will take half the time of running them sequentially (at least in theory). You can take advantage of this technique in Grub by firing up /etc/init.d/rc in a text editor with root permissions and finding the following line:
CONCURRENCY=none
You would then replace none with shell before saving and closing your text editor. When you reboot you should see a noticeable decrease in your boot times (around one or two seconds in most cases). If you don't see an increase, this is because this tweak is aimed primarily at systems with multi-core processors. If you have a solo-core processor you could actually increase your boot time if you use this tweak, which was the case with our test system where we saw a 2.4-second increase.

> In particular, the data accessed during initialization (hereinafter “necessary data”) is loaded into a non-volatile cache and marked or “pinned” to prevent eviction.Accordingly, the necessary data Would be resident in the cache for fast access during system initialiZation even following an unexpected system shutdoWn, thereby avoiding accesses to the disk.[17]
