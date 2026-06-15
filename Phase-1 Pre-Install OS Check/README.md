# Phase-1 Pre-Install OS Check
### First ==> middleware team Raise the CAB {Change Advisory Board} Ticket 
These Phase perform by Both Teams Linux and Middleware teams in the fresh OS, So both teams performs the Below action and take the screenshots as evidence

## Check OS version
```
cat /etc/os-release
```
Why ? 

   Websphere support specific OS only  ==>  If the OS is unsupported, IBM will not provide support.

## Check available disk space 
```
df -hP /apps /opt /tmp /home 
```
Why ? 

   Websphere required specific Space, if not installation Failed
	In Real-Time these "/apps/IBM" these path is mounted as sperate Disk using LVM, so that we can increase volume for these PATH 

/apps atleast need 15 GB for free Websphere Installation

## Check available RAM
```
free -m
```
Why ? 

   Websphere required specific Space, if not installation Failed

## Check JAVA
```
java -version
```
Why ? 
	Installation Manager ships with its own JDK, but organizations verify existing Java installations to avoid conflicts.
	Because  Server already has: Oracle Java (or) OpenJDK, So Middleware team documents them before installation.
