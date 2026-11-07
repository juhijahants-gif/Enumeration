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
<img width="960" height="799" alt="image" src="https://github.com/user-attachments/assets/36b91d6f-59ec-4313-af97-5058c64c9a00" />


##dnsenum

Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:

Get the host’s addresses (A record).
Get the namservers (threaded).
Get the MX record (threaded).
Perform axfr queries on nameservers and get BIND versions(threaded).
Get extra names and subdomains via google scraping (google query = “allinurl: -www site:domain”).
Brute force subdomains from file, can also perform recursion on subdomain that have NS records (all threaded).
Calculate C class domain network ranges and perform whois queries on them (threaded).
Perform reverse lookups on netranges (C class or/and whois netranges) (threaded).
Write to domain_ips.txt file ip-blocks.
This program is useful for pentesters, ethical hackers and forensics experts. It also can be used for security tests.
<img width="958" height="832" alt="image" src="https://github.com/user-attachments/assets/cc404b81-5e63-421b-ae1b-17f4e82ff760" />
##SMTP User Enumeration – smtp-user-enum
## Create username list and VRFY enumeration 
<img width="701" height="413" alt="image" src="https://github.com/user-attachments/assets/887ba4c8-fd00-46a4-ae03-b6dc6c3761d4" />
## RCPT enumeration
<img width="764" height="412" alt="image" src="https://github.com/user-attachments/assets/99f6ff2c-9a9b-4384-bba4-f2f4b0ceddfe" />
##EXPN enumeration
<img width="746" height="377" alt="image" src="https://github.com/user-attachments/assets/a65892bd-a268-438a-b7ac-c380f50bd2d9" />
###Telnet for SMTP Enumeration
<img width="448" height="390" alt="image" src="https://github.com/user-attachments/assets/6ff86eae-c98e-4988-8656-a0bd6f5791e0" />
###Nmap – smtp-enum-users.nse
<img width="690" height="192" alt="image" src="https://github.com/user-attachments/assets/92ac1b92-5e57-4d6a-8761-09dc29ad6c10" />


## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully

