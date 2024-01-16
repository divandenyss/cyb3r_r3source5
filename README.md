# cyb3r_r3source5
This repo provides multiple blog posts that are cyber-specific, it equips Cyber soldiers to go into war with need-to-know knowledge. *For educational purposes only and should be used ethically.







# The Evil Syndicate of RaaS: Ransomware-as-a-Service
Ransomware as a service (RaaS) is an arrangement between an operator, who develops and maintains the tools to power extortion operations, and an affiliate, who deploys the ransomware payload. When the affiliate conducts a successful ransomware and extortion attack, both parties profit.

💡 Imagine if there were criminals who created an effective and tricky way to break into houses and steal valuable items. Instead of using this method themselves, they decided to sell the "burglary toolkit" to other criminals. These buyers, in turn, use the toolkit to break into houses, steal things, and make money. 

In this scenario:

⭐ The original criminals who created the toolkit are like the developers of ransomware.
⭐ The toolkit is the ransomware code.
⭐ The buyers are other hackers who want to use the ransomware to make money through cyber attacks.

👹 👺 We find ourselves in an era marked by the rise of sophisticated organized cybercrime, akin to a well-coordinated syndicate. Within this intricate network, various key players play recurring roles. Notably, there are initial access brokers who specialize in selling entry points to a company's internal network. This illicit trade facilitates Ransomware Affiliate groups in effortlessly infiltrating a company's private network, enabling them to engage in malicious activities with the primary goal of financial gain, often in the form of Bitcoin (BTC).
![RaaS](https://github.com/divandenyss/cyb3r_r3source5/assets/156643542/39e82ee9-55b1-4759-b1bf-670a855f7d06)









# The ticking time bomb: Remote Monitoring Management Software
For the most part, Remote Monitoring Management Software (hashtag#rmm ) is used by Managed Security Providers (hashtag#msps ) or IT teams to gain access to internal servers and perform tasks on them.
 
💣 👹 RMM can provide easy access for hashtag#threatactors to critical internal infrastructure, typically the notorious hashtag#ransomware operators. having multiple or even one misconfigured RMM leaves the house doors open at night in a criminal-infested town. It is a ticking time bomb for data theft, data encryption, or both that is double extortion.

 
💡 Most popular RMM in previous attacks: 

AnyDesk
Atera
ConnectWise
Netsupport
ScreenConnect
Splashtop
TeamViewer

🌟 Mitigation:

⭐ Use Windows Defender Application Control or AppLocker to create policies to block unapproved IT management tools.

⭐ Block connections to RMM software distribution sites via network blocking such as perimeter firewall rules if not in use in your environment.

⭐ For approved RMM systems used in your environment, enforce security settings where possible to implement MFA.

⭐ Consider searching for unapproved RMM software installations If an unapproved installation is discovered, reset passwords for accounts used to install the RMM services. If a System-level account was used to install the software, further investigation may be warranted.

⭐ Turn on the following attack surface reduction rule to block or audit activity associated with this threat:

⭐ Use advanced protection against ransomware
⭐ Block process creations originating from PsExec and WMI commands. Some organizations may experience compatibility issues with this rule on certain server systems but should deploy it to other systems to prevent hashtag#lateralmovement originating from hashtag#PsExec and hashtag#WMI.
![MoTW](https://github.com/divandenyss/cyb3r_r3source5/assets/156643542/57227935-c081-4c16-a7eb-cfa68422be2a)





# Adversary-in-the-Middle (AiTM) - Simplified
Background:

💡 Adversary-in-the-Middle (AiTM) is a phishing technique utilized by threat actors to seamlessly access victims' SaaS Applications, with a specific focus on Microsoft Exchange Online. AiTM attacks have resurfaced due to their effectiveness in stealing session tokens, enabling bypassing of Multi-Factor Authentication (MFA).

💣 💀 Threat Actor Perspective:

⭐ Download and employ "EvilGinx" (while other tools exist, EvilGinx boasts superior success and capabilities).
⭐ Craft a visually appealing "Phishlet" for dissemination to potential victims.
⭐ Distribute the enticing phishing emails.
⭐ Patiently await the successful obtaining of passwords and tokens 
⭐ Various covert activities occur behind the scenes, but for simplicity, let's keep it concise.

🤓 🤕 Victim Perspective:

⭐ Receive a phishing email and click on the link, often prompted by fear tactics or a seemingly legitimate source like the "IT Department" (numerous social engineering methods exist).
⭐ Redirected to a deceptively authentic Microsoft Login Page.
⭐ Obliviously enter the password and complete MFA.
⭐ Unbeknownst to the user, they've now fallen prey to AiTM attacks.

🕵‍♂️ Typical Alerts your trusted MSSP (Managed Security Service Provider) would see: 

⭐ Risky User Detected
⭐ A stolen session cookie was used
⭐ Connection to Adversary-in-the-Middle (AiTM) phishing site
⭐ Possible AiTM phishing attempt
⭐ Risky sign-in attempt after clicking a possible AiTM phishing URL
⭐ Suspicious Inbox Manipulation Rule
![EvilGinx](https://github.com/divandenyss/cyb3r_r3source5/assets/156643542/b08af3ce-e677-472b-8426-d9f1ac798587)
![AiTM-Login-Page](https://github.com/divandenyss/cyb3r_r3source5/assets/156643542/fcf27578-7b08-436d-9df0-9686a79ad0fa)
![AiTM-Defender](https://github.com/divandenyss/cyb3r_r3source5/assets/156643542/66ea066b-e92f-458a-bf14-1fe42913661d)



# Weaponizing Active Directory
Upon gaining initial access to an organization's internal network that utilizes Active Directory, the primary objective for threat actors, typically ransomware operators, is to attain domain dominance, enabling them to employ extortion tactics such as data exfiltration, data encryption, or both. As a defender, the initial questions should be how the attackers were able to abuse Active Directory and what the source of their entry was. “How did they get the opportunity” For instance, VPN often serves as a prime initial access method for threat actors.

💣 Typical Threat Actor Tactics (Active Directory): 
Various "tools" are available to facilitate the accomplishment of their ultimate goals in the following areas. 

💡 Reconnaissance/Enumeration (Getting a "Lay of the Land"):

⭐ IP Address
⭐ Server Names
⭐ Infrastructure (Operating System types, Domain Controller locations, and other critical servers)
⭐ Active Directory Misconfigurations (e.g., "Require Kerberos preauthentication", leaving it abusable to "AS-REP roasting")
⭐ And many more

💡 Lateral Movement:

⭐ Targeting critical servers housing data or Domain Controllers due to their sensitivity
⭐ Obtaining high privileges, often Domain Admin, for successful execution of their objectives, a tactic known as privilege escalation

🚨 The issue lies in the fact that most organizations lack regular Active Directory cleanups (Good AD Hygiene), leaving these opportunities open for threat actors to exploit. Defenders must conduct routine Active Directory checks. Tools such as "Purple Knight" and "Forest Druid" are effective for identifying and addressing potential lateral movement paths, multiple privileged accounts, etc. that threat actors can abuse. Defenders need to recognize that in most cases, it's not the "vulnerabilities" that are exploited, but rather misconfigurations in the system that are manipulated and abused.

🚨 A pivotal measure remains to get visibility on all transactions in the on-prem environment, Microsoft Defender for Identity remains a leader in aiding to this. 

![The-Cyber-Kill-Chain](https://github.com/divandenyss/cyb3r_r3source5/assets/156643542/3a15e106-b325-4bca-be06-1ad28cff7a4c)
![Breach-and-Attack](https://github.com/divandenyss/cyb3r_r3source5/assets/156643542/1632af20-b45b-4e95-ba0a-fe337a42fe9a)



# Honeytokens: A Deep Dive

Have you ever wondered about the intriguing world of Honeytokens? Let's take a look

🛡 What Exactly Are Honeytokens?

In essence, Honeytokens represent a clever ruse within the realm of Active Directory. If you're still utilizing Active Directory, Honeytokens become an indispensable tool in your cybersecurity arsenal.

🔎 The Ultimate Goal

🏖 Picture this:
Imagine you're at the beach, constructing a well-designed tunnel-like structure for the ocean waves to follow. Nature tends to favor the path of least resistance, and similarly, threat actors operate on this principle within compromised environments. They won't go for the most difficult route when pursuing their objectives, whether that entails data encryption or data exfiltration.

🛡 The primary objective of a Honeytoken is to masquerade as tempting bait, enticing threat actors to explore and ultimately breach the account. In a meticulously configured Security Operations Center (SOC), this triggers an alert and promptly notifies the Incident Response (IR) team, granting them the crucial window of time to mount a swift defense against the ongoing threat.

🛡 Characteristics of a Honeytoken Account

A well-crafted Honeytoken possesses distinctive traits that make it alluring to would-be attackers:

⭐ Alluring Alias: Honeytokens often adopt names like "Finance," "HR," or "IT Administrator" to pique the interest of threat actors.

⭐ Intentional Misconfiguration: Active Directory's "do not require Kerberos preauthentication" attribute is deliberately left checked, though there are various other misconfiguration methods, this one tends to yield significant success.

⭐ Domain Authority: Honeytokens are strategically endowed with high-level privileges, such as Domain Admin, Enterprise Admin, or membership in any other potent Active Directory group. Normally with the extension that this might be Service Account. 

Creating a Honeytoken Account

⭐ Robust Password: 50+ character generated password

⭐ Logon Restrictions: Eliminating logon hours is a smart move; even if a threat actor breaches the account, they'll find themselves unable to execute any actions within its context.

⭐ Never Expire Account: The account needs to lay dormant for the rest of time. 

🚨 Of course, it's vital to investigate how threat actors gained the opportunity to engage in enumeration within your environment in the first place. Identifying their initial access method and promptly sealing that initial access vector should always be a priority.

![Honeytoken2](https://github.com/divandenyss/cyb3r_r3source5/assets/156643542/a2a328a1-215a-4b81-b99d-42240a830b20)
![Honeytoken](https://github.com/divandenyss/cyb3r_r3source5/assets/156643542/3718d3ff-ceb6-466d-ab8d-9623bef01b49)
![Honeytoken Alert](https://github.com/divandenyss/cyb3r_r3source5/assets/156643542/db129814-2917-4516-91fd-e947cc2eb70f)



# What are Breach and Attack Simulations (BAS), and why are they vital for organizations?

In essence, Breach and Attack Simulations are real-world attack scenarios designed to assess the effectiveness of an organization's existing security measures.

Key Benefits:

💣 Implementing this proactive security approach yields substantial advantages for Managed Detection and Response Teams and SOC Analysts:

⭐Enhanced Alert Understanding:
 BAS allows Security Teams to visualize alerts from a portal perspective based on the simulated attack type. This equips them with crucial insights into current threats, aiding in incident response.

⭐Gap Identification: 
BAS helps uncover potential misconfigurations in current operational technology features used day-to-day. 

⭐Policy Enrichment through Automation:
 It enables automated responses to ongoing attacks within the environment, streamlining incident response and mitigation.

⭐Purple Teaming for MDR Teams:
 Combining Blue (Defense) and Red (Offensive) Team operations, Purple Teaming empowers security teams to both attack and defend their environment. This approach fosters a deeper understanding of threat actor TTPs (Tactic, Techniques and Procedures) and security technologies.

🔰 Regularly conducting Breach and Attack Simulation scenarios is essential to stay updated on modern threat actor tactics and continuous policy optimizations and enrichment. 

Breach and Attack Simulation Scenarios Include:

🎯 Emerging Modern-Day Threats 
🎯 Known Attack Paths Exploited by Threat Actors

🛡Incorporating BAS into your security strategy not only fortifies your defenses but also ensures preparedness against evolving cyber threats.
![Breach-and-Attack](https://github.com/divandenyss/cyb3r_r3source5/assets/156643542/46ff2e0d-b38b-445b-ba66-9604abbc10f4)


# The Ticking Time-Bomb: Single-Factor Authentication on VPN
🛡 A Virtual Private Network (VPN) stands as a cornerstone of an organization's daily operations, facilitating seamless access to the company's intranet and essential servers and applications. By default, this access relies on the traditional username and password authentication method.

🔰 Regrettably, this conventional approach has become a favored entry point for malicious threat actors seeking to infiltrate a company's intranet, either to exfiltrate data or launch notorious ransomware attacks.

So, what are the associated risks?

🔰 Simply put, if a threat actor manages to acquire identity credentials (username and password) through various social engineering techniques or exploits the vast and often overlooked dark web marketplace for credentials, they gain unhindered access to embark on their motive of complete domain dominance.

Crucial Countermeasures and Business Advantages:

🔰 Integrating Security Assertion Markup Language (SAML) with your VPN enables users to employ a single set of credentials for all access points. When your company leverages Entra ID as the Identity Provider (highly recommended), it empowers users to authenticate seamlessly through the Entra ID authentication flow. In a well-developed and optimized environment, this approach offers a multitude of benefits:

⭐ Multi-Factor Authentication (MFA) for VPN access.
⭐ Enhanced Identity Protection during the authentication process.
⭐ Conditional Access controls for authentication.
⭐ Continuous Access Evaluation throughout the user session.

💸 Furthermore, this approach also translates to cost savings for your business, as it simplifies integration with the Identity Provider, eliminating the need for tokens and associated expenses.

NEC XON strongly encourages companies to adopt a vigilant and proactive stance in fortifying these initial access points that modern adversaries exploit to safeguard their valuable assets.


# 🛡 Securing Against Lateral Movement and Identity Threats

In the ever-evolving landscape of cybersecurity, identities have emerged as the new perimeter. Threat actors leverage a technique called "lateral movement" to penetrate deeper into a company's infrastructure, seeking sensitive information and launching disruptive attacks. This presents a grave challenge to organizations.

💡 The Role of Credentials: 
To embark on lateral movement, threat actors must first acquire credentials. Social engineering, particularly through mechanisms like "phishing," "vishing," and the contemporary "smishing," is a common avenue for malicious actors to obtain these credentials.

Stages of Lateral Movement:

🔰 Reconnaissance (Information Gathering): 
During this stage, attackers meticulously observe, explore, and map the network, its users, and devices. This initial understanding is vital for their subsequent moves.

🔰 Privilege Escalation:
 Privilege escalation involves obtaining high-level credentials within the environment, often granting the actor substantial power, akin to that of an IT Administrator. Armed with these privileges, threat actors gain the freedom to traverse servers, with the ultimate aim of achieving domain dominance.

🔰 The Crucial Role of Credentials: 
It is imperative to understand that the success of threat actors largely hinges on their ability to acquire and exploit credentials. Without these credentials, they are severely restricted in their ability to carry out malicious activities within an organization.

Defenders' Guide:

⭐ Awareness Training: 
Implement regular and automated cybersecurity awareness training for all personnel. In a world where identities are the new perimeter, educating employees becomes paramount.

⭐ Credential Cycling: 
Regularly change passwords for user accounts and, whenever possible, for service accounts. This practice disrupts and prevents malicious activities that rely on stolen credentials.

⭐ Enforce MFA (Multi-Factor Authentication): 
MFA remains a potent defense mechanism against threat actors. Extend MFA to on-premises environments where feasible to further impede unauthorized access.

⭐ Healthy Network Segmentation: 
Ensure robust network segmentation, clearly separating production networks from non-production ones. This strategy prevents lateral movement between networks, effectively containing potential threats.

⭐ Active Directory Hygiene: 
Conduct routine on-premises cleanups, particularly within privileged groups, and remove dormant entities holding privileged roles. This proactive approach strengthens overall security posture.

![lateral-movement](https://github.com/divandenyss/cyb3r_r3source5/assets/156643542/45f3e42b-4f25-4e2b-a286-f2fcf2e04f73)
