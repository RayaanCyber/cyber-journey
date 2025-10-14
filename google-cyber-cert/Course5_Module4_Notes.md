# Course 5 – Module 4: Threats to Asset Security

## Criminal Art of Persuasion

# Social Engineering: 
- manipulation technique that exploits human error to gain private info, access, or valuables

- Stages of Social Engineering: Prepare → Establish Trust → Persuasion Tactics → Disconnect from Target
- Preventing Social Engineering: implement managerial controls, stay informed on trends, share knowledge with others

# Common S.E Tactics

- Baiting: tempting people into compromising their security
- Phishing: using digital communication to trick people into revealing sensitive data or deploying malicious software
- Quid Pro Quo: tricking someone with promise of reward in return for data
- Tailgating: unauthorized person following an authorized person into a restricted area
- Watering-Hole: compromising a website frequently visited by specific group of people, infecting it with malicious software

## Phishing

- Phishing Kit: collection of software tools needed to launch phishing campaign
- Phishing Kit Tools: malicious attachment, fake data-collection forms, fraud web links

## Malicious Software

- Malware: software designed to harm devices or networks
- Worm: malware that can duplicate and spread itself across systems
- Trojan: malware that looks like legit file/program
- Ransomware: attackers encrypt organizations data and demand payment to restore access
- Spyware: used to gather/sell info without consent
- Cryptojacking: installs software to illegally mine cryptocurrency

- Intrusion Detection System (IDS): app that monitors system activity/alerts on possible intrusions

# Cross-Site Scripting (XSS)
- injection attack that inserts code into vulnerability 

- Reflected XSS Attack: malicious script sent to server/activated during server response
- Stored XSS Attack: malicious script injected directly on server
- DOM-based XSS Attack: malicious script exists in webpage when browser loads

## Preventing Injection Attacks

# SQL Injections (SQLi)
- attack that executes unexpected/malicious SQL queries on database
- Goal: modify, delete, or steal info from databases/gain unauthorized access to web apps

# Categories of SQLi 

- In-band: uses same communication channel to launch attack
- Out-of-band: uses different communication channel
- Inferential: attacker cannot directly see results

# Prevention Methods

- Prepared Statements: coding technique that executes SQL statements before user input passed to database
- Input Sanitization: removes user input which could be interpreted as code
- Input Validation: ensures user input


## Threat Modeling
- process of identifying assets, vulnerabilities, and exposure to threats

# Threat Modeling Process Cycle

1. Define scope
2. Identify threats
3. Characterize environment
4. Analyze threats
5. Mitigate risks
6. Evaluate findings

# Common Threat Modeling Frameworks

- STRIDE (Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege): 6 attack vectors
- PASTA (The Process for Attack Simulation and Threat Analysis): risk-centric process that aims to discover evidence of viable threats; 7 step process 
	1. Define business/security objections
	2. Define technical scope
	3. Decompose the application
	4. Perform a threat analysis
	5. Perform vulnerability analysis
	6. Conduct attack modeling
	7. Analyze risk/impact
- Trike: open-source methodology/tool with security-centric approach, focusing on security permissions, use cases, privilege models
- VAST (Visual, Agile, Simple Threat model): automated platform used to automate/streamline assessments


