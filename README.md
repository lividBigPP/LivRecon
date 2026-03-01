# LivRecon
 a comprehensive, multi-threaded reconnaissance framework for security professionals that automates the discovery of hidden infrastructure, origin servers behind CDNs, and security misconfigurations through passive DNS enumeration, certificate transparency logs, and intelligent IP scoring.
LEGAL DISCLAIMER: This tool is for authorized security testing and educational purposes only. Unauthorized scanning of systems you don't own or don't have explicit permission to test may be illegal. Always obtain proper authorization before use.

 Features
Core Capabilities
CDN/Origin Detection: Identifies Cloudflare, Akamai, Fastly, AWS, Azure, and other CDN infrastructure

Origin IP Discovery: Multiple techniques to find real origin servers behind CDNs

Passive DNS Enumeration: Queries multiple free sources (HackerTarget, AlienVault OTX, ThreatCrowd, RapidDNS)

Certificate Transparency: Extracts subdomains and IPs from crt.sh logs

CloudFail Technique: Tests hundreds of subdomains to find non-proxied origins

WAF Detection: Identifies Web Application Firewalls and security proxies

MX Record Analysis: Checks mail servers for origin IP leaks

Intelligence Gathering
DNS Records: A, AAAA, MX, NS, TXT, CNAME, SOA

SSL/TLS Analysis: Certificate details, expiration, SANs, issuer

WHOIS Information: Registrar, creation/expiration dates, organization

Port Scanning: 30+ common ports with service identification

Subdomain Enumeration: 100+ common subdomains with threading

Directory Busting: 90+ common paths with status code analysis

API Integrations (Optional)
Shodan: Open ports, CVEs, organization info, historical subdomains

VirusTotal: Malware flags, domain reputation, subdomains, historical DNS

IPinfo: Enhanced IP geolocation and classification

Smart Features
Origin IP Scoring: Ranks discovered IPs based on likelihood of being the real origin

Rate Limit Detection: Identifies WAF rate limiting to adjust scan speed

Auto Mode Selection: Recommends scan speed based on protection levels

Interactive Menu: User-friendly interface with multiple scan modes

 Installation
Prerequisites
Python 3.6 or higher

pip (Python package manager)

Step 1: Clone the Repository
bash
git clone https://github.com/lividbigpp/livrecon.git
cd recon-tool
Step 2: Install Dependencies
bash
pip install dnspython python-whois
Step 3: Make the Script Executable (Optional)
bash
chmod +x reconv6.py
🔧 Configuration
API Keys (Optional)
The tool works without API keys, but they add deeper intelligence. Set them as environment variable

Get Free API Keys
Shodan: https://account.shodan.io/register

VirusTotal: https://www.virustotal.com/gui/join-us

IPinfo: https://ipinfo.io/signup

Dependencies
Package	Purpose	Installation
dnspython	DNS record lookups	pip install dnspython
python-whois	WHOIS queries	pip install python-whois
All other modules are part of Python standard library.

Project Structure:

text
recon-tool/
├── reconv6.py          # Main script
├── README.md           # This file
├── LICENSE             # MIT License
└── .gitignore          # Git ignore file


Security Considerations:

No data storage: The tool doesn't save any results or API keys

API keys in memory only: Keys are never written to disk

Environment variables: Recommended method for API key storage

Rate limiting: Built-in delays to avoid overwhelming targets

Sources & Credits:

HackerTarget API: https://hackertarget.com/ip-address-lookup/

AlienVault OTX: https://otx.alienvault.com/

ThreatCrowd: https://www.threatcrowd.org/

RapidDNS: https://rapiddns.io/

crt.sh: https://crt.sh/

ipleak.net: https://ipleak.net/
