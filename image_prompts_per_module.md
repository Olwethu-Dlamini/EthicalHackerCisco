# Image Concepts + Generation Prompts
# Cisco Ethical Hacking — LinkedIn Post Visuals

Each image is designed to TEACH something visually, not just look cool.
Use these prompts in Midjourney, DALL-E, Adobe Firefly, or Leonardo AI.

---

## POST 1 — Course Completion / The Five Stages

Concept:
A clean dark-background diagram showing the five stages of penetration testing
as a flowing cycle. Each stage labeled clearly. The visual should feel like something
you would see in a real security training manual.

Prompt:
"A dark-themed infographic diagram showing the five stages of penetration testing
as a circular flow: Reconnaissance, Scanning, Exploitation, Post-Exploitation,
Reporting. Each stage in its own node connected by arrows. Clean sans-serif labels.
Color scheme: dark navy background, cyan and white text, subtle green accents.
No people, no clipart. Flat design. Educational diagram style."

---

## POST 2 — Module 1: Hacker Types

Concept:
A side-by-side comparison chart showing White Hat, Black Hat, and Grey Hat hackers
with their defining characteristics listed under each. Looks like a reference card
a student would keep.

Prompt:
"A dark educational reference card divided into three columns. Left column labeled
White Hat Hacker with characteristics: authorized, legal, reports findings, works
for organizations. Middle column labeled Black Hat Hacker: unauthorized, malicious,
steals data, criminal. Right column labeled Grey Hat Hacker: no permission but no
malicious intent, legal grey area. Each column has a distinct color border: green,
red, yellow. Dark background, clean monospace font. Flat infographic style.
No cartoons, no faces."

---

## POST 3 — Module 2: Rules of Engagement

Concept:
A visual checklist or contract-style document showing what a penetration test
scope document looks like. Shows the key fields: authorized systems, testing window,
emergency contacts, methods allowed. Feels like a real professional document template.

Prompt:
"A dark-themed document template graphic showing a penetration testing scope
agreement. Fields visible: Target IP Ranges, Testing Window, Authorized Methods,
Out of Scope Systems, Emergency Contact, Client Signature. Clean structured layout
like a real form. Dark background with white text and cyan field labels.
Monospace font for field values. Professional and technical. No people.
Flat design infographic style."

---

## POST 4 — Module 3: Information Gathering Tools

Concept:
A tool comparison table showing Nmap, Whois, NSLookup, Shodan, Nessus, Nikto —
what each tool does, what phase it belongs to, and what kind of output it produces.
Looks like a study reference card.

Prompt:
"A dark educational cheat sheet table showing six reconnaissance and scanning tools.
Columns: Tool Name, Purpose, Type (Passive or Active), Example Output.
Rows: Nmap (port scanning, active, open ports and services), Whois (domain lookup,
passive, registrant info), NSLookup (DNS query, passive, IP and record data),
Shodan (internet device search, passive, exposed devices), Nessus (vulnerability scan,
active, CVE list), Nikto (web server scan, active, misconfigurations).
Dark navy background, cyan headers, white text, monospace font.
Clean flat table design. No illustrations."

---

## POST 5 — Module 4: Social Engineering Attack Types

Concept:
A visual attack map showing the four main social engineering methods with a one-line
description and the human vulnerability each one exploits. Feels like a threat
awareness poster.

Prompt:
"A dark security awareness infographic showing four social engineering attack types
arranged in a two by two grid. Each cell contains: attack name, one sentence
description, and the human weakness it exploits.
Top left: Phishing — fake emails stealing credentials — exploits trust.
Top right: Vishing — phone impersonation — exploits authority and urgency.
Bottom left: Tailgating — physical access by following — exploits politeness.
Bottom right: Pretexting — fake identity to gain trust — exploits helpfulness.
Dark background, red accent borders, white text, clean flat design.
No cartoons or clipart. Educational poster style."

---

## POST 6 — Module 5: How a Man-in-the-Middle Attack Works

Concept:
A network diagram showing two devices trying to communicate with an attacker
silently positioned in between intercepting and forwarding traffic. Labels explain
ARP poisoning step by step. This is the kind of diagram that makes the attack
click instantly for someone who never understood it.

Prompt:
"A dark network diagram showing a man-in-the-middle attack using ARP poisoning.
Three nodes: Victim Computer on the left, Router on the right, Attacker Laptop
in the center. Arrows show normal intended traffic path between victim and router.
Second set of red arrows shows actual traffic being redirected through the attacker.
Step labels: Step 1 Attacker sends forged ARP replies, Step 2 Victim maps attacker
MAC to router IP, Step 3 All traffic routes through attacker.
Dark background, cyan nodes, red attack arrows, white labels.
Clean technical diagram style. No people illustrations."

---

## POST 7 — Module 6: How SQL Injection Works

Concept:
A two-panel diagram. Left panel shows a normal login query. Right panel shows
the same field with a SQL injection payload and what the database actually
executes. The visual makes the vulnerability immediately understandable.

Prompt:
"A dark two-panel educational diagram explaining SQL injection.
Left panel labeled Normal Query: shows a login form input field with value john,
below it shows the SQL query the server runs: SELECT * FROM users WHERE username
equals john. Right panel labeled SQL Injection: shows input field containing
1 OR 1=1 UNION SELECT user password FROM users, below it shows the manipulated
query the server executes with the injection highlighted in red.
Below both panels a label reads: The database cannot tell the difference between
data and instructions. Dark background, green for normal, red for injected code,
monospace font for code. Clean flat educational diagram."

---

## POST 8 — Module 7: Cloud Misconfiguration Attack Surface

Concept:
A cloud architecture diagram showing common misconfiguration points labeled
as attack vectors. S3 bucket with public access arrow, IAM role with excessive
permissions, exposed API key in code, management console without MFA.
Looks like something from a cloud security audit.

Prompt:
"A dark cloud infrastructure diagram showing four common cloud misconfiguration
vulnerabilities as labeled attack vectors. Show a cloud architecture with:
a storage bucket labeled Public Access Enabled with a red arrow pointing to it
labeled Data Exposed, an IAM role labeled Overpermissioned with red label
Privilege Escalation Risk, a code block showing an API key hardcoded labeled
Credential Exposure, a management console login without MFA labeled
Unauthorized Access Risk.
Dark background, red warning labels, cyan infrastructure icons, white text.
Clean flat technical diagram style. No stock illustrations."

---

## POST 9 — Module 8: Post-Exploitation Flow

Concept:
A kill chain style diagram showing what an attacker does after initial access.
Four stages in sequence: Privilege Escalation, Persistence, Covering Tracks,
Data Exfiltration. Each stage shows the technique and example tool used.

Prompt:
"A dark horizontal kill chain diagram showing four post-exploitation stages
in sequence connected by arrows.
Stage 1 Privilege Escalation: technique SUID exploit or token impersonation,
tool LinPEAS.
Stage 2 Persistence: technique cron job or registry run key, tool Metasploit.
Stage 3 Covering Tracks: technique log deletion and timestomping, tool manual
or Meterpreter.
Stage 4 Data Exfiltration: technique DNS tunneling or HTTPS, tool custom scripts.
Each stage in a dark card with cyan title, white body text, red tool label.
Dark navy background. Clean flat infographic. No illustrations."

---

## POST 10 — Module 9: Anatomy of a Pentest Report

Concept:
A visual breakdown of what a professional penetration test report contains.
Each section shown as a labeled block with a one-line description of what goes inside.
Looks like a report template overview.

Prompt:
"A dark infographic showing the structure of a professional penetration testing report.
Vertical layout with five stacked sections as labeled blocks.
Block 1 Executive Summary: non-technical overview of findings and business risk.
Block 2 Technical Findings: each vulnerability with description, CVSS score,
proof of concept, and affected systems.
Block 3 Risk Ratings: Critical, High, Medium, Low, Informational severity levels
shown as colored labels.
Block 4 Remediation Guidance: specific developer and sysadmin action items.
Block 5 Appendix: raw tool output, scan data, methodology notes.
Dark background, each block a different shade of dark, cyan section titles,
white body text. Clean flat document diagram style."

---

## POST 11 — CTF Capstone: The Four Challenges

Concept:
A challenge board showing all four CTF challenges as cards: SQL Injection,
Web Server Recon, SMB Enumeration, PCAP Analysis. Each card shows the tool used
and a one-line summary of how it was solved. Looks like a CTF scoreboard.

Prompt:
"A dark Capture The Flag scoreboard style infographic showing four completed
challenges as cards arranged in a two by two grid.
Card 1 Challenge 1 SQL Injection: Tools used: DVWA, John the Ripper, SSH.
Method: UNION-based injection to dump password hashes then cracked with john.
Card 2 Challenge 2 Web Recon: Tool used: Nikto.
Method: Directory scan revealed exposed file with flag.
Card 3 Challenge 3 SMB Enumeration: Tools used: Nmap, enum4linux, smbclient.
Method: Anonymous share access to retrieve flag file.
Card 4 Challenge 4 PCAP Analysis: Tool used: Wireshark.
Method: HTTP traffic analysis to locate flag in XML file.
Each card has a green COMPLETED badge. Dark background, terminal green accents,
monospace font, clean flat design. CTF scoreboard aesthetic."

---

## POST 12 — Final Reflection: The Learning Roadmap

Concept:
A visual roadmap showing the ten modules as milestones on a path, with key
tools and frameworks labeled at each stop. Ends with a marker for what comes
next — CEH, home lab, OSCP. Looks like a learning journey map.

Prompt:
"A dark horizontal learning roadmap infographic showing ten milestones on a path
from left to right.
Milestone 1: Ethical Hacking Foundations — CVSS, hacker types.
Milestone 2: Planning and Scoping — Rules of Engagement.
Milestone 3: Recon and Scanning — Nmap, Shodan, Nessus.
Milestone 4: Social Engineering — Phishing, Pretexting.
Milestone 5: Network Attacks — Wireshark, MITM, ARP Poisoning.
Milestone 6: Web App Attacks — SQL Injection, XSS, Burp Suite.
Milestone 7: Cloud Mobile IoT — OWASP Mobile, Misconfigurations.
Milestone 8: Post-Exploitation — LinPEAS, Persistence, Exfiltration.
Milestone 9: Reporting — CVSS Scoring, Executive Summary.
Milestone 10: CTF Capstone — All tools combined.
Beyond the path a marker labeled What Is Next: CEH, OSCP, Home Lab.
Dark background, cyan milestone dots, white labels, subtle connecting line.
Clean flat infographic style. No illustrations."

---

Notes on which AI tool to use for each type:

For diagrams and charts (Posts 1, 2, 3, 4, 10, 12) use ChatGPT with DALL-E
or Adobe Firefly. They handle text in images better than Midjourney.

For attack flow diagrams (Posts 6, 7, 8, 9) use Leonardo AI or DALL-E.
Midjourney struggles with accurate text labels.

For the CTF scoreboard (Post 11) use DALL-E or Firefly.

If text in the generated image comes out wrong, regenerate and add the note:
"ensure all text labels are spelled correctly and legible" at the end of the prompt.
