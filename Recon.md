## High Level
1. Read Scope & Understand Program Rules
- review engagment and bug bounty notes from target.
- Configure scope if applicable
- 
2. Light Manual Recon & root/seed domain discovery
- homepage
- robots.txt
- .well-known/
- TLS ceerts
- Tech Stack
- ANS enumeration
- Reverse WHOIS whoxy.com
- GOOGLE FU

3. Subdomain numeration - expand attack surface
- subfinder
- assetfinder
- amass

4. Check Live Hosts - refine attack surface
- httpx
- httprobe
- nmap (TCP scans)

5. Endpoint / URL Discovery
- waybackurls
- gau
- katana

6. Parameter Discovery
- paramspider
- arjun
- gf (with param patterns)

7. Authentication & Access Control Mapping
- Burp Suite
- jwt_tool
- Browser DevTools

8. Automated Vulnerability Scanning
- nuclei
- nikto
- wpscan(wordpress only)

9. Manual Vulnerability Testing

10. Exploition & Implact Validation (Prove severity safely)
- Burp Repeater
- curl
- postman (API testing)

11. Write Report & Submit




### Tool breakout
1. Use the app as intended and learn features and get a baseline of what the applications has to offer.
2. Parameter Discovery
Initial tools
- Arjun https://github.com/s0md3v/Arjun
- ParamSpider https://github.com/devanshbatham/ParamSpider
- Param-Miner https://github.com/PortSwigger/param-miner
- KATANA BURP EXTENSIONS WORKS ON COMMUNITY use that first
JavaScript Source Code Review(still searching for params)
- LinkFinder https://github.com/GerbenJavado/LinkFinder
- Run the JacaScript bookmarklets https://bsky.app/profile/renniepak.nl
- JSLinkFinder https://github.com/PortSwigger/js-link-finder
- GAP https://github.com/xnl-h4ck3r/GAP-Burp-Extension
- JSpector https://github.com/hisxo/JSpector

Vulnerability Checks on params
- XSS https://github.com/hahwul/dalfox

3. Fuzzing
- Forced Browsing
- ffuf https://github.com/ffuf/ffuf
- dirb https://github.com/v0re/dirb
- Path Fuzzing
- Parameter Fuzzing
- Header Fuzzing
- Burp Intruder


Word lists SECLISTS https://github.com/danielmiessler/SecLists/tree/master
- COMMON.txt https://github.com/danielmiessler/SecLists/blob/master/Discovery/Web-Content/common.txt
- COLDFUSION https://github.com/xmendez/wfuzz/blob/master/wordlist/vulns/coldfusion.txt
- generate your own wordlist https://github.com/digininja/CeWL

##Subdomain enumeration
used to find ll subdomains in scope.

1. passive subdomain enumeration
- http://web.archive.org/

2. Enumate subdomains using public databases
- https://censys.com/data-and-search
- https://www.shodan.io/
- https://securitytrails.com/
- https://github.com/projectdiscovery/subfinder built into https://projectdiscovery.io/
- https://github.com/owasp-amass/amass

3. Google Dorking
- site:*.domain.com

4. Active subdomain enumeration
- crawl, bruteforce, virtual host,fuzzing

5. Dont get WAF banned
- rate limit
- use rotating proxies
- adhere to robot.txt initially

6. DNS brute-forcing
- word list https://github.com/danielmiessler/SecLists
- word list https://github.com/trickest/mksub?tab=readme-ov-file
- https://github.com/OJ/gobuster


7. Virtual Host Fuzzing ## once you have domains
- gobuster
- https://github.com/ffuf/ffuf
- https://github.com/xmendez/wfuzz

8. Reverse DNS lookup
- https://github.com/projectdiscovery/dnsx

9. Crawling for subdomains
- https://portswigger.net/burp

10. HTTP probes ## test which domains are active
- https://github.com/projectdiscovery/httpx
- https://github.com/tomnomnom/httprobe

















Misc work flow
SEED DOMAINS

ANS ENUMERATION - find root/seed domains



Reverse Whois - whoxy.com  DOMlink



Ad/analytics relationships - built with .com(domain discovery



GOOGLE FU - Google cooy

IMG_2942.png



Shodan - web crawler FOR SEED DOMAINS



😀



SUBDOMAINS



Linked and JS discovery

Linked discovery & subdomain enumeration 

Burp suite pro
gospider 
Hakrawler
Subdomainizer (Subdomain enumeration)
Subscrapper
Subdomain scrapping ()
IMG_2944.png

Google subdomain subtraction site: domain -what you don’t want
Amass & subfinder
GitHub subdomain.py
Shosubgo 
Cloud ranges


Subdomain Bruteforcing

MassDNS
Amass
ShuffleDNS
Wordlist(
Alteration scanning(can do waf bypass)


PORT ANALYSIS

mass scan
Nmap
Dnmassscan


SEVICEScanning

brutespray
GitHub forking manual


Starting review of domains

manually view each one do I see hackable functionality 
Review subdomain takeover (can I take over xyz)

