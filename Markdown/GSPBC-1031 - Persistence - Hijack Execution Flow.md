##### CIRT Playbook Battle Card: **GSPBC-1031 - Persistence - Hijack Execution Flow**

**(P) Preparation**

1.  Patch asset vulnerabilities
2.  Perform routine inspections of controls/weapons
3.  Ensure antivirus/endpoint protection software is installed on workstations and laptops
4.  Conduct employee security awareness training
5.  Ensure all software is kept up to date
6.  Restrict the loading of remote DLLs \[1\]
7.  Restrict users to the least privileges required
8.  Confirm that servers and workstations are logging to a central location

**(I) Identification**

1.  Monitor for:  
    a. Moving, renaming, replacing, or modifying of DLLs  
    b. Applications loading DLLs not consistent with past behavior  
    c. DLLs that have the same file name but abnormal paths  
    d. Changes to environment variables  
    e. Unusual process activity  
    f. Suspicious modification or creation of .manifest and .local redirection files \[2\]
2.  Investigate and clear ALL alerts

**(C) Containment**

1.  Inventory (enumerate & assess)
2.  Detect | Deny | Disrupt | Degrade | Deceive | Destroy
3.  Observe -> Orient -> Decide -> Act
4.  Utilize EDR hunter/killer agents to terminate offending processes
5.  Remove the affected system from the network
6.  Determine the source and pathway of the attack
7.  Issue a perimeter enforcement for known threat actor locations

**(E) Eradication**

1.  Close the attack vector by applying the Preparation steps listed above
2.  Perform endpoint/AV scans on affected systems
3.  Reset any compromised passwords
4.  Inspect ALL assets and user activity for IOC consistent with the attack profile
5.  Inspect backups for IOC consistent with the attack profile PRIOR to system recovery
6.  Patch asset vulnerabilities

**(R) Recovery**

1.  Restore to the RPO within the RTO
2.  Assess and Address collateral damage
3.  Resolve any related security incidents
4.  Restore affected systems to their last clean backup

**(L) Lessons/Opportunities**

1.  Perform routine cyber hygiene due diligence
2.  Engage external cybersecurity-as-a-service providers and response professionals
3.  Implement policy changes to reduce future risk
4.  Utilize newly obtained threat signatures

**References:**

1.  MITRE ATT&CK Mitigation M1044: https://attack.mitre.org/mitigations/M1044/
2.  Dynamic-Link Library Redirection: https://docs.microsoft.com/en-us/windows/win32/dlls/dynamic-link-library-redirection?redirectedfrom=MSDN
3.  MITRE ATT&CK Technique T1574: https://attack.mitre.org/techniques/T1574/

**Resources:**

*    GuardSight GSVSOC Incident Response Plan: https://github.com/guardsight/gsvsoc\_cybersecurity-incident-response-plan
*    IT Disaster Recovery Planning: https://www.ready.gov/it-disaster-recovery-plan
*    Report Cybercrime: https://www.ic3.gov/Home/FAQ

![](data:image/png;base64,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)

  
© GuardSight, Inc.® | https://www.guardsight.com