# Kerberos Attacks

<ins>**Kerberoasting**</ins> - Extract service tickets for offline cracking.   
**Detect** - Monitor excessive TGS requests (4769), unusual SPN access  

<ins>**AS-REP Roasting**</ins> - Crack accounts without preauthentication enabled.   
**Detect** - Look for AS-REP requests without preauth (4768, 4771)  

<ins>**Pass-the-Ticket**</ins> - Reuse stolen Kerberos tickets.   
**Detect** - Detect ticket reuse across hosts, abnormal logon patterns  

<ins>**Golden Ticket**</ins> - Forge TGT using KRBTGT hash.   
**Detect** - Long-lived TGTs, abnormal domain admin activity, no DC logs  

<ins>**Silver Ticket**</ins> - Forge service ticket for specific service.   
**Detect** - Service access without DC validation, missing 4769 events  

<ins>**Overpass-the-Hash**</ins> - Use NTLM hash to get TGT.   
**Detect** - Logon type anomalies, NTLM usage followed by Kerberos  

<ins>**Skeleton Key**</ins> - Patch authentication to allow master password.   
**Detect** - LSASS memory anomalies, unusual authentication success  

<ins>**Kerberos Relay**</ins> - Relay tickets to authenticate elsewhere.   
**Detect** - Suspicious delegation use, unusual service ticket flows  

<ins>**Ticket Replay**</ins> - Reuse captured tickets within validity.   
**Detect** - Duplicate ticket usage, multiple logons from different hosts  