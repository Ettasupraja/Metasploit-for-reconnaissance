# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:
Find out the ip address of the attackers system
## OUTPUT:
![1](https://github.com/user-attachments/assets/c1c077a0-3fe2-440c-8018-807faab0a4a4)
Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows:
systemctl start postgresql
msfdb init
Invoke msfconsole:
![2](https://github.com/user-attachments/assets/80a3d1cc-52a3-446d-9682-9f78d35f8dab)
Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.
![WhatsApp Image 2025-03-28 at 18 03 52_8b3a2af8](https://github.com/user-attachments/assets/5e63a20e-dcea-4fc4-aa7b-a8692ce1bb27)
Port Scanning: Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000
OUTPUT:
![3](https://github.com/user-attachments/assets/97f87fb1-c98d-419e-b178-f60c3b64b086)
multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l
output:
![WhatsApp Image 2025-03-28 at 18 11 24_991c9ddc](https://github.com/user-attachments/assets/b507ca0c-1912-49b6-96ab-c5820f340a67)
Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit
output:
![WhatsApp Image 2025-03-28 at 18 13 52_0bc8c487](https://github.com/user-attachments/assets/ad483593-c346-410a-916e-38778f3c9a7c)
The info command provides information regarding a module or platform,
![WhatsApp Image 2025-03-28 at 18 17 09_607f10bf](https://github.com/user-attachments/assets/99dda179-a69e-40fe-9588-f2c207102bfb)
MYSQL ENUMERATION
Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>
![4](https://github.com/user-attachments/assets/c88a471b-6404-4ae2-a4fc-3d01adc6fb54)
Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql
use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version
![5](https://github.com/user-attachments/assets/dcff7eb0-7d5f-47de-93bf-8cc823f4658a)

## RESULT:
The Metasploit framework for reconnaissance is  examined successfully.
