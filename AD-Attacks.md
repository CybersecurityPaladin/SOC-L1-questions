# The most popular AD attacks

<ins>**NTLM Attacks**</ins>  
**1. Pass-the-Hash** - Reuse stolen NTLM hash  
**2. NTLM Relay** - Relay authentication to another service  
**Detect** - Monitor NTLM usage, logon anomalies (4624), relay patterns, SMB/LDAP auth spikes  

<ins>**Kerberos Attacks**</ins>  
**3. Kerberoasting** - Extract service tickets for cracking  
**4. AS-REP Roasting** - Abuse accounts without preauth  
**5. Pass-the-Ticket** - Reuse stolen Kerberos tickets  
**6. Golden Ticket** - Forge TGT using KRBTGT  
**7. Silver Ticket** - Forge service ticket  
**Detect** - Monitor 4768/4769 anomalies, unusual TGS requests, ticket lifetime, lateral movement  

<ins>**Domain Controller Attacks**</ins>  
**8. DCSync Attack** - Abuse directory replication  
**9. DCShadow Attack** - Inject rogue replication changes  
**Detect** - Monitor replication events (4662), abnormal DC behavior, privileged account activity  

<ins>**Privilege Abuse**</ins>  
**10. ACL Abuse** - Escalate via permission changes  
**11. SeBackupPrivilege Abuse** - Dump sensitive files via backup rights  
**12. SeRestorePrivilege Abuse** - Modify system files via restore rights  
**13. SID History Injection** - Add privileged SID to account  
**14. Kerberos Delegation Abuse** - Impersonate users via delegation  
**Detect** - Monitor privilege use (4672), ACL changes (4670), abnormal group membership, delegation anomalies  