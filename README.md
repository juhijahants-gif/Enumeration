<img width="792" height="498" alt="image" src="https://github.com/user-attachments/assets/9450d429-ecb1-45e5-9926-3aa64a800f17" /># Enumeration
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

### Perform DNS Zone Transfer (AXFR)

**Command:**
```bash
dig @ns1.google.com google.com AXFR
```

**Output:**
<img width="950" height="292" alt="image" src="https://github.com/user-attachments/assets/46bf333a-c246-4340-b252-02dca2f21cc7" />


### Find Additional Names and Subdomains Using Google

**Search Query:**
```text
allinurl: -www site:google.com
```

**Output:**
```text
Search results containing indexed
names and subdomains of google.com.
```

### Step 3: Display DNSenum Tool Information

**Command:**
```bash
dnsenum --help
```

**Output:**
```text
dnsenum - DNS enumeration tool

Usage:
dnsenum [options] <domain>

Options:
--threads    Specify number of threads
--help       Display help information
```

### Step 4: Check DNS Enumeration Tool

**Command:**
```bash
which dnsenum
```

**Output:**
```text
/usr/bin/dnsenum
```

### Step 5: Check DNS Reconnaissance Information

**Command:**
```bash
dig google.com NS
```

**Output:**
```text
;; ANSWER SECTION:
google.com. IN NS ns1.google.com.
google.com. IN NS ns2.google.com.
google.com. IN NS ns3.google.com.
google.com. IN NS ns4.google.com.
```

### Step 6: Display Linux Usernames

**Command:**
```bash
head /etc/passwd
```

**Output:**
<img width="607" height="361" alt="image" src="https://github.com/user-attachments/assets/b623cab4-8c3e-4924-adfa-1db163675a90" />


### Step 7: Check SMTP User Enumeration Tool

**Command:**
```bash
which smtp-user-enum
```

**Output (if installed):**
```text
/usr/bin/smtp-user-enum
```

### Step 8: Display SMTP User Enumeration Help

**Command:**
```bash
smtp-user-enum -h
```

**Output:**
```text
SMTP User Enumeration Tool

Methods:
VRFY - Verify username
EXPN - Expand mailing list
RCPT - Check recipient
```

### Step 9: Check SMTP Port 25 Connectivity

**Command (authorized lab server):**
```bash
nc -vz <lab_IP_address> 25
```

**Output (if successful):**
<img width="890" height="135" alt="image" src="https://github.com/user-attachments/assets/f46dfa17-b175-4402-aa9a-3929cf69cf27" />


### Step 10: Connect to SMTP Using Telnet

**Command:**
```bash
telnet <lab_IP_address> 25
```

**Output (example):**
<img width="758" height="195" alt="image" src="https://github.com/user-attachments/assets/2f0f20fa-e07c-4e1a-9bea-b51fe5ca52d0" />


### Step 11: Execute SMTP EHLO Command

**Command (inside the Telnet session):**
```text
EHLO lab.example.local
```

**Output (example):**
```text
250-mail.example.local
250 HELP
```

### Step 12: Close SMTP Connection

**Command:**
```text
QUIT
```

**Output:**
```text
221 Bye
Connection closed by foreign host.
```

### Step 13: Check Nmap SMTP Enumeration Script

**Command:**
```bash
ls /usr/share/nmap/scripts/smtp-enum-users.nse
```

**Output (if installed):**
```text
/usr/share/nmap/scripts/smtp-enum-users.nse
```

### Step 14: Display Nmap SMTP Enumeration Script Information

**Command:**
```bash
nmap --script-help smtp-enum-users.nse
```

**Output:**
```text
smtp-enum-users

Attempts to enumerate users on an SMTP server
using VRFY, EXPN or RCPT TO commands.
```

### Step 15: Save IP Addresses in a File

**Command:**
```bash
dig +short A google.com > domain_ips.txt
```

**Display the file:**
```bash
cat domain_ips.txt
```

**Output:**
<img width="585" height="247" alt="image" src="https://github.com/user-attachments/assets/61ede321-4273-4cc8-b658-4750f70455d9" />



## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully

