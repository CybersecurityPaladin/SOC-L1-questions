# IDOR Attacks

<ins>**Classic (URL Tampering)**</ins> - Modify ID in request to access data  
**Detect** - Monitor sequential ID access, unusual resource enumeration  

<ins>**Parameter Manipulation (GET/POST)**</ins> - Change object ID in parameters  
**Detect** - Detect abnormal parameter changes, access to unauthorized objects 

<ins>**API IDOR (BOLA)**</ins> - Access other users data via API IDs  
**Detect** - Monitor API calls with changing object IDs, privilege anomalies  

<ins>**File Access IDOR**</ins> - Access files by modifying file paths  
**Detect** - Detect path manipulation, unauthorized file access patterns  

<ins>**Mass Enumeration IDOR**</ins> - Iterate IDs to dump large datasets  
**Detect** - High volume requests with incremental IDs  

<ins>**Horizontal Privilege Escalation**</ins> - Access same-level user data via ID  
**Detect** - Same role accessing multiple user resources  

<ins>**Vertical Privilege Escalation (IDOR)**</ins> - Access admin objects via ID change  
**Detect** - Low-priv user accessing high-priv endpoints  

<ins>**Indirect Object Reference Abuse**</ins> - Use predictable indirect references to access data  
**Detect** - Correlate indirect IDs with unauthorized resource access  