# **OpenWrt-vulnerabilities**

This project aims to create and publish Proof-of-Concept attack payloads for various vulnerabilities found in OpenWrt firmware. 

The intention of this project is to promote education and awareness. 

### **Get started**
You will need a virtulization software like VMWare or Virtualbox.  
Download the .ovf or .ova files and import to simulate OpenWrt router enviornment.  
Launch the Virtual machine and type `$ ifconfig`.  
Check the IP address of the VM. If you cannot see the IP, you can use the command `$ ifconfig br-lan`.  
Try to access the OpenWrt WebUI via a browser by accessing the OpenWrt IP.  
If you can access it as shown below, then you are good.  
<img src="https://raw.githubusercontent.com/paragmhatre1993/OpenWrt-vulnerabilities/master/images/ss1.png" width="740">

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
[https://owasp.org/www-community/xss-filter-evasion-cheatsheet](https://owasp.org/www-community/xss-filter-evasion-cheatsheet)  

4. Exploit the XSS vulnerability via CSRF to redirect a user to www.google.com


### **How to contribute**

I'm far from being an expert and this project can be expanded to include a lot of other vulnerabilities.  
Contributions are more than welcome!


### **Contact**

You can contact me on Twitter @paraaagggg or by email paragmhatre1993@gmail.com
