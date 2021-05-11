# What is it?
Osysinfo is a basic CLI tool to see your system details. 

It utilizes flags to allow you to limit the information shown to you.

# How does it work?
The format of the command is as follows:

```
osysinfo -flag option
```

Here's a list of flags: 
```
     -f
       Return information about everything
     -sy
       Return general information about the system
     -c
       Return information about the CPU
     -m
       Return information about the memory
     -sw
       Return information about the swap space
     -n
       Return information about the network
```
       
       
Here are the additional options to filter the previous categories further:
```
      -sy
        Default: 'full'
        Alternative options: st - System type, d - Distribution, h - Hostname, kv - Kernel version, kd - Kernel date, pr - Processor, pl - Platform, u - Uptime
      -c
        Default: 'full'
        Alternative options: c - Cores, max - Max. frequency, min - Min. frequency, cf - Current frequency
      -m
        Default: 'full'
        Alternative options: t - Total, a - Available, u - Used, p - Percentage
      -sw
        Default: 'full'
        Alternative options: t - Total, f - Free, u - Used, p - Percentage
      -n
        Default: 'full'
        Alternative options: ip - IP address, n - Netmask, bip - Broadcast IP, ma - MAC address, mn - MAC netmask, bm - Broadcast MAC
```
# Examples
Thus if you for example run ```osysinfo -c c```, it will output the following:
```
------- CPU
Cores: x cores (y threads)
```
where x refers to your number of cores and y to your number of threads.


Simply running ```osysinfo -c``` wouĺd output:
```
------- CPU
Cores: x cores (y threads)
Max. frequency: aMhz
Min. frequency: bMhz
Current frequency: cMhz
```
where x and y are as before and a, b and c are the different frequency values.

![Screenshot from 2021-05-10 22-17-39](https://user-images.githubusercontent.com/60475104/117725471-dc84fa80-b1ed-11eb-8a7c-0657b0e1fb54.png)
![Screenshot from 2021-05-10 22-17-50](https://user-images.githubusercontent.com/60475104/117725489-e149ae80-b1ed-11eb-9d11-608ba28ea08c.png)
![Screenshot from 2021-05-10 22-18-01](https://user-images.githubusercontent.com/60475104/117725495-e27adb80-b1ed-11eb-9d72-39e4492f3c08.png)
![Screenshot from 2021-05-10 22-18-21](https://user-images.githubusercontent.com/60475104/117725498-e3137200-b1ed-11eb-9e65-845371b24401.png)


# Dependencies
There are some dependencies for installing osysinfo. These are the following python modules:

- fire
- distro
- psutil

To install them, just run the following with pip installed (you may have to use pip3 instead of pip):

```
pip install fire
pip install distro
pip install psutil
```
# Installation
With the dependencies installed, to install osysinfo, simply download the source code and move the osysinfo file to /usr/local/bin/ and make it executable.

As root, do the following:
```
mv /path/to/osysinfo /usr/local/bin/
chmod +x /usr/local/bin/osysinfo
```

Once that is done you should be able to run osysinfo with the flags mentioned previously and find the provided system details.

There is also an AUR package for Arch (credit to bobolin for that): https://aur.archlinux.org/packages/osysinfo/
