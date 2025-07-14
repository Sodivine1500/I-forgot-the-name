**Objective**

The goal of this project was to build a safe, isolated environment for studying how malware operates, spreads, and can be analyzed. The virtual lab was designed to prevent infection outside the sandbox while providing a real-world environment to observe malware behavior.

**Lab Setup**

Virtualization Environment:

Installed VMware to create a secure and isolated virtual machine.

Ensured no network bridging or shared folders were active to keep malware contained.

Forensics Tools:

Installed FLARE VM on the virtual machine, which includes a comprehensive suite of malware analysis and reverse engineering tools.

Malware Samples:

Downloaded 15 high-severity malware samples from MalwareBazaar.

After downloading, the files were unzipped, triggering some of the malware to begin executing—initiating the analysis phase.

**Phase 1: Static Analysis**
Tools Used:
HxD (Hex Editor)

Notepad++

PEStudio

Actions:
Performed initial inspection of the binary data with HxD to understand file structure and embedded data.

Extracted SHA-256 hashes for 8 out of 15 malware samples initially and documented them in Notepad++ for tracking.

Used PEStudio to analyze the malware executables for suspicious behaviors or forced commands.

Key Observations:
Found several packed and unpacked SHA-256 hashes during string analysis.

Identified hardcoded or embedded strings that hinted at command-and-control mechanisms.

Found evidence of .exe files transforming into DLLs, which indicated behavior-masking or injection tactics.

**Phase 2: Dynamic Analysis**
Tools Used:
Process Explorer

Process Monitor

Wireshark

Actions:
Monitored process tree behavior and identified a malicious executable that converted into a DLL for stealth execution.

Traced activity back to a suspicious DLL:
C:\Windows\SysWOW64\msasn1.dll
This file was actively involved in brute-force activity, targeting security functions.

Used Wireshark to monitor network traffic and identified outbound communication to an external IP address.

**Key Findings:**
The IP address had a country code of 22 (Senegal), showing the malware was trying to communicate with an external server, likely for command and control (C2).

Observed brute-force behavior and attempts to persist or reinitiate on system boot.

**Final Observations**
Malware can activate upon file decompression, not just execution.

Malware often disguises itself by injecting into DLLs or altering process behavior.

Detected that some samples were configured to auto-run on startup, while others relied on process triggers.

Malware can operate in a multi-stage approach — stealthy initial access followed by aggressive actions (e.g., brute force or data exfiltration).

**What I Learned**
How malware functions: From initial infection to lateral movement and persistence mechanisms.

Analysis tools: Gained practical experience with HxD, PEStudio, Process Monitor, Wireshark, and others.

Speed and stealth: Malware can execute and act quickly and quietly, often evading detection unless thoroughly monitored.

**Conclusion**
This project gave me valuable hands-on experience in analyzing real malware samples in a controlled environment. I now have a deeper understanding of how malware behaves and how to use industry-standard tools to detect and monitor malicious activity.
