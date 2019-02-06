# NMAP CHEATSHEET

## nmap
```
$ nmap 8.8.8.8
 Starting Nmap 7.70 ( https://nmap.org ) at 2019-02-06 01:54 PST
 Nmap scan report for google-public-dns-a.google.com (8.8.8.8)
 Host is up (0.042s latency).
 Not shown: 999 filtered ports
 PORT   STATE SERVICE
 53/tcp open  domain
```
## nmap -sS vs nmap -sT

## nmap -p
Specify which ports to scan (1-65535 = TCP Range)
```
$ nmap -p 1-65535
```
## nmap -sV
Probe open ports to determine service/version info



## nmap -O
OS identification
```
$ nmap -O 172.16.0.15
 Starting Nmap 5.21 ( http://nmap.org ) at 2015-06-23 09:49 EST
 Nmap scan report for 172.16.0.15
 Host is up (0.00032s latency).
 Not shown: 996 closed ports
 PORT STATE SERVICE
 88/tcp open kerberos-sec
 139/tcp open netbios-ssn
 445/tcp open microsoft-ds
 631/tcp open ipp
 MAC Address: 00:00:00:00:00:00 (Unknown)
 Device type: general purpose
 Running: Apple Mac OS X 10.5.X
 OS details: Apple Mac OS X 10.5 - 10.6 (Leopard - Snow Leopard) (Darwin 9.0.0b5 - 10.0.0)
 Network Distance: 1 hop
```


## nmap -Pn (disable ping)
Treat all hosts as online -- skip host discovery


## nmap -iL
Scans a list of IP addresses
```
nmap -iL ip-addresses.txt
```
## nmap -T
Set timing template - higher is faster (less accurate)

## OUTPUT PARAMETERS
```
$ nmap -oA
//Output in the three major formats at once (-oN,-oX,-oG)
$ nmap -oN
//Normal Output
$ nmap -oG
//GREPable Output
$ nmap -oX
//XML Output
```
## nmap -sS -sV --script=vulscan www.google.com
//Vulscan is a module which enhances nmap to a vulnerability scanner. 
