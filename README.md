# Cybersecurity SOC Analyst (L1) questions

<ins>**1: What are the key responsibilities of a SOC analyst?**</ins>  
Responsibilities include **monitoring** alerts, **investigating** potential threats, **conducting** vulnerability assessments and **IR**. 

<ins>**2: (VA) Vulnerability assessment**</ins>  
is the process of identifying security weaknesses in systems to determine their severity.

<ins>**3: How do you handle working with team members who have different opinions?**</ins>  
I **listen** actively to understand their perspectives, **share** my viewpoints clearly, and **look for** common ground. The goal is to **work towards** a solution that benefits the team.

<ins>**4: What if Someone Yelling**</ins>  
I would stay **professional**, **not respond** **emotionally**, and try to **de-escalate** the situation. If the behavior continues, I would **report** it according to company policy.

<ins>**5: What would you do if you detected a potential data breach?**</ins>    
First, I would **verify** the alert to confirm it’s not a false positive. Then, I’d **isolate** affected systems to contain the breach. Next, I’d **analyze** evidence to understand the scope of the breach. I’d **notify** the relevant stakeholders. Follow the IR plan to mitigate the threat. Finally, I’d **document** the incident to learn from the event.

<ins>**6: How do you document and report a security incident?**</ins>  
**Overview**: A brief summary of the incident.  
**Timeline**: Detailed chronology of events, from detection to resolution.  
**Impact Analysis**: Assessment of the incident’s effect on the organization.  
**Root Cause Analysis**: Identification of the underlying issues that led to the incident.  
**Response Actions**: Steps taken to contain, mitigate, and resolve the incident.  
**Lessons Learned**: Insights and recommendations to prevent future incidents.  

<ins>**7: CIA Triad**</ins>  
is a model that combines three cybersecurity principles.  
**Confidentiality** - means only authorized users can access data.  
**Integrity** - data is not modified without authorization.  
**Availability** - systems are accessible when needed.  

<ins>**8: VTER**</ins>  
**Vulnerability** - is a weakness in a system. 
Examples include outdated software, weak passwords, or missing MFA.  
**Threat** - is any things that can potentially cause harm to a system.
This can include attackers, malware, insiders, or automated bots.  
**Exploit** - is a method used to take advantage of a vulnerability.
This can include code, phishing, or brute-force attacks.  
**Risk** - is the potential impact of a threat exploiting a vulnerability.

<ins>**9: Windows Logs**</ins>  
are records of events that happen on computer  
[Logs here](Windows-Logs.md)

<ins>**10: (AAA) is a security framework**</ins>  
**Authentication** verifies the identity of a user. <ins>“Who are you?”</ins>

**Authorization** determines what actions the authenticated user is allowed to do. 
<ins>“What are you allowed to do?”</ins>

**Accounting** <ins>records user activity</ins> for monitoring.

<ins>**11: Subnet Mask**</ins>  
is a 32-bit number determines which part of an IP represents the network and which part represents the host.

IPv4 addresses contain 32 bits (4 octets).


Common subnet masks:  
/8 — 255.0.0.0 (≈16 million hosts)  
/16 — 255.255.0.0 (≈65k hosts)  
/24 — 255.255.255.0 (254 hosts)

<ins>**12: IP subnetting**</ins>  
is the process of dividing a larger network into smaller sub-networks to improve IP address management. 

<ins>**13: TCP & UDP**</ins>  
is a network protocol that provides communication between devices over a network.

**Transmission Control Protocol** - connection-oriented, reliable, guarantees delivery and packet order, slow.  
**User Datagram Protocol** - connectionless, order and delivery no guarantee, fast. 

<ins>**14: 3-Way Handshake**</ins>  
is a process for establishing a (full duplex) connection where both sides **SYN**chronize and **ACK**nowledge each other.   
🔹 Client SYN → Server SYN-ACK → Client ACK
Connection established.  
[Illustration](screenshots/3-way-handshake.PNG)

<ins>**15: Network port**</ins>  
is a numeric identifier (0-65535) managed by the OS to direct network traffic to service.  
[Ports here](Ports.md)

<ins>**16: DNS (Domain Name System)**</ins>   
is a protocol that translates domain names into IP addresses so computers can communicate with servers. 

<ins>**17: HTTP (Hypertext Transfer Protocol)**</ins>  
is an application-layer protocol used for communication between a client and a web server to transfer web resources.

**Response codes**  
1XX: Informational  
2XX: Success  
3XX: Redirection  
4XX: Client-Side Error  
5XX: Server-Side Error  

<ins>**18: HTTPS**</ins>  
is HTTP over TLS encryption.

<ins>**19: Transport Layer Security (TLS)**</ins>  
Is a security protocol that provides privacy(enceyption), integrity(hashing) and  authenication(certificates). SSL is older version of TLS. 

<ins>**20: Structured Query Language Injection**</ins>  
is an attack where inserts malicious SQL code into input fields to manipulate database queries.  
**In-Band** query is sent and a replied to over the same channel.  
**Inferential (Blind)** attacker infers information by observing application behavior via response differences or timing.  
**Out-Of-Band.** Query is communicated over a different channel (ex. via DNS).  
**Prevent:** Never concatenate user input into SQL. Validate input and disable detailed database errors.

<ins>**21: XSS**</ins>   
is a web vulnerability where an attacker injects malicious JavaScript into a website.  
**Stored XSS:**  Malicious input is stored on the server and executed whenever users access the affected page.  
**Reflected XSS:** Malicious input is sent in a request and immediately reflected in the response.   
**DOM-based:** client-side XSS where JavaScript inserts untrusted input into the DOM, leading to code execution.

<ins>**22: Cross-Site Request Forgery (CSRF)**</ins>  
is an attack that forces authenticated users to submit a request to a web application against their will.   
**Mitigation:** CSRF tokens, SameSite cookies, referer check.

<ins>**23: ioc / ioa**</ins>   
**Indicators of Compromise** - are forensic artifacts that show a system has **already** been compromised.

**Indicators of Attack** - are behavioral patterns that show an attack is **happening or in progress**. 

<ins>**24: FP/FN**</ins>  
**False Positive → no attack, alert+** (An alert that flags benign activity as malicious)  
**False Negative → no attack, alert-** (A real attack that is not detected)

<ins>**25: Malware**</ins>  
short for malicious software. It's intrusive software developed by cybercriminals. 

**Trojan** - disguised as legitimate software   
**Worm** - self-spreading   
**Ransomware** - encrypts files   
**Spyware** - collects user data   
**Backdoor** - remote access   
**Stealer** - steals credentials/cookies  
**Drainer** - steals cryptocurrency   
**Keylogger** - records keystrokes   
**Botnet** - infected host controlled  
**Downloader** - installs additional malware  
**Rootkit** - hides malware   

<ins>**26: How mw works**</ins>  
**Execution** - run malware  
[**Persistence**](Persistence-Malware.md) - stay on system  
**Command and Control** - communicate with attacker  
**Actions** - perform attack  
 

<ins>**27: Incident response**</ins>   
is the process of detecting, analyzing, and responding to security incidents.   
**Preparation** - readiness   
**Detection** - alert is triggered   
**Analysis** - investigate if it is a real incident   
**Containment** - limit the attack   
**Eradication** - remove the threat   
**Recovery** - restore systems

<ins>**28: Threat Hunting**</ins>   
is a proactive approach to threat detection that looks for signs of malicious activity. 

<ins>**29: Firewall**</ins>   
is a device that allows or blocks the network traffic according to the rules. 

<ins>**30: Types of firewall**</ins>   
**Network** - Placed at the network perimeter to protect the whole network.  
**Host-based** - Installed on individual PCs, laptops, or servers.

<ins>**31: Attack/Detect (Firewall)**</ins>     
➣ **Network**  
**HTTP tunneling** - web traffic disguise (inspect TLS patterns, check unusual User-Agent)  
**DNS tunneling** - data via DNS (monitor query length, detect high entropy domains)  
**Fragmentation attack** - is when an attacker splits malicious payload into multiple IP fragments to evade firewall, IPS/IDS inspection and bypass signature-based detection. (detect overlapping fragments, monitor abnormal fragmentation rates)

➣ **Exploitation**   
**SQL injection**   
**Command injection** - OS command execution (trace process trees, monitor parent-child anomalies)   
**Reverse shell** - outbound control (detect unusual outbound sessions, monitor rare destinations)   

➣ **Misc.**   
**Misconfiguration abuse** - is a security vulnerability caused by incorrect configuration.  
**Ddos** - overwhelming firewall or protected services
(rate limiting, SYN flood protection, anomaly detection) 

<ins>**32: Compliance**</ins>  
Following the set of standards authorized by an organization or government.

<ins>**33: MITRE ATT&CK®**</ins>  
is a knowledge base of adversary tactics and techniques based on real-world observations. 

<ins>**34:  Cyber Kill Chain**</ins>  
is a model by Lockheed Martin used to identify and prevent cyber attacks.  
   **Reconnaissance** - information gathering  
   **Weaponisation** - payload creation  
   **Delivery** - payload transmission  
   **Exploitation** - vulnerability exploitation  
   **Installation** - persistence establishment  
   **C2** - remote communication  
   **Actions on Objectives** - goal execution  

<ins>**35: Blue team tools**</ins>   
➣ **Firewall** (Cloudflare)   
➣ **IDS** (Intrusion Detection System) detect traffic   
➣ **IPS** (Intrusion Prevention System) block traffic    
➣ **WAF** (Web Application Firewall) (pfSense)  
➣ **HIDS** (Wazuh) Host IDS   
➣ **NIDS** (Zeek) Network IDS   

<ins>**36: (EDR) Endpoint detection & response**</ins>  
is a proactive technology that helps identify, respond to, and mitigate cyberthreats. (CrowdStrike, Microsoft Defender, SentinelOne). 

<ins>**37: What steps do you take when you identify a security incident?**</ins>  
First, you verify the incident to rule out false positives. Next, you contain the incident to prevent further damage. This might involve isolating affected systems. Then, you investigate to understand the scope and impact. Finally, you work on eradication, recovery, and documenting the incident for future reference.


<ins>**38: (SIEM) Security Information & Event Management**</ins>  
is a program that provides real-time event logging and monitoring.

<ins>**39: Zero Trust security concept**</ins>  
is a model that operates on the principle of   
"never trust, always verify."

<ins>**40: OSI model**</ins>   
📌Developed model then protocol.   
**7 - Application** [HTTP, FTP, DNS, SMTP, Telnet]  
Providing services and interfaces to applications  
⚔️ SQL injection, XSS

**6 - Presentation** [SSL, TLS, JPEG, UNICODE]  
Data encoding, encryption and compression  
⚔️weak encryption exploitation  

**5 - Session** [NFS, NetBIOS, PPTP]  
Establishing, maintaining, and synchr. sessions  
⚔️session hijacking

**4 - Transport** [TCP, UDP]  
E2e communication and data segmentation   
⚔️SYN flood (DoS), reconnaissance (nmap)

**3 - Network** [IP, ARP, ICMP, IPSec]    
Addressing and routing between networks     
⚔️ICMP flood (ping flood)

**2 - Data Link** [PPP, ATM, Ethernet]  
Reliable data transfer between adjacent nodes  
⚔️ARP spoofing

**1 - Physical** [Eth., USB, Bluetooth, IEEE802.11]  
Physical data transmission media   
⚔️ Rogue devi**ce**

<ins>**41: TCP/IP**</ins>  
📌Developed protocols then model  
1 - **Application** += Session + Presentation  
2 - **Transport**   
3 - **Internet** = OSI Network  
4 - **Link** = DataLink + Physical  

<ins>**42: (MAC) MEDIA ACCESS CONTROL**</ins>  
MAC is a 48-bit hexadecimal address assigned to a network interface. A device can have multiple MAC addresses, one for each network interface (wifi/ethernet/vpn). 

<ins>**43: Address Resolution Pr. (ARP)**</ins>  
is a protocol for mapping an IP address to a physical machine address (MAC address) that is recognized in the local network.

<ins>**44: Spoofing**</ins>  
is a type of attack designed to trick the user or system into thinking the hacker is a legitimate source with a valid request (Arp, Dns, email).       
**Detected by** monitoring inconsistencies in ARP tables, such as IP-to-MAC mapping changes  
**Mitigations:** Dynamic arp inspection

<ins>**45: Dynamic Host Configuration Protocol**</ins>  
is a network protocol used on Internet Protocol networks for automatically assigning IP addresses to devices connected to the network. 

<ins>**46: Internet Protocol (IP)**</ins>  
is a set of rules for routing and addressing packets of data. 

<ins>**47: KERBEROS**</ins>  
is a network authentication protocol that uses cryptography to authenticate users and services in a network environment.  
➣ [How KERBEROS works](screenshots/Kerberos.PNG)   
➣ [Kerebros Attacks](Kerberos-Attacks.md)

<ins>**48: Open Worldwide Application Security Project**</ins>  
is a standard awareness document for developers and web application security. ([OWASP](https://owasp.org/))

<ins>**49: (IDOR) Insecure Direct Object Reference**</ins>  
is a vulnerability caused by the lack of an authorization mechanism. When a user can change an id and access another user’s data.  
➣ [IDOR Attacks here](IDOR-Attacks.md)

<ins>**50: (RFI) Remote File Inclusion**</ins>  
is a vulnerability where an attacker can make the application include and execute a remote file from an external server by manipulating a file URL input.

<ins>**51: (LFI) Local File Inclusion**</ins>  
is a vulnerability where an attacker can make the application include and read local files on the server by manipulating file path input. 

<ins>**52: (WAF) Web Application Firewall**</ins>   
protect web application by filtering and monitoring HTTP traffic between a web application and the Internet.

<ins>**53: Encoding, Hashing, Encryption**</ins>  
**Encoding:** the process of converting data or information into a specific format (ASCII, URL) for efficiency.  
**Hashing:** the process of transforming any size of data into a unique, fixed-size string of characters using a hash function.   
**Encryption:** the process of converting readable information into an unreadable, scrambled format using cryptographic algorithms and keys

<ins>**54: Salted Hashes**</ins>  
is a cryptographic hash produced by applying a hash function to a password combined with a unique random value (salt). For generate different hash outputs.

<ins>**55: Static and dynamic malware analysis**</ins>  
**Static Analysis:** It is the approach of analyzing malicious software by reverse engineering methods without running them. by decompiling/disassembling  
**Dynamic Analysis:** It is the approach 
of analysing malicious software by running it.

<ins>**56: (CTI) Cyber Threat intelligence**</ins>  
is the process of collecting, analyzing, and applying data on cyber threats, adversaries, and attack methodologies.  
Platforms: [IBM X-Force Exchange](https://exchange.xforce.ibmcloud.com/),
[Cisco Talos](https://talosintelligence.com/),
[OTX AlienVault](https://otx.alienvault.com/). 

<ins>**57: (TAXII) Trusted Automated eXchange of Intelligence Information**</ins>  
defines how cyber threat information can be shared via services and message exchanges.

<ins>**58: Types of Threat Intelligence**</ins>  
➣ **Strategic** Threat Intelligence.  
➣ **Tactical** Threat Intelligence.  
➣ **Technical** Threat Intelligence.   
➣ **Operational** Threat Intelligence.  

<ins>**59: Linux Paths**</ins>  
/var/log/syslog - logs of the system

/var/log/messages
/var/log/audit/audit.log
/var/log/boot.log

/var/log/auth.log - authentication logs  
For All: grep "Session opened|Session closed"   
For SSHD: "Accepted|Failed"

~/kern.log - kernel messages  
~/dpkg.log - package manager  
~/.bash_history - history of the commands

/etc/passwd - list of users  
/etc/shadow - passwords. hashes: MD5, Blowfish, bcrypt , SHA-256, SHA-512.  

/etc/ssh/sshd_config — settings SSH  
~/.ssh/authorized_keys — authorised keys

<ins>**60: Microsoft Paths**</ins>    
Passwords. Hashes: LM hash, NT hash (NTLM hash), NTLMv1, NTLMv2, Kerberos AES128 key, Kerberos AES256 key, Kerberos RC4-HMAC key, MSCache (DCC), DPAPI master key, WDigest hash.   
Windows\System32\config\SAM  
Windows\System32\config\SYSTEM  
Windows\System32\lsass.exe  
Windows\NTDS\NTDS.dit  

Logs:  
C:\Windows\System32\winevt\Logs\

Viruses:  
 C:\Windows\Temp\
C:\Users\username\AppData\Local\Temp\

<ins>**61: Active Directory**</ins>  
is a service that manages information about user accounts in an organization.  
➣ [AD ATTACKS](AD-Attacks.md)


<ins>**62: Network/Internet/WWW**</ins>  
**Network** is a set of interconnected devices that exchange data.  
**Internet** is a global system of interconnected networks.  
**World Wide Web** is a system of interconnected public webpages accessible through the Internet. 

<ins>**63: What would you do if you see a suspicious PS commands? Which one are suspicious?**</ins>  
I would first analyze the PowerShell command to understand its intent, check the process context and parent process, validate if it’s malicious using logs and EDR, and if suspicious, I would contain the endpoint, collect evidence, and escalate to L2 or incident response.
➣ [Suspicious PowerShell commands](Suspicious-PS-commands.md)

<ins>**64: Phishing**</ins>  
is a form of social engineering where attackers deceive people into revealing sensitive information. 

<ins>**65: Network types**</ins>  
PAN - Personal Area Network  
Connects personal devices. Example: Bluetooth.  
WPAN - Wireless Personal Area Network  
Wireless subset of PAN. Example: ZigBee, UWB.  
**LAN** - Local Area Network  
Single building or site. High speed. Example: office Ethernet.  
**WLAN** - Wireless Local Area Network  
Wireless subset of LAN. Example: Wi-Fi.  
**VLAN** - Virtual Local Area Network. Logically segments a physical LAN into isolated broadcast domains.  
CAN - Campus Area Network  
Connects multiple LANs across a campus (university)  
MAN - Metropolitan Area Network  
Covers a city or large district. (municipal Wi-Fi)  
WAN - Wide Area Network  
Spans countries/continents. The Internet is the largest WAN.  
**GAN** - Global Area Network  
Covers the entire world. Essentially the Internet or a true global backbone.  
SAN - Storage Area Network  
High-speed network connecting storage devices to servers.   
**VPN** - Virtual Private Network  
Encrypted tunnel running over another network (LAN/WAN/Internet).


<ins>**66: Sniffer**</ins>  
tool that monitors, captures, and analyzes data flowing over a computer network

<ins>**67: Data transmission methods(layer 2)**</ins>  
**Unicast** - is one-to-one communication.   
**Broadcast** - is one-to-all within a local network.   
**Multicast** - is one-to-many where only subscribed hosts receive the traffic.

<ins>**68: Proxy**</ins>  
is a server that provides a gateway between users and the internet

<ins>**69: Why deleted data not deleted**</ins>  
Deleted data is not immediately erased; the operating system only removes file references while the actual data remains on the storage medium until it is overwritten or securely wiped.

<ins>**70: Advanced persistent threat (APT) group**</ins>  
is a stealthy threat, typically manipulated by a group. 

<ins>**71: SSH (Secure Shell)**</ins>  
is a network protocol that establishes encrypted connections between computers for secure remote access. 

<ins>**72: (CDN) Content delivery network**</ins>  
is a geographically distributed group of servers that caches content close to end users. 
(Cloud-flare)

<ins>**73: (MITM) Man-in-the-middle**</ins>    
when attacker places themself between two communicating parts. 

<ins>**74: (NAT) Network Address Translation**</ins>  
is a mechanism that translates private internal IP addresses into public IP addresses

<ins>**75: Port forwarding**</ins>  
is a method used in networking to allow external devices to connect to devices on a private network

<ins>**76: How to bypass BIOS password?**</ins>  
**PC:**  password can be cleared by resetting CMOS.   

**Laptop:**   
**1.** Master password - serial number on bios-pw (dell, hp, acer etc). via Error Code.   
**2.** Via jumper reset CMOS (old versions).  
**3.** Flashing. Combination of flashes. CH341A+SOIC8+1.8VAdapter

<ins>**77: BitLocker**</ins>  
Is a Windows security feature that protects your data by encrypting your drives

<ins>**78: Detect malicious activity around both SAM and passwd/shadow file?**</ins>  
**Windows:**  
➣ Request/attempt (Event ID 4656 / 4663)  
➣ LSASS (Sysmon Event ID 10)  
➣ Process Creation (4688 / Sysmon 1)  
➣ EDR alerts (credential dumping).   

**Linux:**  
➣ Auditd  
➣ Auth.log  
➣ FIM.   

<ins>**79: P0-P4**</ins>  
incidents represent severity levels, where P0 is critical (immediate response) and lower levels indicate decreasing impact and urgency.

<ins>**80: Authentication protocols**</ins>  
are standardized rules that define how a system verifies a user's identity and manages access to network.  
[List of protocols](Authentication-Protocols.md)

<ins>**81: Would you Encrypt and Compress or Compress and Encrypt?**</ins>  
You should compress first and then encrypt, because encryption produces high-entropy data that cannot be effectively compressed. If you compress after encryption, you lose compression efficiency entirely. 
In most secure communication pipelines like TLS, compression (if used at all) happens before encryption for exactly this reason

<ins>**82: (SLA) Service level agreement**</ins>  
is a contract between a service provider and a customer

<ins>**83: What would you do if you detected a phishing email?**</ins>  
If a user reports a phishing email, I would collect the email details, analyze indicators like sender, links, and attachments, check if other users received it, block malicious domains or URLs, and escalate if necessary. I would also ensure the user did not interact with the email and take remediation steps if they did.

<ins>**84: You discover user clicked links in phishing email, also shared credentials.**</ins>  
If a user clicked a phishing link and submitted credentials, I would immediately reset the password, revoke active sessions. Then I would check for suspicious logins and activity, isolate the endpoint if needed, block malicious indicators, and assess the scope across the environment. Finally, I would document and escalate if there are signs of compromise.

<ins>**85: SPM DKIM DMARC records are related to?**</ins>  
➣ **Sender Policy Framework** is an email authentication method that helps to identify the mail servers that are allowed to send email for a given domain.   
➣ **DomainKeys Identified Mail** is an email authentication method that uses a digital signature to let the receiver of an email know that the message was sent and authorized by the owner of a domain.   
➣ **Domain-based Message Authentication, Reporting & Conformance** is an email authentication policy and reporting protocol. 

<ins>**86: How can you determine if the email spam? What is the action taken to arrest the spread of same if you have to act?**</ins>  
I would analyze the email headers, sender reputation, links and attachments, and check authentication results like SPF, DKIM, and DMARC. If confirmed as spam or phishing, I would block the indicators, remove similar emails from other users’ inboxes, and update email security controls to prevent further spread.

<ins>**87: Make a playbook for case of BEC (Business Email Compromise)**</ins>  
**1. Trigger** - User report/Alert.   
**2. Triage** - Collect email || Check headers.  
**3. Containment** - Reset password || Revoke sessions.  
**4. Investigation** - Check logins || Mail rules.  
**5. Eradication** - Remove rules || Block domain.  
**6. Recovery** - Restore access || Monitor activity.  

<ins>**88: What is Process Injection? Name some methods**</ins>  
Process injection is an attack where the attacker copies and executes a code in the memory of a process.  
**1. DLL Injection** - Injecting a DLL into another process — often via CreateRemoteThread.  
**2. Process Hollowing** - A legitimate process is started → its memory is hollowed out → malware is loaded into it.  
**3. Reflective DLL Injection** - A DLL is loaded directly into memory without being written to disk.  
**4. Thread Injection** - Code injection by creating or modifying threads.  
**5. APC Injection** - Injection via the Asynchronous Procedure Call (APC) queue.  
**6. PE Injection** - Inserting an executable PE (Portable Executable) into a process's memory.  

<ins>**89: How would you classify a website as malicious?**</ins>  
**1. Reputation Check** - Check blacklist status.  
**2. Phishing Indicators** - Detect fake login.  
**3. URL Analysis** - Inspect URL structure.  
**4. Behavior Analysis** - Observe redirects.  
**5. TLS Validation** - Verify certificate.  
**6. Code Analysis** - Check obfuscated scripts.  
**7. SE Check**  - Identify manipulation tactics.  

<ins>**90: What is drive-by-downloads?**</ins>  
unintentional download of malicious code

<ins>**91: Can website with Green-Lock (SSL) be dangerous?**</ins>  
HTTPS only encrypts the connection but does not guarantee that the website itself is safe or trustworthy.

<ins>**92: You discover your infrastructure is under DDoS attack. What will be your resonse plan?**</ins>  
If I detect a DDoS attack, I would first confirm the attack, then mitigate it by filtering traffic, enable DDoS protection services, and coordinate with network and ISP teams. I would also monitor the impact, maintain service availability, and analyze logs for further action. 

<ins>**93: What are different DNS Records?**</ins>  
**DNS records** are text instructions stored on DNS servers. They indicate the IP address associated with a domain.  
**A** — IPv4 mapping.   
**AAAA** — IPv6 mapping.  
**CNAME** — Domain alias.  
**MX** — Mail routing.  
**TXT** — Text / verification.  
**NS** — Name servers.  
**SOA** — Zone authority info.  
**PTR** — Reverse lookup.  

<ins>**94: Application and OS are Vulnerable, which one will you priotize to fix and why?**</ins>  
I would prioritize fixing the operating system first, because it provides the foundation for all applications and has the highest impact if compromised.

<ins>**95: Can you do Network backet Analysis of HTTPS (SSL Enabled) traffic with Wireshark?**</ins>  
Yes, I can analyze metadata such as IPs, ports, TLS handshake, and certificates.
But I cannot see the encrypted payload unless I have access to the decryption keys. 

<ins>**96: What are the logs from a Linux machine you would pick for SIEM?**</ins>  
Auth Logs, Syslog, Messages, Audit Logs, Kernel Logs, Boot Logs 

<ins>**97: Credential Stuffing**</ins>  
Is an attack method in which attackers use lists of compromised user credentials to breach into a system.

<ins>**98: Credential Dumping**</ins>  
Extracting credentials (passwords or hashes) from a system, most often from the LSASS process (Local Security Authority Subsystem Service).
What is stored there: NTLM hashes, Kerberos tickets, sometimes plaintext passwords
Tools: mimikatz

<ins>**99: What happens when you open a website**</ins>  
➣ DNS resolves domain to IP address.  
➣ TCP connection is established (3-way handshake).  
➣ TLS handshake establishes encryption (HTTPS).  
➣ Browser sends HTTP request (encrypted if HTTPS).  
➣ Server returns HTTP response (encrypted if HTTPS).  
➣ Browser renders the content.   

<ins>**100: Port scanning**</ins>  
is a method of determining which ports on a network are open and could be receiving or sending data.

<ins>**101: DNS exfiltration**</ins>  
is a data exfiltration method in which an attacker uses DNS queries to covertly extract information from a compromised network.  
**To detect DNS exfiltration:**  
**1.** Monitor for unusually long and high-entropy domain names.  
**2.** identify high volumes of unique subdomain queries.  
**3.** analyse DNS query frequency and beaconing patterns.  
**4.** check for unusual DNS record types like TXT
