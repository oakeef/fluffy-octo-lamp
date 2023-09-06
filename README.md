
# How to set up an X86 Windows 10 VM on an M1/M2 Mac


## ====== Prerequisites ====== 

Download and install UTM on mac:
https://mac.getutm.app/

Download Windows 10 image from here: 
https://www.microsoft.com/en-ca/software-download/windows10


## ========= Step 1 ==========

Click on Create a New Virtual Machine

Select Emulate

Select Windows

> Settings:
> - Install Windows 10 or Higher
> - Click Browse and select your Windows 10 ISO from above
> - Install drivers and SPICE tools

Continue to next page

> Settings:
> - X86_64
> - Standard PC (Q35 + ICH9, 2009) (alias of pc-q35-7.2) (q35)
> - 4GB Memory (8GB is preferred if you have 16GB Memory)
> - 6 CPU Cores

Continue to next page

> Settings:
> - 64GB Storage (Storage is dynamic so it doesn't take up 64GB right away)

Continue to next page

Feel free to set up a Shared Directory if you want but you can set this up later as well

Continue to next page and if all the settings look right then click Save


## ========= Step 2 ==========

Go into settings before starting the VM and change the following:

> SYSTEM > CPU
> - QEMU Virtual CPU Version 2.5+ (qemu64-v1)
> - Force Multicore


## ========= Step 3 ==========

***Everything from here on will be very slow because it is being emulated so have patience. Some of these next steps will take 20+ mins***

Boot up VM and press any key when it tells you to to boot from DVD

Install Windows 10


## ========= Step 4 ==========

When it reboots it will blue screen. That is ok Turn Off VM and change the following settings:

> QEMU
> - TPM 2.0 OFF

Boot up VM again


## ========= Step 5 ==========

Run through Windows First Run Wizard


## ========= Step 6 ==========

When the setup is complete, install SPICE guest tools

The end
