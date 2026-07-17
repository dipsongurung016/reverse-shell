# PHP Reverse Shell (Educational Demonstration)

## Overview

This project demonstrates the concept of a **PHP Reverse Shell** in a controlled laboratory environment. It was developed as part of a cybersecurity coursework assignment to understand how reverse shells operate, how attackers establish remote command execution, and how defenders can detect and mitigate such activity.

> **Disclaimer:** This project is intended **only for educational purposes** and must be used exclusively in environments where you have explicit authorization, such as virtual machines, CTFs, or penetration testing labs. Unauthorized use against systems you do not own or have permission to test is illegal and unethical.

---

## Learning Objectives

* Understand how a reverse shell establishes an outbound connection.
* Learn the basics of remote command execution.
* Observe reverse shell behavior from a defender's perspective.
* Practice identifying reverse shell activity using network monitoring and security tools.
* Gain experience documenting cybersecurity projects.

---

## How It Works

The PHP script performs the following actions:

1. Sets up the PHP execution environment.
2. Attempts to run as a background process (if supported).
3. Creates an outbound TCP connection to a predefined IP address and port.
4. Launches a system shell.
5. Relays input and output between the shell and the remote listener.
6. Maintains the session until either side closes the connection.

This demonstrates the basic workflow of a reverse shell commonly discussed in penetration testing and cybersecurity education.

---

## Project Structure

```text
.
├── reverse_shell.php
└── README.md
```

---

## Technologies Used

* PHP
* Linux
* TCP Networking
* Virtual Machines (Lab Environment)

---

## Lab Environment

This project was tested in an isolated virtual lab.

Example setup:

* **Attacker Machine:** Kali Linux
* **Target Machine:** Linux system with PHP
* **Network:** Private VirtualBox/VMware Internal Network
* **Purpose:** Educational demonstration only

---

## Educational Value

This project helps students understand:

* Reverse shell fundamentals
* Remote command execution concepts
* Network communication between client and listener
* Indicators of compromise (IOCs)
* Defensive monitoring and detection techniques

---

## Defensive Considerations

Security teams can detect reverse shell activity by monitoring for:

* Unexpected outbound network connections
* Web server processes spawning interactive shells
* Suspicious PHP script execution
* Unusual process creation events
* Network traffic to unknown internal or external hosts
* Endpoint Detection and Response (EDR) alerts
* SIEM correlation rules

Possible mitigations include:

* Disable unnecessary PHP functions.
* Apply the principle of least privilege.
* Restrict outbound network connections.
* Deploy EDR and IDS/IPS solutions.
* Monitor web server logs and process activity.
* Keep systems updated and patched.

---

## Skills Demonstrated

* PHP scripting
* Linux command line
* Network communication
* Cybersecurity lab setup
* Reverse shell concepts
* Security documentation
* Ethical hacking fundamentals

---

## Author

**Dipson Gurung**

---

## License

This repository is provided for **educational and research purposes only**. The author is not responsible for any misuse of the information or code contained in this repository.
