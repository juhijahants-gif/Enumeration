# Enumeration
Enumeration Techniques

# Explore Google hacking and enumeration 

# AIM:

To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

Following Categories of pen test tools are identified:
Information Gathering.

Google Hacking:

Google hacking, also known as Google dorking, is a technique that involves using advanced operators to perform targeted searches on Google. These operators can be used to search for specific types of information, such as sensitive data that may have been inadvertently exposed on the web. Here are some advanced operators that can be used for Google hacking:

site: This operator allows you to search for pages that are within a specific website or domain. For example, "site:example.com" would search for pages that are on the example.com domain.
Following searches for all the sites that is in the domain google.com

<img width="955" height="930" alt="image" src="https://github.com/user-attachments/assets/aed1aaea-9290-45b1-9488-bece458fee98" />

filetype: This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
Following searches for pdf file in the domain google.com

<img width="955" height="930" alt="image" src="https://github.com/user-attachments/assets/2f5b987d-3ac2-41ac-b379-19c858a3588d" />



intext: This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.

<img width="955" height="930" alt="image" src="https://github.com/user-attachments/assets/6f9b29ff-04d9-4a01-8e35-6ed59c752f58" />


inurl: This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.

<img width="955" height="930" alt="image" src="https://github.com/user-attachments/assets/ed1e101c-e249-475d-a0aa-8c389aa6d547" />


intitle: This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag:

<img width="955" height="930" alt="image" src="https://github.com/user-attachments/assets/756473eb-de79-4311-b872-d84fbb77f0a6" />


link: This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.
<img width="955" height="930" alt="image" src="https://github.com/user-attachments/assets/7afd5584-be34-4c03-a514-b585f3d6edb9" />


cache: This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.

 
#DNS Enumeration


##DNS Recon
provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion
## OUTPUT:







##dnsenum
Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:

<img width="1600" height="785" alt="image" src="https://github.com/user-attachments/assets/c53bed55-194b-452f-9bf7-7e94750a10c8" />


Get the host’s addresses (A record):
```
dig google.com A
```

<img width="532" height="287" alt="image" src="https://github.com/user-attachments/assets/a7fe919c-3237-48f8-9237-364528abc8fb" />


Get the namservers (threaded):
```
dig google.com NS
```



<img width="538" height="482" alt="image" src="https://github.com/user-attachments/assets/11a71faa-b289-465f-b4d3-e53e91bd8391" />


Get the MX record (threaded):
```
dig google.com MX
```

<img width="482" height="470" alt="image" src="https://github.com/user-attachments/assets/7bde099f-20bb-4eff-89a4-fe31c6f51f32" />

Perform axfr queries on nameservers and get BIND versions(threaded).
Get extra names and subdomains via google scraping (google query = “allinurl: -www site:domain”).
Brute force subdomains from file, can also perform recursion on subdomain that have NS records (all threaded).
Calculate C class domain network ranges and perform whois queries on them (threaded).
Perform reverse lookups on netranges (C class or/and whois netranges) (threaded).
Write to domain_ips.txt file ip-blocks.
This program is useful for pentesters, ethical hackers and forensics experts. It also can be used for security tests.


##smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.


In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:

select any username in the first column of the above file and check the same


#Telnet for smtp enumeration
Telnet allows to connect to remote host based on the port no. For smtp port no is 25
telnet <host address> 25 to connect
and issue appropriate commands
  
 ##Output
  
  

## nmap –script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.


## OUTPUT:


## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully

