# Windows Logs

**All logs:**  
[eventvwr.msc](https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/)  
[Sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)


---

### The most popular from <ins>eventvwr.msc</ins>

<ins>**Authentication & Logon**</ins>  
**4624** — Successful logon.  
**4625** — Failed logon attempt.   
  **4634** — Logoff. 
  **4648** — Logon with explicit credentials.  
**4672** — Privileged logon.  
  **4768** — Kerberos TGT request.  
  **4769** — Kerberos service ticket request.  
  **4771** — Kerberos pre-authentication failed.  
  **4776** — NTLM authentication.  

<ins>**Account Management**</ins>  
**4720** — User account created.  
**4722** — User account enabled.  
**4723** — Password change attempt.  
  **4724** — Password reset.  
  **4725** — User account disabled.  
  **4726** — User account deleted.  
  **4738** — User account changed.  

<ins>**Group & Privilege Changes**</ins>  
**4728 / 4732 / 4756** — User added to a group.  
**4729 / 4733 / 4757** — User removed from a group.  
 **4735 / 4737** — Group modified.  
  **4670** — Permissions on an object changed.  

<ins>**Process Execution**</ins>  
  **4688** — Process creation (high-value event).  
  **4689** — Process termination.  

<ins>**System Events**</ins>  
  **4608** — Windows startup.  
  **4609** — System shutdown.  
  **4616** — System time changed.  

<ins>**Audit Policy Changes**</ins>  
  **4719** — Audit policy changed.  
  **4902 / 4904 / 4905** — Audit settings modified.  

<ins>**Remote Access / RDP**</ins>  
  **4778** — RDP session reconnected.  
  **4779** — RDP session disconnected.  

<ins>**Log Tampering (Critical)**</ins>  
  **1102** — Security log cleared.  

---

### The most popular from <ins>Sysmon</ins>

<ins>**Process & Execution**</ins>  
**1** — Process creation (command line, parent, hashes).  
  **5** — Process terminated.  

<ins>**Network Activity**</ins>  
**3** — Network connection (IP, port, process).  
  **22** — DNS query (domain resolution).  

<ins>**File & Image Activity**</ins>  
**7** — Image (DLL) loaded.  
  **11** — File created.  
  **15** — FileCreateStreamHash (Alternate Data Streams).  
  **2** — File creation time changed (timestomping).  

<ins>**Process Injection & Access**</ins>  
**8** — CreateRemoteThread (code injection).  
  **10** — Process access (e.g., LSASS access).  

<ins>**Registry & Persistence**</ins>  
**12** — Registry object created/deleted.  
  **13** — Registry value set.  
  **14** — Registry object renamed.  

<ins>**System & Drivers**</ins>  
**6** — Driver loaded.  
  **9** — RawAccessRead (direct disk access).  
  **16** — Sysmon configuration change.  

<ins>**Lateral Movement & IPC**</ins>  
**17** — Pipe created.  
  **18** — Pipe connected.  