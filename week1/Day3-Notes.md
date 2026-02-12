# Day 3 - Cyber Kill Chain & Attack Frameworks

**Date:** Tuesday, February 11, 2026  
**Time Spent:** 4 hours  
**Status:** ✅ Complete

## 🎯 What I Accomplished Today
1. ✅ Completed TryHackMe "Cyber Kill Chain" room
2. ✅ Completed TryHackMe "Unified Kill Chain" room
3. ✅ Finished Cisco Module 2: Attacks, Concepts and Techniques
4. ✅ Explored MITRE ATT&CK framework
5. ✅ Mapped real ransomware attack to frameworks

## 📚 Key Learnings

### The Cyber Kill Chain (7 Stages)

**Created by:** Lockheed Martin (2011)

**The 7 Stages:**

1. **Reconnaissance**
   - **What:** Information gathering phase
   - **Attacker Actions:** Port scans, OSINT, social media research
   - **Blue Team Defense:** Minimize public footprint, monitor for scans
   - **Detection:** IDS/IPS alerts, honeypots

2. **Weaponization**
   - **What:** Creating the attack payload
   - **Attacker Actions:** Develop malware, craft exploits
   - **Blue Team Defense:** Threat intelligence feeds
   - **Detection:** Difficult (happens externally)

3. **Delivery**
   - **What:** Transmitting weapon to target
   - **Attacker Actions:** Phishing emails, malicious websites, USB drops
   - **Blue Team Defense:** Email filtering, web proxies, awareness training
   - **Detection:** Email gateways, proxy logs

4. **Exploitation**
   - **What:** Triggering the vulnerability
   - **Attacker Actions:** Execute exploit code
   - **Blue Team Defense:** Patch management, virtual patching
   - **Detection:** EDR, IPS signatures

5. **Installation**
   - **What:** Installing persistent access
   - **Attacker Actions:** Backdoors, rootkits, scheduled tasks
   - **Blue Team Defense:** Application whitelisting, EDR
   - **Detection:** File integrity monitoring, registry monitoring

6. **Command & Control (C2)**
   - **What:** Establishing remote connection
   - **Attacker Actions:** Beacon to external server
   - **Blue Team Defense:** Firewall rules, DNS filtering
   - **Detection:** Anomalous outbound traffic, C2 signatures

7. **Actions on Objectives**
   - **What:** Achieving attack goal
   - **Attacker Actions:** Data theft, ransomware, destruction
   - **Blue Team Defense:** DLP, backups, segmentation
   - **Detection:** Data exfiltration alerts, encryption activity

### The Unified Kill Chain (18 Phases)

**More comprehensive, modern framework**

**Cycle 1 - IN (Initial Foothold):** 7 phases
- Getting into the network
- Establishing presence
- Evading detection

**Cycle 2 - THROUGH (Network Propagation):** 6 phases
- Moving laterally
- Escalating privileges
- Expanding access

**Cycle 3 - OUT (Action on Objectives):** 5 phases
- Collecting data
- Exfiltrating information
- Causing impact

**Why it's better than original:**
- More detailed and realistic
- Covers lateral movement explicitly
- Addresses modern APT tactics
- Aligns with MITRE ATT&CK

### MITRE ATT&CK Framework

**What it is:**
- Real-world knowledge base of adversary tactics and techniques
- Based on actual observed attacks
- Used by SOCs worldwide for threat detection

**The 14 Tactics (Enterprise):**
1. Initial Access
2. Execution
3. Persistence
4. Privilege Escalation
5. Defense Evasion
6. Credential Access
7. Discovery
8. Lateral Movement
9. Collection
10. Command and Control
11. Exfiltration
12. Impact
13. Reconnaissance (new)
14. Resource Development (new)

**Example Techniques I Studied:**

**Tactic: Initial Access**
- T1566.001: Phishing - Spearphishing Attachment
- T1190: Exploit Public-Facing Application
- T1078: Valid Accounts

**Tactic: Persistence**
- T1547: Boot or Logon Autostart Execution
- T1053: Scheduled Task/Job
- T1136: Create Account

**How Blue Team Uses ATT&CK:**
- Map detections to specific techniques
- Identify coverage gaps
- Create detection rules
- Threat hunting hypotheses
- Incident response playbooks

### Cisco Module 2 - Attack Types

**Malware Types:**
1. **Virus:** Requires user action, spreads via files
2. **Worm:** Self-replicating, spreads automatically
3. **Trojan:** Disguised as legitimate software
4. **Ransomware:** Encrypts data, demands payment
5. **Spyware:** Secretly monitors user activity
6. **Rootkit:** Hides malware presence

**Common Attack Methods:**
- **Phishing:** Fraudulent emails to steal credentials
- **Social Engineering:** Manipulating people
- **DoS/DDoS:** Overwhelming system with traffic
- **MitM:** Intercepting communications
- **SQL Injection:** Attacking databases via input
- **XSS:** Injecting malicious scripts into websites

## 🎯 Practical Exercise: Ransomware Attack Mapping

**Scenario:** WannaCry-style ransomware attack

**Cyber Kill Chain Mapping:**
1. ✅ Reconnaissance: Scan for vulnerable SMB ports
2. ✅ Weaponization: EternalBlue exploit + ransomware
3. ✅ Delivery: Network propagation (worm behavior)
4. ✅ Exploitation: SMB vulnerability exploited
5. ✅ Installation: Ransomware installed
6. ✅ C2: Contact server for encryption key
7. ✅ Actions: Encrypt files, display ransom note

**MITRE ATT&CK Mapping:**
- Initial Access: T1190 (Exploit Public-Facing Application)
- Execution: T1106 (Native API)
- Lateral Movement: T1021.002 (SMB/Windows Admin Shares)
- Impact: T1486 (Data Encrypted for Impact)

**Blue Team Detection:**
- Network scans for SMB (port 445)
- Exploit attempt signatures
- Mass file modification activity
- C2 communication patterns
- Ransom note creation

**Blue Team Prevention:**
- Patch SMB vulnerabilities immediately
- Disable SMBv1 protocol
- Network segmentation
- Regular backups (offline)
- Email filtering and awareness training

## 💡 Critical Insights

**Why These Frameworks Matter for SOC Analysts:**

1. **Common Language:** Everyone in cybersecurity uses these frameworks
2. **Detection Strategy:** Know what to look for at each attack stage
3. **Defense in Depth:** Implement controls at multiple stages
4. **Incident Response:** Understand what happened and what's next
5. **Threat Hunting:** Proactively search for TTPs

**The Blue Team Mindset:**
- Think like the attacker to defend better
- Every attack stage is a detection opportunity
- Break the kill chain = stop the attack
- Earlier detection = less damage

**Connection to My 15 LPA Goal:**
SOC Analyst job descriptions ALWAYS mention:
- "Understanding of cyber kill chain" ✅
- "Knowledge of MITRE ATT&CK" ✅
- "Threat detection across attack lifecycle" ✅

**I'm building exactly what employers want!**

## 🛠️ Tools & Frameworks Used Today
- TryHackMe (learning platform)
- MITRE ATT&CK Matrix (attack.mitre.org)
- Cisco Networking Academy
- Kali Linux (for note-taking)

## 📊 Progress Stats
- **TryHackMe Rooms:** 4 total (2 today)
  - Intro to Cyber Security ✅
  - Intro to Defensive Security ✅
  - Cyber Kill Chain ✅
  - Unified Kill Chain ✅
- **Cisco Progress:** 40% (2/5 modules)
- **Frameworks Learned:** 3 (Kill Chain, Unified, ATT&CK)

## 🎯 How This Helps My Career

**Job Interview Scenario:**
*Interviewer: "How would you detect a ransomware attack?"*

**My Answer Now:**
"I'd implement detections across the kill chain:
- Email gateway: Block suspicious attachments (Delivery)
- EDR: Detect macro execution and suspicious processes (Exploitation/Installation)  
- Network monitoring: Identify C2 beaconing (Command & Control)
- SIEM: Correlate mass file encryption activity (Actions on Objectives)
- Using MITRE ATT&CK, I'd specifically look for T1566.001 (phishing), T1204 (user execution), and T1486 (data encryption for impact)"

**That's a 15 LPA answer!** 🎯

## 💪 Challenges Faced
- 18 phases in Unified Kill Chain felt overwhelming at first


## ✅ What Went Well
- Kill Chain concept makes perfect sense now
  
## 🎯 Tomorrow's Goals (Day 4)

**Day 4 Focus: MITRE ATT&CK Deep Dive & Diamond Model**
- Complete "MITRE ATT&CK" room on TryHackMe
- Complete "Diamond Model" room
- Cisco Module 3
- Create attack scenario mapping exercises
- Practice more Linux commands

## 🔥 Motivation Check

**Days Completed:** 3/180 (1.67%)  
**Streak:** 3 days 🔥  
**Feeling:** [Your feeling - Confident/Energized/Focused]

**Today's Big Win:**
"I now understand how attacks flow from start to finish. More importantly, I know WHERE and HOW to defend at each stage. This is exactly what SOC analysts do - detect attacks across the kill chain. I'm becoming a defender!" 🛡️

**Reminder to Self:**
Every day I'm building skills that most people only talk about. 177 days until my 15 LPA offer. Keep pushing! 💪

---

**Progress: 1.67% of journey complete (3/180 days)**

Next: Day 4 - MITRE ATT&CK Deep Dive & Diamond Model
