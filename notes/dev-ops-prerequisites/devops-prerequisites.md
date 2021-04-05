https://youtu.be/Wvf0mBNGjXY

![](images/curriculum.png)

## Linux Basics

Create folder tree in single command
    
`mkdir -p /home/sub1/sub2`

`rm -r /home/sub1/sub2`

`cp -r  <source-folder-tree> <destination>`


`curl <link of the file> -O`

-O to save the file, else it just prints out

`wget <link_to_file> -O "filename"`

Check OS Version

`ls /etc/*release*`

`cat etc/*release*`
 
Cent OS package manager
RPM - RedHat Package Manager

![](images/2020-10-01-13-31-56.png)

RPM does not install the dependency pakages, it just installs the \<package_name>.rpm file.

YUM is a High Level Package manager that overcomes this problem.

`yum install <package-name>`

yum uses rpm to install packages

repo info is stored at `/etc/yum.repos.d`

`yum repolist`
![](images/images/2020-10-01-13-35-57.png)



## Sevices

Run a service even after reboot
![](images/2020-10-01-13-38-30.png)

systemd file is rquired to achieve this

![](images/2020-10-01-13-40-32.png)

inside `/etc/systemd/system` folder create a \<servicename>.system file

the file must contain

    [Service]
    ExecStart=<command to execute after reboot>

    [Install]
    WantedBy=multi-user.target

then run `systemctl daemon-reload` to enable it

finally 
`systemctl start <service name>`

`systemctl enable <service-name>`

Example

Docker Service FIle
![](images/2020-10-01-13-45-50.png)


## [Daemon](images/https://en.wikipedia.org/wiki/Daemon_(computing))

A daemon is a computer program that runs as a background process, rather than being under the direct control of an interactive user.

raditionally, the process names of a daemon end with the letter d

syslogd is a daemon that implements system logging facility, and sshd is a daemon that serves incoming SSH connections. systemd is also notable

## VI Editor

`vi filename`

![](images/2020-10-01-13-49-12.png)

![](images/2020-10-01-13-49-56.png)


Tools

Source Code Management

    Git 

Build Tool

    Jenkins

Language / Framework

    Java
    Python
    Node.js

Web Server

    Apache
    Tomcat
    Nginx

Databases
    
    MySQL
    MongoDB

Containerization Tools

    Docker
    Kubernetes

Automation Tools

    Ansible - Orchestration 
    Chef
    Puppet

Cloud Management Tools

    NoCloudSDk ??


## Connecting to a Remote Machine

Windows - RDP Services

Linux `service sshd status` SSH Service

if ip address is not set, run the following
![](images/2020-10-01-14-06-49.png)

## [NAT](https://en.wikipedia.org/wiki/Network_address_translation)

Network address translation (NAT) is a method of remapping an IP address space into another by modifying network address information in the IP header of packets while they are in transit across a traffic routing device.

**IP masquerading** is a technique that hides an entire IP address space, usually consisting of private IP addresses, behind a single IP address in another, usually public address space.

