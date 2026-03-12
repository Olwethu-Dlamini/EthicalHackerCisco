# LinkedIn Posts — Cisco Ethical Hacking


---


POST 1 — Course Completion

I spent roughly 5 months on and off completing the Cisco Ethical Hacker course and I finally passed the final exam.

I want to be honest about what it actually took. This was not a weekend course. There were weeks I barely touched it, weeks I went hard, and moments I genuinely questioned whether I was cut out for this. But I kept coming back and I finished it.

Over 10 modules I went from learning what ethical hacking actually means to performing real penetration testing techniques hands on. The final assessment was a Capture The Flag challenge where I had to chain real techniques together — SQL injection, cracking password hashes, enumerating SMB shares, analyzing network traffic in Wireshark. No multiple choice. Actual work.

I'll be breaking down every module over the coming weeks so follow along if you're interested in what this field actually looks like from the inside.

#EthicalHacking #Cisco #CyberSecurity #PenetrationTesting #LearningInPublic


---


POST 2 — Module 1: What Ethical Hacking Actually Means

Before you touch a single tool, you need to understand what you're actually doing and why.

Module 1 cleared up a lot of misconceptions I had going in. Ethical hacking is not about finding ways to break things for fun. It's a structured, authorized process that helps organizations find their own security weaknesses before real attackers do.

The methodology follows five stages. First is reconnaissance, where you gather intelligence on a target without touching it directly. Second is scanning, where you actively probe systems to identify open ports and running services. Third is exploitation, where you attempt to leverage discovered vulnerabilities. Fourth is post-exploitation, where you assess how deep the damage could go once inside. Fifth is reporting, where you document everything with evidence and remediation guidance.

The course also covered hacker classifications. White hat hackers operate with full legal authorization. Black hat hackers operate without it and with malicious intent. Gray hat hackers fall somewhere in between and while they may not intend harm, operating without permission is still illegal regardless of intent.

That last point was emphasized heavily. No written authorization means no test. It does not matter how good your intentions are.

#EthicalHacking #PenTesting #Cisco #CyberSecurity


---


POST 3 — Module 2: Planning and Scoping

The most dangerous penetration tester is not the one with the most tools. It is the one who skips the planning phase.

Module 2 was entirely about how to set up an engagement properly before any technical work begins. The rules of engagement define exactly what is allowed, what methods can be used, which systems are in scope, and what happens if something goes wrong during the test.

Scope definition is critical. You produce a specific list of IP ranges, domains, and systems that are authorized for testing. Everything outside that list is off limits regardless of what you find or how tempting it looks. Crossing that boundary turns an ethical hacker into an unauthorized intruder legally.

Written authorization is not optional. It is the document that protects both the tester and the client. Without it you have no legal standing.

The module also covered setting testing windows to avoid disrupting live production systems and establishing emergency contacts in case something breaks unexpectedly during an assessment. In a real engagement, an untested system going offline because of your scan is a serious incident and it reflects on you professionally.

What I took from this module is that professionalism in this field is not separate from technical skill. It is part of the job.

#PenetrationTesting #EthicalHacking #Cisco #CyberSecurity


---


POST 4 — Module 3: Information Gathering

Before exploiting anything you need to know everything you can about the target. This phase is called reconnaissance and it is where a lot of the real work happens before a single exploit is launched.

I practiced with several tools during this module. Nmap is the industry standard port scanner. A basic service detection scan looks like nmap -sV -O followed by the target IP. The -sV flag identifies what version of a service is running on each open port. The -O flag attempts to fingerprint the operating system. What comes back tells you a lot about what you are dealing with.

Whois queries domain registration databases and returns information about who owns a domain, when it was registered, and what nameservers it uses. NSLookup and Dig are used to query DNS records. Mail servers, subdomains, and zone transfers can reveal significant details about an organization's infrastructure that they may not realize is public.

Shodan is worth mentioning separately because it changes how you think about exposure. It indexes internet-facing devices and their open ports continuously. Routers, cameras, industrial control systems, medical devices — if it is connected to the internet and has open ports, Shodan probably knows about it. Finding your own organization on Shodan before an attacker does is a very different experience than reading about it in theory.

After recon comes vulnerability scanning. Nessus and OpenVAS map discovered services against known CVEs, which are the publicly catalogued vulnerabilities maintained in the National Vulnerability Database. Nikto specializes in web servers and checks for outdated software, dangerous default files, and misconfigurations.

The distinction that matters: reconnaissance tells you what exists. Vulnerability scanning tells you what is broken.

#InformationGathering #Nmap #Shodan #Nessus #EthicalHacking #Cisco


---


POST 5 — Module 4: Social Engineering

I went into this course thinking hacking was mostly about code and terminals. Module 4 changed that.

Some of the most successful attacks never touch a single line of code. They target people. Social engineering is the practice of manipulating human behavior to gain access to information or systems, and it is responsible for a significant portion of real-world breaches.

Phishing is the most common form. Fraudulent emails are crafted to look legitimate and designed to steal credentials or deliver malware. Spear phishing is the targeted version where the attacker has researched the individual and personalizes the message to increase credibility. Vishing is the same concept over a phone call, often impersonating IT support or a bank with enough urgency to bypass critical thinking.

Tailgating is purely physical. An attacker follows an authorized person through a secured door without needing credentials of their own. Pretexting involves building an entirely fabricated backstory to establish trust before making a request that the target would otherwise refuse. Baiting exploits curiosity, often through infected USB drives left in parking lots or common areas.

MITRE ATT&CK, which is one of the most widely referenced frameworks in the industry, catalogs phishing as technique T1566 under Initial Access. Social engineering is not a soft skill category in cybersecurity. It is a documented, studied attack vector.

What changed for me after this module was how I respond to unexpected requests for information regardless of how legitimate they appear.

#SocialEngineering #Phishing #EthicalHacking #Cisco #CyberAwareness


---


POST 6 — Module 5: Network Attacks

This module is the reason you should treat public Wi-Fi as a hostile network.

The first tool I want to mention is Wireshark, a packet analyzer that captures raw network traffic and lets you inspect it in detail. On an unencrypted network you can read HTTP requests, session cookies, and in some cases credentials in plaintext. We used Wireshark directly in the final CTF to analyze a captured .pcap file and extract hidden data from HTTP traffic. It is one of the most important tools in this field and also one of the most legitimate — security teams use it daily for troubleshooting and incident investigation.

Ettercap is used to perform man-in-the-middle attacks through a technique called ARP poisoning. ARP stands for Address Resolution Protocol and it is how devices on a local network map IP addresses to MAC addresses. By sending forged ARP replies, an attacker can associate their own MAC address with a legitimate IP, causing traffic meant for another device to route through the attacker's machine instead. The two original hosts have no idea this is happening.

On the wireless side the module covered WEP cracking, which is almost academic at this point because WEP is a fundamentally broken protocol that should not exist on any modern network. WPA and WPA2 cracking through dictionary attacks and captured handshakes, rogue access points, and evil twin attacks were also covered. An evil twin is a fake access point with the same SSID as a legitimate one. Devices connect automatically. The attacker sees everything passing through.

One honest note: some of the wireless content in this module was dated. WPA3 and newer attack research were not covered. The fundamentals hold but the field has moved and you need to supplement with current resources.

#NetworkSecurity #Wireshark #EthicalHacking #Cisco #WiFiSecurity


---


POST 7 — Module 6: Web Application Vulnerabilities

Every input field on a website is a potential attack surface. That is not an exaggeration.

Module 6 focused on web application security and I practiced on DVWA, which stands for Damn Vulnerable Web Application. It is a deliberately insecure application built specifically for learning these techniques in a legal environment.

SQL injection is one of the most well-known vulnerabilities and still one of the most common in real-world breaches. It happens when user input is passed directly into a database query without being sanitized. In the CTF final I used a UNION-based injection payload to dump the entire users table from a database including password hashes. The payload told the database to ignore the original query and return different data entirely. From there I cracked the hash using John the Ripper.

Cross-site scripting, known as XSS, involves injecting malicious JavaScript into a web page that other users load. In the stored variant the script persists in the database and executes automatically for every visitor who loads the affected page. Command injection occurs when a web application passes user input directly to a system shell without sanitization. Typing a semicolon followed by a system command into a field designed for something else can return server-level output.

Broken authentication covers a range of issues including weak session tokens, missing account lockout policies, and password hashing with MD5, which is not a secure hashing algorithm and can be cracked rapidly with tools like John the Ripper or Hashcat.

Burp Suite was the primary tool throughout this module. It functions as an intercepting proxy sitting between your browser and the web server, allowing you to capture, inspect, and modify HTTP requests in real time before they reach their destination. It is used by professional penetration testers worldwide and was essential in every web challenge.

All of this maps directly to the OWASP Top 10, which is the industry-standard list of the most critical web application security risks updated regularly by the Open Web Application Security Project.

#WebSecurity #SQLInjection #BurpSuite #OWASP #EthicalHacking #Cisco


---


POST 8 — Module 7: Cloud, Mobile and IoT

The attack surface is not just servers in a data center anymore.

Module 7 covered three areas that define where security risk actually lives today. Cloud misconfigurations are consistently one of the top causes of major data breaches. S3 buckets left publicly accessible, overpermissioned IAM roles that give services far more access than they need, management consoles without multi-factor authentication, and API keys accidentally committed to public GitHub repositories — these are not exotic attack techniques. They are configuration mistakes that happen constantly.

The shared responsibility model is important to understand here. Cloud providers secure the underlying infrastructure. The customer is responsible for securing everything built on top of it. That line gets blurred often and the consequences are significant.

On mobile, the common vulnerabilities come from how apps are built rather than the devices themselves. Sensitive data stored unencrypted on the device, credentials hardcoded directly into the APK file, improper session handling, and unvalidated deep links are all in the OWASP Mobile Top 10.

IoT was the section that stuck with me most. Millions of devices including cameras, routers, smart appliances, and medical equipment ship with default credentials that most users never change. Many have no firmware update mechanism. Many transmit data unencrypted. Many are deployed with no network segmentation meaning a compromised smart bulb on the same network as a workstation is a legitimate lateral movement risk.

After this module I ran Nmap scans on my own home network to check what was exposed. I then looked some of my devices up on Shodan. I changed several settings that same day.

#CloudSecurity #IoTSecurity #MobileSecurity #EthicalHacking #Cisco


---


POST 9 — Module 8: Post-Exploitation

Getting into a system is chapter one. What happens next is where the real damage is done.

Post-exploitation is what attackers do after establishing an initial foothold, and understanding it is just as important for defenders as it is for offensive testers.

Privilege escalation is the process of moving from a low-privilege account to administrator or root. On Linux this often involves exploiting misconfigured SUID binaries or kernel vulnerabilities. On Windows common paths include unquoted service paths, weak registry permissions, and token impersonation. Tools like LinPEAS and WinPEAS automate the search for escalation opportunities on a compromised machine by checking hundreds of potential vectors in seconds.

Persistence is about surviving reboots and password changes. Attackers add SSH keys to authorized_keys files, create scheduled tasks or cron jobs, install web shells in web server directories, and modify registry run keys on Windows systems so their access is re-established automatically after a restart.

Covering tracks involves manipulating or deleting logs to remove evidence of activity. On Linux this means clearing files like /var/log/auth.log. On Windows it means wiping Event Logs. Timestomping modifies file timestamps to make forensic analysis harder. This is why log forwarding to an external SIEM matters so much in a real environment — if logs only exist on the compromised machine they can be erased by the attacker.

Data exfiltration is the final objective for many attackers. DNS tunneling hides stolen data inside DNS queries which are often less monitored than HTTP traffic. Steganography conceals data inside image files. Both techniques are designed to avoid triggering alerts in security monitoring tools.

#PostExploitation #EthicalHacking #RedTeam #Cisco #CyberSecurity


---


POST 10 — Module 9: Reporting

You can find a critical vulnerability in a system and it means nothing if nobody acts on it.

Module 9 was dedicated entirely to reporting and communication, which is the part of ethical hacking that most people skip over and the part that determines whether your work actually produces change.

A professional penetration test report has a specific structure. The executive summary is written for decision-makers, not engineers. It explains what was tested, what was found at a high level, and what the business risk is without requiring technical background to understand. This is often the only section a senior manager or board member reads, so it has to be clear and direct.

The technical findings section documents each vulnerability individually. Each finding includes a description of the vulnerability, a CVSS score which is a standardized 0 to 10 severity rating developed by FIRST, a proof of concept with screenshots or code showing the vulnerability is real and reproducible, the affected systems, and specific remediation steps that a developer or sysadmin can actually act on.

CVSS scoring deserves its own mention. A score of 9.8 is critical. A score of 4.0 is medium. The difference in urgency and resource allocation between those two is enormous and communicating that clearly to someone without a technical background is an actual skill that takes practice.

The best penetration test report is one where the development team reads it and immediately knows what to fix first without having to ask for clarification.

#Reporting #EthicalHacking #CVSS #PenetrationTesting #Cisco


---


POST 11 — The CTF Capstone

The final Capture The Flag assessment was where everything I learned had to work together. Four challenges, real tools, no guidance. Here is what I actually did.

The first challenge was SQL injection. The target was DVWA running on a local IP. I injected a UNION-based payload into the User ID field to dump the users table and pull password hashes. I then took Gordon Brown's MD5 hash and wrote it to a text file, ran John the Ripper against it with the raw-md5 format flag, and cracked it in seconds. From there I SSH'd into the target machine as that user and found the flag sitting in his home directory in a text file.

The second challenge was web server reconnaissance. I ran Nikto against the target and it flagged a directory with indexing enabled. Navigating to that path in the browser revealed a file containing the flag. One command, one finding, clean result.

The third challenge involved SMB share enumeration. I used Nmap to discover hosts on the subnet and identified a machine running SMB on port 445. Then I ran enum4linux against it to list the accessible shares and connected using smbclient. I navigated the share structure, found a file in a subdirectory, downloaded it, and read the flag with cat.

The fourth challenge was PCAP analysis. I opened a captured network traffic file in Wireshark, filtered the HTTP requests, and traced the traffic to a URL pointing to an XML file on one of the hosts. Inside that file the flag was embedded in a Signature field for a specific record.

What the CTF actually teaches you is that real penetration testing is about connecting pieces of information across tools. No single tool does everything. The skill is knowing what to reach for at each step and why.

Honest take: the course tools are solid but some of the documentation around certain modules was dated. Supplement with current resources, especially on the wireless side. The methodology though is timeless.

#CTF #EthicalHacking #SQLInjection #Wireshark #Nmap #Cisco #CaptureTheFlag


---


POST 12 — Final Reflection

I thought I would finish this course in a few weeks. It took me five months.

Life happened in between. There were stretches where I did not open the course for weeks. There were evenings I sat in front of a lab that was not working and could not figure out why. There were moments where I genuinely questioned whether this was the right path.

But I kept coming back and I finished it.

What surprised me most was the breadth. This course covers OSINT, social engineering, network attacks, web application vulnerabilities, cloud misconfigurations, IoT exposure, post-exploitation techniques, and professional reporting. It is not shallow on any of them.

Coming out the other side I have a working understanding of frameworks that the industry actually uses. OWASP Top 10 for web security. CVSS for vulnerability severity. MITRE ATT&CK for mapping attack techniques to real-world threat behavior. The five-stage penetration testing methodology that structures every professional engagement.

The tools I worked with are not beginner toys. Nmap, Burp Suite, Wireshark, John the Ripper, Nikto, Metasploit, enum4linux, smbclient — these are what professionals use.

Some of the course content was outdated, particularly around wireless attacks and certain tool documentation. That is worth knowing going in. Supplement as you go and build a home lab to practice outside of the course environment.

Five months, on and off, with everything else going on — and you can come out with a real foundation. If you are thinking about getting into this field, start. Do not wait until the timing is perfect because it never will be.

#EthicalHacking #Cisco #CyberSecurity #NeverStopLearning #LearningInPublic


---

Posting order: Start with Post 1. Then run the module posts in order every 2 to 3 days. Post 11 and 12 go last. That gives you about 5 weeks of content from one certification.
