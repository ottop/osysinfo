Osysinfo is a basic CLI tool to see your system details. 

It utilizes flags to allow you to limit the information shown to you.


The format of the command is as follows:

osysinfo -flag option


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
       
       
Here are additional options to filter the previous categories further:
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
      n
        Default: 'full'
        Alternative options: ip - IP address, n - Netmask, bip - Broadcast IP, ma - MAC address, mn - MAC netmask, bm - Broadcast MAC
```
  
Thus if you for example run "osysinfo -c c" (without the quotation marks obviously), it will output the following:

------- CPU
Cores: x cores (y threads)

where x refers to your number of cores and y to your number of threads.


Simply running "osysinfo -c" wouĺd output:

------- CPU
Cores: 6 cores (6 threads)
Max. frequency: 4600.00Mhz
Min. frequency: 800.00Mhz
Current frequency: 2721.57Mhz

where x and y are as before and a, b and c are the different ffrequency values.


There are some dependencies for installing osysinfo. These are the following python modules:

- fire
- distro
- psutil

To intall them, just run the following with pip installed (you may have to use pip3 instead of pip):

```
pip install fire
pip install distro
pip install psutil
```

With the dependencies installed, to install osysinfo, simply download the source code and move the osysinfo file to /usr/local/bin/ and make it executable.

As root, do the following:
```
mv /path/to/osysinfo /usr/local/bin/
chmod +x /usr/local/bin/osysinfo
```

Once that is done you should be able to run osysinfo with the flags mentioned previously and find the provided system details.
