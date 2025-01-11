<p align="center">
<img src="https://citinewsroom.com/wp-content/uploads/2020/09/cvit-security.jpg" alt="Traffic Examination"/>
</p>

<h1>CompTIA Securtity+ Labs</h1>

<h2>Password Auditing</h2>

- ### [Auditing Passwords with a Password Cracking Utility](https://youtu.be/9Uf0wB-Atx4?si=AWNobhbLQ4vN_9k4)

## Role and Objective of the Lab

In this lab, you assume the role of a **Systems Administrator** tasked with demonstrating the critical risks associated with the use of weak and easily guessable passwords within an enterprise environment. The lab emphasizes the potential vulnerabilities that arise when password security policies are insufficient or not rigorously enforced, showcasing how these vulnerabilities can be exploited by threat actors.

### Key Activities

#### 1. **Password Cracking with John the Ripper**
The lab leveraged the powerful password-cracking tool **John the Ripper** to simulate a real-world scenario where a malicious actor, having already breached the perimeter of the organization’s network, begins reconnaissance activities. Specifically, the tool was used to:

- Identify and exploit weak or simple passwords stored in hashed formats.
- Demonstrate how password hashes, if improperly secured, can be cracked to gain further unauthorized access to critical systems.
- Illustrate how a compromised user account can act as a stepping stone for lateral movement within the network, escalating privileges and enabling deeper penetration into the infrastructure.

#### 2. **Social Engineering Techniques**
Another crucial component of this lab introduced the concept of **social engineering**, highlighting how human factors often represent the weakest link in an organization's security posture. The lab simulated scenarios where a threat actor employs social engineering tactics to:

- Manipulate employees into revealing sensitive information, such as personal details or operational practices, without realizing they are providing valuable intelligence to attackers.
- Showcase how questions phrased innocuously during conversations can lead individuals to inadvertently disclose data that aids attackers in crafting spear-phishing campaigns or conducting other targeted attacks.
- Highlight the role of awareness training and robust policies in mitigating the risks of social engineering attacks.

### Lab Goals and Lessons Learned

By simulating these scenarios, the lab provided insights into:
- The importance of implementing strong password policies, such as enforcing the use of complex passwords, regular rotations, and multi-factor authentication (MFA).
- The necessity of securing password storage mechanisms by employing techniques such as salting and using cryptographically secure hash algorithms.
- How security awareness training can empower employees to recognize and resist social engineering attempts, ultimately strengthening the overall security posture of the organization.
- The ways in which tools like **John the Ripper** can be utilized by administrators and penetration testers for defensive purposes, identifying and mitigating weaknesses before they can be exploited by malicious actors.

This lab underscores the critical importance of integrating technical safeguards, robust policies, and user education to build a resilient defense against both technical and human-centric attacks.

<h2>Scanning Network Nodes</h2>

- ### [Scanning Network Nodes](https://youtu.be/_gzjUoiMEAo?si=6JgT62g_E6OHMVRp)

## Network Reconnaissance and Analysis in the Lab

In this lab, the focus was on conducting network reconnaissance to identify devices, services, and vulnerabilities within a simulated environment. The primary goal was to understand the techniques used by both administrators and potential threat actors to gather critical information about a network's structure and its connected devices. The tools and methods employed highlight the importance of proactive monitoring and defense.

### Key Activities and Tools

#### 1. **Network Mapping with Nmap**
The lab made extensive use of **Nmap (Network Mapper)**, a powerful open-source tool for network discovery and security auditing. The activities included:

- **Device Identification:** Scanning the network to identify active hosts and determine their IP addresses and operating systems.
- **Port Scanning:** Enumerating open ports on each host to reveal potential entry points for further exploration or exploitation.
- **Service Detection:** Leveraging Nmap's service detection capabilities (`-sV` flag) to identify running services and their versions, providing insight into potential vulnerabilities.

This step illustrated how threat actors might use Nmap to map an organization's network and locate targets, while also demonstrating how administrators can use the same tool to identify and mitigate risks.

#### 2. **Banner Grabbing**
After identifying active hosts and their open ports, a **banner grabbing** exercise was performed to extract detailed information about the services running on the hosts. This involved:

- Capturing and analyzing service banners using tools like `telnet` or specific Nmap scripts.
- Revealing key information such as:
  - Service names and versions.
  - Potentially misconfigured services that expose sensitive information.
- Highlighting how outdated or improperly secured services could serve as entry points for attackers.

The banner grabbing exercise reinforced the importance of securing service configurations and limiting the information disclosed to unauthorized users.

#### 3. **DNS Information Gathering**
To further investigate the network, **DNS tools** were utilized for gathering name resolution and domain information. This step included:

- **Reverse DNS Lookups:** Mapping IP addresses to hostnames to better understand the naming structure of the network.
- **Zone Transfers (if applicable):** Attempting to identify misconfigured DNS servers that could leak the entire DNS zone data, exposing internal naming conventions and network layouts.
- **Hostname Enumeration:** Querying the DNS to identify additional hosts and services running within the network.

This phase of the lab highlighted the critical role of DNS in both operational functionality and potential reconnaissance activities.

---

### Lessons Learned

The lab provided insights into several critical aspects of network security and defense:

- **Visibility:** Tools like Nmap offer unparalleled visibility into network activity, helping administrators proactively identify vulnerabilities, but the same tools can be exploited by attackers if proper defenses are not in place.
- **Service Hardening:** Banner grabbing demonstrated the risks of exposing unnecessary information in service responses. Securing configurations and updating services to the latest versions can mitigate these risks.
- **DNS Security:** DNS, while a cornerstone of network communication, can be a weak point if misconfigured. Practices such as securing DNS servers and preventing unauthorized zone transfers are essential.

By employing these reconnaissance techniques, administrators can adopt a threat actor's perspective to identify and address vulnerabilities, improving the organization's overall security posture.

