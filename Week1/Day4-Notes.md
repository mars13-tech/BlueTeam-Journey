# Day 4 - Attack Frameworks Mastery

**Date:** Wednesday, February 12, 2026  
**Time:** 4 hours  
**Status:** ✅ Complete

## 🎯 What I Did Today

1. ✅ TryHackMe: "Pyramid of Pain" room (FREE)
2. ✅ MITRE ATT&CK study via attack.mitre.org (FREE official site)
3. ✅ Diamond Model via official paper + YouTube (FREE)
4. ✅ Cisco Module 3 progress
5. ✅ Created WannaCry attack analysis using ALL frameworks

## 📚 Frameworks Mastered

### 1. Pyramid of Pain

**The 6 Levels (Bottom → Top):**
                /\
               /  \
              / TTPs \
             /--------\
            /  Tools   \
           /------------\
          / Network/Host \
         /   Artifacts    \
        /------------------\
       /      Domains       \
      /----------------------\
     /     IP Addresses       \
    /--------------------------\
   /       Hash Values          \
  /------------------------------\
        
**Key Insight:**  
Focus on **TTP-based detection** (top of pyramid), not just signatures (bottom). TTPs are most painful for attackers to change.

**Example:**
- ❌ Bad: Block ransomware hash → Attacker recompiles (new hash)
- ✅ Good: Detect mass file encryption behavior → Catches ANY ransomware

---

### 2. MITRE ATT&CK Framework

**Source:** attack.mitre.org (official, free)

**The 14 Tactics:**

1. Reconnaissance
2. Resource Development
3. Initial Access
4. Execution
5. Persistence
6. Privilege Escalation
7. Defense Evasion
8. Credential Access
9. Discovery
10. Lateral Movement
11. Collection
12. Command & Control
13. Exfiltration
14. Impact

**Key Techniques I Studied:**

- **T1566.001:** Phishing - Spearphishing Attachment
- **T1003.001:** OS Credential Dumping - LSASS Memory
- **T1486:** Data Encrypted for Impact (Ransomware)
- **T1021.002:** Lateral Movement via SMB

**How SOC Uses ATT&CK:**
- Map SIEM rules to techniques
- Identify detection gaps
- Threat hunting playbooks
- Incident documentation

---

### 3. Diamond Model

**The 4 Points:**
             Adversary
                /\
               /  \
              /    \
     Capability ---- Infrastructure
              \    /
               \  /
                \/
              Victim

**Why It Matters:**
- **Pivoting:** Known infrastructure → Find other victims
- **Pattern Recognition:** Same capability + infrastructure = Same adversary
- **Threat Intel:** Structured incident documentation

---

## 💡 Framework Integration - WannaCry Example

**Scenario:** WannaCry ransomware attack (2017)

### Cyber Kill Chain:
1. Reconnaissance: Scan for SMB port 445
2. Exploitation: EternalBlue (MS17-010)
3. Installation: Ransomware payload
4. C2: Contact Tor payment sites
5. Actions: Encrypt files, display ransom

### MITRE ATT&CK:
- T1190: Exploit Public-Facing Application (SMB)
- T1021.002: Lateral Movement (SMB worm)
- T1486: Data Encrypted for Impact

### Diamond Model:
- **Adversary:** Unknown (possibly nation-state)
- **Capability:** EternalBlue exploit + WannaCry ransomware
- **Infrastructure:** Bitcoin wallets, Tor sites, kill switch domain
- **Victim:** 200K+ systems globally (unpatched Windows)

### Pyramid of Pain Defense:
- ❌ Blocking hash: Trivial (variants bypass)
- ❌ Blocking IPs: Simple (new IPs cheap)
- ✅ Detecting mass file encryption: PAINFUL (can't bypass without defeating ransomware purpose)

**Best Defense:** TTP-based detection catches WannaCry AND future ransomware variants!

---

## 🎯 Key Takeaways

1. **All frameworks work together:**
   - Kill Chain = WHEN (timeline)
   - ATT&CK = WHAT (specific techniques)
   - Diamond = WHO/WHY (context)
   - Pyramid = DEFENSE PRIORITY (focus on TTPs)

2. **Behavioral > Signature detection:**
   - Signatures are easy to bypass
   - Behaviors are painful to change

3. **Free resources are excellent:**
   - MITRE official site > premium courses
   - Learning to use primary sources = professional skill

4. **SOC analysts use these DAILY:**
   - Every job description mentions ATT&CK
   - Industry standard language
   - I can now speak it fluently!

---

## 📊 Progress Stats

- **Days:** 4/180 (2.2%)
- **TryHackMe Rooms:** 8
- **Frameworks Mastered:** 5 (Kill Chain, Unified, ATT&CK, Diamond, Pyramid)
- **Cisco:** 60% complete
- **Cost:** ₹0 (all free resources!)

---

## 🔥 Tomorrow: Day 5

Focus: Incident Response + Log Analysis fundamentals

---

**Framework foundation COMPLETE! Ready for hands-on technical skills.** 🛡️
