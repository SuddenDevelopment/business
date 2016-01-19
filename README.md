1. *Hire a CISO* First things first. Hire someone that is dedicated to your information security and can spend the necessary time to walk through this process. A good competent CISO should be capable of all of the tasks here, just maybe not all at once. It will be a serial process until/unles there is more staff, but one person can go a long ways
1. basics like *virus protection* on endpoints, 
1. *prevent spam* from getting to user inboxes,
1. *user training* on "don't click on that url".
1. *Identify what is critical* and what is not, what is worth securing? Don't just focus on the perimeter, many things come from inside your network. Identfy user land separate from systems land
1. *Reduce the footprint of critical assets* If what is most valuable is spread out everywhere can you consolidate it so that you can focus on hardening a smaller area (For example access audit logs, tight controls)
1. *secure your most valuable area* internal firewall or whatever is appropriate, think at multiple layers. I cant tell you what is most valuable.
1. *get a  SIEM*, there are a few free ones: https://www.alienvault.com/solutions/siem-log-management, or you can roll your own, it's basically a log DB
1. *baseline your network*, through all that shit at the SIEM, look at it, what's normal, what's WTF, establish a baseline of what your network should look like.
1. *examine your activity* Identify what definitely should not happen on your network, they sections like user land and systems, infrastructure ips, outside in, inside out etc.
1. *Add alerts* scenarios to your SIEM
1. *open source scan* everything, these are the tools most commonly used by "bad actors" : http://www.openvas.org/ http://sqlmap.org/ http://buffer.github.io/thug/ analyze and resolve found issues
1. *Harden apps* programtically, do you stop brute force password attempts? Clean all vars, pay special attention to var length.
1. *Create secure bridges* you may consider more dedicated hardened access points / bridges. *BSD is common in this role. only open what's necessary. if you can set inclusive firewall rules instead of exclusive that would help
1. Now consider something like *Threat Intelligence* when you add a layer of threat intelligence to your SIEM you can add alert states / protections / actions like dont allow shit from TOR, or we have no business with russia and china.
1. Need to start getting fancy? Take an old box and set it up as a *honeypot*, pay special attention to its logs. Most effective honeypot looks just like what you are protecting, and actually works up to a point, just dead ends at certain depths. Name it like it's production etc. Anything connecting to it is very interesting.
1. *Outside assessment* by this point you know enough about your own stuff to give them the info they need to give you more than I mentioned above. You may be comfortable at this point to just keep moving on your own. Nothing is better than a decicated insider who knows your systems and is working to assess and iprove your security.