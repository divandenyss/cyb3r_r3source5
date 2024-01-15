# cyb3r_r3source5
This repo provides multiple blog posts that are cyber-specific, it equips Cyber soldiers to go into war with need-to-know knowledge.







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



