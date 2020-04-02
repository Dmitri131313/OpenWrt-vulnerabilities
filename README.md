# **OpenWrt-vulnerabilities**

This project aims to create and publish Proof-of-Concept attack payloads for various vulnerabilities found in OpenWrt firmware. 

The intention of this project is to promote education and awareness. 


### **Vulnerabilities covered**



1. CVE-2019-17367 \
OpenWrt is vulnerable to multiple CSRF vulnerabilities. \
[https://nvd.nist.gov/vuln/detail/CVE-2019-17367](https://nvd.nist.gov/vuln/detail/CVE-2019-17367)
2. CVE-2019-18992 \
OpenWrt is vulnerable to multiple XSS vulnerabilities. \
[https://nvd.nist.gov/vuln/detail/CVE-2019-18992](https://nvd.nist.gov/vuln/detail/CVE-2019-18992) 



### **Exploits**



1. Insert a port forwarding rule in the OpenWrt firewall that forwards packets from LAN port 6879 towards the LAN port 22.  \
You have to exploit the CSRF vulnerability - CVE-2019-17367 to accomplish this task. \
A proof-of-concept CSRF form is available for reference - `exploits/csrf_forms/csrf.html`.
2. Change the name of WiFi SSID on OpenWrt to “Hacked”. \
You have to exploit the CSRF vulnerability - CVE-2019-17367 to accomplish this task. \
You can use the form from Exploit 1 for reference.
3. Find the exact fields where OpenWrt is vulnerable to XSS attacks and insert a payload to redirect a user to www.google.com  \
You can use the OWASP Filter Evasion cheat sheet to find the correct payload.  \
[https://owasp.org/www-community/xss-filter-evasion-cheatsheet](https://owasp.org/www-community/xss-filter-evasion-cheatsheet)  \

4. Exploit the XSS vulnerability via CSRF to redirect a user to www.google.com


### **How to contribute**

I'm far from being an expert and this project can be expanded to include a lot of other vulnerabilities.  \
Contributions are more than welcome!


### **Contact**

You can contact me on Twitter @paraaagggg or by email paragmhatre1993@gmail.com
