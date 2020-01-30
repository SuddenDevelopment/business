DISCLAIMER: I have many years as a security professional. This information is freely given, not proprietary, and has no guarantees. I hope that you find it useful. suggestion for improvements are always welcome.

# Security Discussion Reference

## WHY YOU SHOULD CARE: 

1. If you have any **information** that can damage you or your customers you have an obligation to protect it. 
2. If you are **obligated by any regulations**
1. If you have any **online services and systems** that are critical to your operations.
1. If **public defacement** would damage your business
1. If **you have no idea** where you sit on all of the above. Ignorance isnt a great legal defense and worse brand protection.

## Security misconceptions

1. **Security is in layers**, don;t leave gaping holes because you expect something else to catch something. The best security is highly redundant in coverage of attacks
2. **Security through obscurity is a myth** Don't assume anything that requires special knowledge or is hidden or not advertised will not be attacked.
3. **Products alone won't protect you.** 

## A note about security products
* Remember that the security industry is built to sell products, which may or may not align with protecting you.
* Products are compartmentalized into what's easily developed, packaged and deployed. Real threats dont follow the same dividing lines. If someone has any malicious intentions towards you, they will use everything they can to accomplish their goal and it's ALL related to the same threat. This relationship is rarely seen when multiple products are used from different security components.
* No one will tell you what you DONT need, or that you are ever SAFE ENOUGH. You have to have a sober assessment of your own vulnerability and risk tolerance/liability for what you're protecting.
* Most tools are great up to the 80% level very quickly getting you results in a POC to purchase. After that they get more difficult to tune to your needs, whcih becomes necessary.
* Many of the tools will have an overwhelming amount of alerts you need to sift through internall or outside the tool, but hopefully automated. 
* You have to be your own best advocate.

## Security Checklists
It's difficult to have a single checklist for security. It would assume a single perspective or approach. These checklists are meant to have a lot overlap but approach the problem from varying perspectives to catch distinct things. These lists are also good to check against an MSSP you hire. Any information gathered in this process will have a large overlap to what they need to know to properly serve you.

1. Discovery: Goals, Risk, Needs
2. Coverage: Assess coverage based on the OSI model
3. Best Practices: See what others do as popular solutions
4. Custom Applications: If you write your own software you need this list

## Legend

:white_check_mark: Process
:wrench: Tool
:gear: configuration

## Discovery Checklist

1. What are your security goals? See the "Why you should care" section above for ideas
2. What are your known security risks?
3. What regulations do you need to legally comply with?
4. If something were wrong, how would you know? (per scenario)

## Security Coverage Checklist

1. Physical
	1. Access to employee systems
	1. Access to servers
	1. Access to network
	1. Access to sensitive paperwork
1. Network
	1. Physical, Ethernet ports
	1. Wifi
	1. Remote
	1. Segmentation
1. Transport
	1. Employee access to systems
	1. Customer access to systems
	1. Partner access to systems
1. Session
	1. Session timeouts
	1. Session portability
1. Application
	1. Operating System
	1. Business Applications
	1. Internal Applications
1. Data
	1. Business critical data
	1. Sensitive data
1. Employees
	1. Naive behavior
	1. Sloppy OpSec
	1. Malicious Intent
1. Partners
	1. Insecure partner
	1. Compromised partner
	1. Malicious partner
1. Outsiders
	1. Automated: Target of opportunity
	1. Targetted: Target of value

## Best Practices Checklist

These are some of the areas people consider for security specialty. They roughly align to products and in recommended priority order. The more you can check off with fewer products the better. 3 through 10 are considered so basic that it's recommended for the average home computer user. 1 & 2 are simply necessary to ensure they are happening.

1. **Designate Someone who is responsible for security**, :white_check_mark: preferably full time. 
1. **Policy and Procedure**: :white_check_mark: Know what to do and communicate it. 
1. **Endpoint Protection**: :wrench: What used to be known as antivirus, with higher standards 
1. **Multi Factor Authentication**: :gear: require this for all critical accounts for employees and customers
1. **Employee Awareness Training**: :white_check_mark: Make your employees harder to social engineer 
1. **Firewall** :wrench: , Firewall management :white_check_mark: :  the most basic network protection for all systems
1. **Patching**: :white_check_mark: stay up to date on all firmware, operating systems, applications, dependancies
1. **Identify what is critical**.:white_check_mark: Data & Systems
	1. Code repositories, proprietary information
	1. customer account information
	1. Accounting data
	1. Email & ticket systems
	1. File shares / document repositories
	1. internal system credentials / authentication
	1. All of the above in backups
1. **Reduce the critical attack surface**: :gear: The more consolidated critical systems and data are the easier it is to secure
	1. Consider offloading or tokenizing PII. If you dont need to keep it don't. If you have to keep it, protect it.
1. Focus on **Securing what's most critical first** :white_check_mark:
1. **Audit access** :white_check_mark: :wrench: to critical systems and data.
1. **Vulnerability Scanning**: :white_check_mark: verify system patching against known vulnerabilities
1. **Employee Phishing**: :white_check_mark: :wrench: Run some basic tests aginst your employees, give them remedial training based on the results
1. **Forensic capability**: :wrench: If a system is compromised how do you know the scale and impact? How long will it take to understand
1. **Global Policy Management**: :gear: Enforce things like strong passwords on all systems
1. **Software management**: :white_check_mark: Make sure all systems stay up to date and free of prohibited software that is insecure or malicious
1. **Proxy / DNS / Content filtering**: :wrench: Keep systems away from the riskiest content.
1. **SPAM Filtering**: :wrench: Filter email before employees have a chance to be tricked by it.
1. **Identify Normal Behavior** :white_check_mark:
	1. Customers
	1. Employees
	1. Partners
1. **Mobile Security** :white_check_mark: :wrench: A lot of business is done on personal phones and they are traditionally ignored in corporate security
1. **IDS/IPS**: :wrench: Intrusion detection and prevention. Recognize and alert on suspicious network traffic 
1. **Holistic Monitoring**: "wrench: :white_check_mark: Add your specific business context and expected behaviors into a monitoring app to understand what changes and add internal context to alerts.
1. **Context of external system**s, aka **Threat Intelligence**: :wrench: External systems are hard to understand without some threat intelligence. This can help you understand if the suspicious traffic you are seeing is a compromised customer, or a state sponsored hacking group. You won;t know if it's actionable until you have the context for the decision.
1. **Threat Hunting**: :white_check_mark: :wrench: Assume you are compromised, find the evidence
1. **Deception Technology**: :gear: :wrench: This is pretty advanced level of sophistication and maturity for most. Setup honeypots whether they are on your network, in the cloud, in your users or in your application. Any traffic you see here is known to be malicious whether automated or targeted. This can help because it doesnt require filtering benign traffic.

## Custom Software Checklist

1. **Developer training**: :white_check_mark: All developers should know defensive coding tactics and how they apply to what they are developing.
1. **Harden applications**: :gear: Identify possible attack vectors on your software and block them from being effective.
	1. Clean variables
	1. Avoid Evals, implicit or otherwise
	1. Password and session requirements
	1. Least privilege access
	1. Zero trust development
	1. Remove Easy Recon
1. **Dependancy management**: :gear: Regularly scan dependancy libraries for known vulnerabilities
1. **Static Analysis**: :wrench: Scan your code with language specific products that will look for insecure programming practices.
1. **Web Application Firewall** :wrench: aka Layer 7 firewall: 
1. **Pen Test** :wrench: :white_check_mark: your software, whether internal or external, someone friendly needs to make an intelligent attempt at compromising your systems and report the findings.

## Other Lists

- https://github.com/sbilly/awesome-security
