## High Level
1. read scope
2. light manual recon(root domain, robots, certs)
3. Subdomain enumeration
4. check live hosts
5. find URLS/endpoints
6. find parameters
7. test for vuln



### Tool breakout
1. Use the app as intended and learn features and get a baseline of what the applications has to offer.
2. Parameter Discovery
Initial tools
- Arjun https://github.com/s0md3v/Arjun
- ParamSpider https://github.com/devanshbatham/ParamSpider
- Param-Miner https://github.com/PortSwigger/param-miner
- 
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

