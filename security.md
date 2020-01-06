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
1. Remember that the security industry is built to sell products, which may or may not align with protecting you.
1. Products are compartmentalized into what's easily developed, packaged and deployed. Real threats dont follow the same dividing lines. If someone has any malicious intentions towards you, they will use everything they can to accomplish their goal and it's ALL related to the same threat. This relationship is rarely seen when multiple products are used from different security components.
1. No one will tell you what you DONT need, or that you are ever SAFE ENOUGH. You have to have a sober assessment of your own vulnerability and risk tolerance/liability for what you're protecting.
1. Most tools are great up to the 80% level very quickly getting you results in a POC to purchase. After that they get more difficult to tune to your needs, whcih becomes necessary.
1. Many of the tools will have an overwhelming amount of alerts you need to sift through internall or outside the tool, but hopefully automated. 
1. You have to be your own best advocate.

## Security Checklists
It's difficult to have a single checklist for security. It would assume a single perspective or approach. These checklists are meant to have a lot overlap but approach the problem from varying perspectives to catch distinct things. These lists are also good to check against an MSSP you hire. Any information gathered in this process will have a large overlap to what they need to know to properly serve you.

1. Discovery: Goals, Risk, Needs
2. Coverage: Assess coverage based on the OSI model
3. Best Practices: See what others do as popular solutions
4. Custom Applications: If you write your own software you need this list

## Discovery Checklist

1. What are your security goals? See the "Why you should care" section above for ideas
2. What are your known security risks?
3. What regulations do you need to legally comply with?
4. If something were wrong, how would you know? (per scenario)

## Security Coverage Checklist

1. Physical
	2. Access to employee systems
	3. Access to servers
	4. Access to network
	5. Access to sensitive paperwork
2. Network
	3. Physical, Ethernet ports
	4. Wifi
	5. Remote
	6. Segmentation
3. Transport
	4. Employee access to systems
	5. Customer access to systems
	6. Partner access to systems
4. Session
	5. Session timeouts
	6. Session portability
5. Application
	6. Operating System
	7. Business Applications
	8. Internal Applications
6. Data
	7. Business critical data
	8. Sensitive data
7. Employees
	8. Naive behavior
	9. Sloppy OpSec
	10. Malicious Intent
8. Partners
	9. Insecure partner
	10. Compromised partner
	11. Malicious partner
9. Outsiders
	10. Automated: Target of opportunity
	11. Targetted: Target of value

## Best Practices Checklist

These are some of the areas people consider for security specialty. They roughly align to products and in recommended priority order. The more you can check off with fewer products the better. 3 through 10 are considered so basic that it's recommended for the average home computer user. 1 & 2 are simply necessary to ensure they are happening.

0. **Designate Someone who is responsible for security**, preferably full time.
1. **Policy and Procedure**: Know what to do and communicate it.
1. **Endpoint Protection**: What used to be known as antivirus, with higher standards
2. **Multi Factor Authentication**: require this for all critical accounts for employees and customers
3. **Employee Awareness Training**: Make your employees harder to social engineer 
5. **Firewall**, Firewall management: the most basic network protection for all systems
6. **Patching**: stay up to date on all firmware, operating systems, applications, dependancies
7. **Identify what is critical**. Data & Systems
	8. Code repositories, proprietary information
	9. customer account information
	10. Accounting data
	11. Email & ticket systems
	12. File shares / document repositories
	13. internal system credentials / authentication
	14. All of the above in backups
8. **Reduce the critical attack surface**: The more consolidated critical systems and data are the easier it is to secure
9. Focus on **Securing what's most critical first**
10. **Vulnerability Scanning**: verify system patching against known vulnerabilities
11. **Employee Phishing**: Run some basic tests aginst your employees, give them remedial training based on the results
10. **Forensic capability**: If a system is compromised how do you know the scale and impact? How long will it take to understand
5. **Global Policy Management**: Enforce things like strong passwords on all systems
6. **Software management**: Make sure all systems stay up to date and free of prohibited software that is insecure or malicious
6. **Proxy / DNS / Content filtering**: Keep systems away from the riskiest content.
7. **SPAM Filtering**: Filter email before employees have a chance to be tricked by it.
8. **Identify Normal Behavior**
	9. Customers
	10. Employees
	11. Partners
8. **IDS/IPS**: Intrusion detection and prevention. Recognize and alert on suspicious network traffic 
9. **Holistic Monitoring**: Add your specific business context and expected behaviors into a monitoring app to understand what changes and add internal context to alerts.
10. **Context of external system**s, Threat Intelligence: External systems are hard to understand without some threat intelligence. This can help you understand if the suspicious traffic you are seeing is a compromised customer, or a state sponsored hacking group. You won;t know if it's actionable until you have the context for the decision.
11. **Threat Hunting**: Assume you are compromised, find the evidence
11. **Deception Technology**: This is pretty advanced level of sophistication and maturity for most. Setup honeypots whether they are on your network, in the cloud, in your users or in your application. Any traffic you see here is known to be malicious whether automated or targeted. This can help because it doesnt require filtering benign traffic.

## Custom Software Checklist

1. **Developer training**: All developers should know defensive coding tactics and how they apply to what they are developing.
2. **Harden applications**: Identify possible attack vectors on your software and block them from being effective.
	3. Clean variables
	4. Avoid Evals, implicit or otherwise
	4. Password and session requirements
	5. Least privilege access
	6. Zero trust development
	7. Remove Easy Recon
2. **Dependancy management**: Regularly scan dependancy libraries for known vulnerabilities
2. **Static Analysis**: Scan your code with language specific products that will look for insecure programming practices.
3. **Web Application Firewall**, aka Layer 7 firewall: 
4. **Pen Test** your software, whether internal or external, someone friendly needs to make an intelligent attempt at compromising your systems and report the findings.

## Other Lists

- https://github.com/sbilly/awesome-security
