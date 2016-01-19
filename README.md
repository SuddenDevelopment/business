1. **Hire a CISO** First things first. Hire someone that is dedicated to your information security and can spend the necessary time to walk through this process. A good competent CISO should be capable of all of the tasks here, just maybe not all at once. It will be a serial process until/unles there is more staff, but one person can go a long ways
1. basics like **virus protection** on endpoints
- https://antivirus.comodo.com/
- http://ossec.github.io/
1. **Help with Binaries** Inevitably you'll run into situations where you are suspicious of files and you don't want to wait until antivirus sees it or misses it to find out if it's ok. In this siutation you can sandbox a file, or at least try to look it up:
- run your own sandbox: https://github.com/cuckoosandbox/cuckoo
- run on a hosted sandbox: malwr.com
- look it up http://virustotal.com
1. **prevent spam** from getting to user inboxes, if you use something like Gmail you should be pretty good already, if you run Excahnge you'll need to buy something.
1. **user training** on "don't click on that url". Phish your users, generate the URLs with something that lets you know who clicked on a URL for reporting. Then you know who needs a refresher course.
- HAve anyone REALLY interested in security? Send them here to learn to start thinking from an informed security perspective: http://captf.com/practice-ctf/	
1. **Developer training** start here:
- https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project
1. **Identify what is critical** and what is not, what is worth securing? Don't just focus on the perimeter, many things come from inside your network. Identfy user land separate from systems land
1. **Reduce the footprint of critical assets** If what is most valuable is spread out everywhere can you consolidate it so that you can focus on hardening a smaller area (For example access audit logs, tight controls)
1. **secure your most valuable area** internal firewall or whatever is appropriate, think at multiple layers. I cant tell you what is most valuable.
1. **get a  SIEM**, there are a few free ones, or you can write your own if you are proficient in large data stream handling
- https://www.alienvault.com/solutions/siem-log-management
1. **baseline your network**, throw everything at the SIEM, look at it, what's normal, what's unusual, establish a baseline of what your network should look like.
1. **examine your activity** Identify what definitely should not happen on your network, they sections like user land and systems, infrastructure ips, outside in, inside out etc.
1. Look into an IPS/IDS/PROXY base don your needs. they should be able to give you significant data into your SIEM to investigate. Keep in mind these will have false positives but it's good to have this data to start with and then start filtering.
- http://suricata-ids.org/
- https://www.bro.org/
- http://www.squid-cache.org/
- http://www.modsecurity.org/
- https://github.com/aol/moloch
1. **Add alerts** scenarios to your SIEM
1. **open source scan** everything 
- http://www.openvas.org/ 
- http://sqlmap.org/ 
- http://buffer.github.io/thug/ analyze and resolve found issues
- https://github.com/rapid7/metasploit-framework
1. **Harden apps** programtically, do you stop brute force password attempts? Clean all vars, pay special attention to var length.
1. **Create secure bridges** you may consider more dedicated hardened access points / bridges. *BSD is common in this role. only open what's necessary. if you can set inclusive firewall rules instead of exclusive that would help
1. Now consider something like **Threat Intelligence** when you add a layer of threat intelligence to your SIEM you can add alert states / protections / actions like dont allow traffic from TOR, or we have no business with russia and china.
- be careful with free crowd sourced threat feeds. They are often poisoned and they are very stale.
- Create you own batch feeds from services directly like the advertised TOR exit nodes, or lists from your own IDS/IPS and other systems
_ consider purchasing a GEOIP subscription like Maxmind
1. Need to start getting fancy? Take an old box and set it up as a **honeypot**, pay special attention to its logs. Most effective honeypot looks just like what you are protecting, and actually works up to a point, just dead ends at certain depths. Name it like it's production etc. Anything connecting to it is very interesting.
1. **Outside assessment** by this point you know enough about your own stuff to give them the info they need to give you more than I mentioned above. You may be comfortable at this point to just keep moving on your own. Nothing is better than a decicated insider who knows your systems and is working to assess and iprove your security.
1. For times when all else has failed you and you are in **Incident Response** mode
- http://www.sleuthkit.org/sleuthkit/