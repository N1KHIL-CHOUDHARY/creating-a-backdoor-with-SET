# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
<img width="380" height="71" alt="image" src="https://github.com/user-attachments/assets/7203d86c-057b-4176-a85e-addcf688a710" />

<img width="675" height="820" alt="image" src="https://github.com/user-attachments/assets/4d5037d9-fe5d-4338-89ac-1f8d843477e6" />

**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```

<img width="578" height="314" alt="image" src="https://github.com/user-attachments/assets/f0822c73-4bb4-463e-957e-d0f2a9bd4930" />
<img width="1700" height="472" alt="image" src="https://github.com/user-attachments/assets/d15cce51-7028-45dc-872e-0bcc3092fd2a" />


**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
<img width="1083" height="334" alt="image" src="https://github.com/user-attachments/assets/8e5c0e68-a601-49e9-a1cb-b7c6390b9de3" />

**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**

<img width="1154" height="375" alt="image" src="https://github.com/user-attachments/assets/198ef212-5cd4-42ce-8723-ada9b0def1d9" />


**6. Send the generated link to the victim.**

<img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/a2153e7a-b03d-400d-929a-7bf2e4a43d25" />


**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```

<img width="1567" height="466" alt="image" src="https://github.com/user-attachments/assets/d0be7299-2c68-40e2-bffa-9f8bf64bfaa0" />

<img width="379" height="286" alt="Screenshot 2025-09-30 112830" src="https://github.com/user-attachments/assets/ed481e39-812c-437b-b00b-ad1887f20a2c" />


## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
