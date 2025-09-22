## Tools Used
Nmap
Wireshark 

## Process Followed

1. I installed Nmap from the official website as instructed.
2.IP Range Discovery:** I identified my local network's IP address range, which was `$192.168.1.0/24$`, to define the scan target.
3.  Port Scan Execution: I performed a TCP SYN scan using the recommended Nmap command
    nmap -sS 192.168.1.0/24
4.  Results Analysis: I noted the IP addresses of discovered devices and the specific ports that were found to be open. I then researched the common services that operate on these ports to understand their function
5.  Documentation: The complete scan results were saved as a text file, which can be found in the `/scan_results` directory of this repository

| IP Address          | Open Ports             | Common Service              | Potential Security Risks                                                                    |
| ------------------- | ---------------------- | --------------------------- | ------------------------------------------------------------------------------------------- |
| `[e.g., 192.168.1.1]`   | `80 (http)`, `443 (https)` | Router Web Interface        | An open HTTP port could allow for unencrypted credential capture.                           |
| `[e.g., 192.168.1.10]`  | `445 (microsoft-ds)`   | Windows File Sharing (SMB)  | Could be vulnerable to exploits if not patched; weak passwords could allow unauthorized access. |
| `[e.g., 192.168.1.15]`  | `22 (ssh)`             | Secure Shell                | Susceptible to brute-force attacks if password authentication is weak.                      |

