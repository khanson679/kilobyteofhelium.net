<!--
.. title: Linux Adventures
.. slug: linux-adventures
.. date: 2022-12-23
.. tags: linux, Ubuntu
.. category: linux
.. link: 
.. description: 
.. type: text
-->

I've been using [Linux](https://en.wikipedia.org/wiki/Linux) in some capacity for over 10 years now, and it's been my primary operating system for about 7.
For the most part, it's served my needs well.
It's also been interesting to watch Linux mature as a desktop OS while Windows has mostly gotten *worse* over the same time period.
In this post I want to talk a bit about my journey.


# What even is Linux?

For those who aren't aware, Linux is one of the major general purpose operating systems, along with Windows and Mac OS.
Linux is extremely prevalent on web servers, and utterly dominates scientific and high-performance computing, but is still pretty marginal on ordinary PCs.
Technically, Android and ChromeOS are built on top of Linux, but these are very different products, and it's not helpful to lump them together.

There are a couple factors that distinguish Linux from its competitors.
The first is that it is free and open source software ("FOSS").
This means that anyone can acquire, modify, and redistribute the source code.
In the past, Linux was mostly developed by volunteers and hobbyists, but nowadays a large proportion of contributions come from corporations that use it as a foundation for various products and services.

The second distinguishing factor is that the various parts of the system, such as the Linux kernel (the core of the system) and the graphical and audio subsystems, are independent projects.
These are assembled into complete systems called called "distros" (short for "distribution").
Most of the big distros that you may have heard of, like Ubuntu, Fedora, and Arch, are overwhelmingly similar to each other.
No matter which you use, you're getting the Linux kernel, X.Org or Wayland for graphics, PulseAudio for audio, and so on.
Because of this, which to use mostly comes down to personal preference.

Perhaps the coolest thing about Linux from the user perspective is that there are several completely different graphical interfaces available, called "desktop environments".
Imagine being able to put the Mac interface on your Windows 10 installation, or vice versa.
That's basically the situation with Linux.
If one desktop environment doesn't suit your fancy, you can swap it about for another.


# Early Experiments

I'm not sure exactly when I first discovered Linux, though in high school I had a friend who had it installed on his PS3 (yes, you could do that back then!), along with an old desktop.
Partly inspired by this, I played around with Ubuntu and several other distros using virtual machines.

A [virtual machine](https://en.wikipedia.org/wiki/Virtual_machine) is exactly what it sounds like.
Basically, it's a program that you run on your computer like any other, which allows you to run *a whole other operating system* inside.
From the perspective of the "guest" operating system, it's just running on ordinary computer hardware, but this is an illusion created by the virtual machine software.
In reality, it's sharing the hardware of the "host" system.
From the user perspective you get get a normal window showing the virtual display.
You can click into it and use your keyboard like any other program, give it pass-through internet access and so on.
The concept is similar to but not exactly the same as an emulator, which simulates a completely different kind of computer (emulators are commonly used for playing old video games on modern computers).

The software I was using is called [VirtualBox](https://en.wikipedia.org/wiki/VirtualBox), and it's still around today.
I highly recommend it as a way of getting your feet wet.
You can install and try out different distros without affecting your current setup, and you can screw around to your heart's content with essentially no risk of damage to the host system.

It was probably around 2008 when I started doing this.
Linux really wasn't ready for prime time yet, though things were changing rapidly.
I experimented a lot with [Ubuntu](https://en.wikipedia.org/wiki/Ubuntu), then a newcomer, which was more polished and user friendly that its competitors at the time.

But there were a lot of stupid problems.
I remember "not having permission" to use my CD burner.
Thinking myself clever, I opened the command line and used "sudo" command to start the CD burning program as the superuser (=administrator).
This worked, but it also broke the graphical system, and the next time I started the virtual machine I could only log in to the command line.
It turns out you're only supposed to use "sudo" with command line programs (this is a common beginner mistake).
Sure, I was able to fix the problem by Googling, but not being allowed to use your CD burner by default is a pretty stupid design.

Suffice to say, the situation is lot better nowadays.
Actually, things really started to come together within the next couple of years, and
I think this was in part because of the level of community engagement at the time.
Unfortunately, the cloud and mobile revolutions in the mid 2010s soon sucked attention away from desktop computing -- it wasn't "hip" anymore.
Progress has been a lot slower since then.


# Linux for Programming

In college we used Linux for most of my computer science classes.
We were taught how to use SSH to log in to a server, and navigate using the terminal (command line), and write our programs in Vim (a hardcore programming text editor).
I kept up with the first two, but gave up on Vim after a semester -- it was just too weird.
Nowadays I could probably make myself learn it, but now I have [Sublime Text](https://www.sublimetext.com/), which basically does everything I could possibly ask for.

The department's Linux workstations and servers all ran [Debian](https://en.wikipedia.org/wiki/Debian).
The only reason I knew this was because of the default desktop background.
Since everything was managed by the department, the choice of distro was more or less irrelevant for us.

I feel like I really got going one summer when I worked as a research assistant for a computer science lab.
I was basically a grunt programmer, but it was a perfect opportunity to work on my techie skills while getting paid.
We had a little robot running Ubuntu, and we needed to offload some of the heavy computing to another Ubuntu computer.
Naturally, I did all my work on an Ubuntu workstation as well.
I taught myself how to install and configure all the software we needed.
By the end of the summer, I more or less knew what I was doing.

In the process, I also got used to using Ubuntu for everyday tasks.
I was using [Gnome 2](https://en.wikipedia.org/wiki/GNOME_2) as my desktop environment, the default at the time.
It was basically fine.
The interface was snappy, updates were quick and painless, and I had Firefox, LibreOffice, and Dropbox.
When there was a problem, it was very easy to ask Google what package I needed to install, or what setting to change.

My understanding is that by this point there were two big issues holding Linux back: (1) hardware compatibility and (2) inability to run most games and commercial software.
My work computer was a generic Dell desktop; if you had a laptop and the WiFi didn't work, then you'd be pretty much out of luck.
Likewise, I had no need for any specific proprietary software at work.
Both of these issues have diminished considerably in the years since then, but I think they are still the two major sticking points.

I continued to use Windows on my personal computer mostly for software reasons, but I installed [Linux Mint](https://en.wikipedia.org/wiki/Linux_Mint) in a dual-boot configuration for programming.
Linux provides a way better programming environment than Windows, especially for beginners.
Make a little Python program, type "python3 name-of-program.py", and you're on your way.
Only in the last few years with the advent of [WSL 2](https://en.wikipedia.org/wiki/Windows_Subsystem_for_Linux), which is basically glorified virtual machine, has the gap narrowed at all.
In any case, by this point I more or less knew that I'd be able to switch to Linux full time should I feel inclined.


# Goodbye, Windows

It was an incident at work while I was teaching English in Japan that prompted me to finally pull the trigger.
My computer decided to reboot and install updates right before I was about to teach a class.
As anyone who has ever used a Windows computer knows, this can take *forever*.
I lost precious class time, and I was pissed.
My lessons were not the kind where you could just stop when the bell rang and pick up the next day.
I only saw my kids once a month -- if the day's activity couldn't be finished in 45 minutes then that was it, the end.
But I digress.

It's possible that I had left to do something and the usual 15 minute countdown appeared---and concluded---while I was gone, or it could have been an irregularity.
The fact of the matter is that this sort of thing is not acceptable.
*I* will decide whether or not now is an okay time to update my computer.

By this time Windows 10 was already out, and I knew that this sort of behavior was becoming a matter of policy -- you didn't own your computer anymore.
So, I decided that this would be a good time to try making Linux my primary operating system.
I started doing all my work on my Linux Mint install, only switching back to Windows when absolutely necessary, which it rarely was.

I transitioned from Microsoft Office to LibreOffice.
LibreOffice Writer was already quite good, actually superior to Word in many ways.
Calc, the spreadsheet app, was perfectly adequate for my purposes.
Impress, the PowerPoint equivalent, was pretty bad (it still is), but that didn't really matter to me.

Some of my programs, like Firefox and Dropbox, were already available on Linux, so no change there.
I switched from Notepad++ to Sublime Text, and couldn't be happier.
I really only missed two things: Age of Empires (an RTS game) and Sibelius (music composition software).
Even so, I could boot back into Windows just for those, so who cares.
I already had a desktop at home that only ran Linux Mint, so I was already used to that as well.

And that was basically it.
In my day-to-day life, Linux has suited me just fine, though there have been a few hiccups.
I'll mention a couple big ones.

For various reasons, I experimented with several desktop environments, eventually settling on KDE, which I consider to be the true successor to old-school Windows.
So what was the problem?
Well, the transition from KDE 4 to version 5 was happening around this time, and it was a bit messy.
The first few releases of KDE 5, officially "Plasma 5", were so buggy that they were unusable, while KDE 4 was no longer being developed, and therefore not receiving any bug fixes and improvements.
Linux Mint, which tracks the LTS (2 year release cycle) version of Ubuntu, was stuck on the frozen KDE 4, while the most recent non-LTS (6 month) releases of Ubuntu had the buggy Plasma 5.
By 2016, though, Plasma 5 was more or less fine, and it has only gotten better and better since then.
Linux Mint discontinued their KDE release, so I went with Ubuntu.

Another problem is that Ubuntu started to go down in quality of releases, failing to fix old problems while creating new ones.
For example, in one release they broke Bluetooth, then refused to fix it for "stability" reasons.
You see, in Linux distro world, "stable" doesn't mean "works as intended and doesn't crash"; it means "no changes in functionality".
Never mind the fact that broken software is, well, broken, and therefore useless.
Anyway, it was a simple matter of installing the bugfix via the lovely Ubuntu [PPA](https://help.ubuntu.com/community/PPA) system.

If you think this sounds kind of crappy, well, it is.
But the thing is, if Ubuntu ever becomes intolerable, it's very easy to switch to something else.
If Microsoft, Apple, or Google ruins something for you, you have no recourse; with Linux, you have options.

At the same time, I've been watching Windows going downhill since Windows 8, while Linux has been improving.
I've had the exquisite displeasure of helping family members troubleshoot and fix the most insane problems with Windows 10---things that never could have happened with Linux, nor with Windows 7---and you know what, I think I'm getting a better deal right now.

My computer is snappy and responsive despite being 5 years old and only having a dual-core CPU.
My software updates are instantaneous and rarely require reboots; upgrading to the next version of Ubuntu takes minutes, not hours.
Plasma 5 is beautiful, functional, and customizable; Windows 10 is ugly and full of irritating pop-ups, advertisements, and spyware.
I have can install almost all of my software automatically with a single command if I ever need to setup a new computer.
Some of my old games that I play using [Wine](https://en.wikipedia.org/wiki/Wine_(software)) or in a virtual machine don't work on recent versions of Windows anyway.

Oh, and before you suggest that I get a Mac: no.
Apple's computers are overpriced, I don't like their hardware or their software, and I still can't play my games without Wine.


# Linux for everyone?

So, you might be wondering if I recommend other people to switch to Linux nowadays.
Actually, no, not necessarily.
Linux is ideal for two groups of people: those with very basic needs, who basically spend all their time in a web browser, and power users, who are willing to take the time to learn how to setup and maintain their system.
For everyone else, it depends.

Again, hardware and software compatibility are the big problems.
You can, and should, put Linux on a flash drive and give it a test run (the installer for most distros doubles as a demo system).
If it works well on your computer, great!
If it doesn't work right, and you're not willing to fiddle around to make it work, then that's that.
Likewise if you need MS Office, or the Adobe suite, or whatever.

Also, you need to find a desktop environment that suits your preferences.
If you liked Windows 7, then I think you'll love KDE/Plasma.
If you are used to Mac OS, you might prefer Gnome.
And if the first thing you try isn't quite right, you'll need to experiment, because there are several good options out there.
If this is fun for you like it is for me, then go for it.
But the fact is that a lot of people just don't care that much, and find this to be too much effort.

Finally, there's the problem of choosing a distro.
I'm of the opinion that it doesn't matter that much.
I suggest Ubuntu, not because I'm convinced that it's the best, but because it's available with almost every major desktop environment, and it's popular, so it's easy to get help.
But if you have a friend or family member who can provide you with tech support and they use something different, then maybe try that instead.
