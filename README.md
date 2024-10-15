# Automated Tool for Enumeration
<img src="https://github.com/jokerexe01/DeepScan/blob/main/DeepScan.png?raw=true" alt="DeepScan" width="500"/>

**This script automates the domain enumeration process, simplifying the task of discovering and analyzing subdomains, detecting live hosts, and extracting relevant URLs.**

- **Tool Availability Check:** Verifies that all necessary enumeration tools (subfinder, httpx, nuclei, wafw00f, katana) are installed. If any tools are missing, the script alerts the user to install them before proceeding.  
- **Subdomain Enumeration:** Utilizes subfinder to thoroughly enumerate subdomains for the target domain, including recursive search options, and saves the output in `subs.txt`.  
- **Live Host Detection:** Uses httpx to detect live subdomains by retrieving their HTTP status codes, titles, IP addresses, and CDN information. Results are saved in `live_host.txt`.  
- **Live Subdomain Filtering:** Filters and extracts only live subdomains from `live_host.txt` and saves them to `live_subs.txt` for further analysis.  
- **Vulnerability Scanning (Optional):** Sprays live subdomains with nuclei to identify vulnerabilities based on critical, high, and medium severity levels, and outputs results to `nuclei_results.txt`.  
- **WAF Detection:** Leverages wafw00f to detect the presence of Web Application Firewalls (WAFs) on live subdomains and stores the output in `waf_detection.txt`.  
- **403 Status Filtering:** Identifies subdomains returning a 403 Forbidden status from `live_host.txt` and lists them.  
- **URL Extraction:** Uses katana to extract URLs from the live subdomains for further investigation.  

## How to use
```bash
git clone https://github.com/jokerexe01/DeepScan.git
cd DeepScan
```
**Ensure the required tools (subfinder, httpx, nuclei, wafw00f, katana) are installed. The script will verify and prompt you to install any missing tools.**  
**After copying the DeepScan script into your /bin directory:**  
```bash
sudo cp deepscan /bin
```
**Now you can use this tool form any directory.**

**Happy Bug Hunting**
