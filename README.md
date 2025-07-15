# Understanding VPNs for Privacy and Secure Communication

## Introduction

Virtual Private Networks (VPNs) are essential tools for enhancing online privacy and security. They create an encrypted tunnel for your internet traffic, masking your IP address and protecting your data from various threats. This report outlines a hands-on experience using a free VPN service, ProtonVPN, to demonstrate its functionality and explore its benefits and limitations.

## VPN Setup and Connection

### 1. Choose a Reputable Free VPN Service and Sign Up

ProtonVPN was chosen due to its strong privacy features and a robust free tier. The signup process was straightforward, involving creating an account on their website. The free tier offers access to servers in five countries and allows the connection of one device at a time [1].

### 2. Download and Install the VPN Client

While ProtonVPN offers dedicated clients, this exercise used OpenVPN configuration files for manual setup on Kali Linux. The `openvpn` package was already installed on the system [2].

### 3. Connect to a VPN Server

OpenVPN configuration files were downloaded from the ProtonVPN website. The 'GNU/Linux' platform and 'UDP' protocol were selected. A free server configuration file was chosen—specifically, `jp-free-2.protonvpn.udp`. The connection was successfully established using the imported config [3].

### 4. Verify Your IP Address Has Changed

Before connecting to the VPN, a speed test showed the location as New Delhi, India. After connecting, `whatismyipaddress.com` displayed the IP as `37.19.205.196` with the location listed as Tokyo, Japan, confirming a successful VPN tunnel [4]. The site also noted, "Looks like you're using a VPN!"

### 5. Browse a Website to Confirm Traffic is Encrypted

Browsing various websites revealed no connectivity issues, confirming that traffic was routed through the encrypted tunnel. Although the browser lock icon (HTTPS) does not directly relate to the VPN, the new IP and browsing functionality confirmed the VPN's encrypted operation.

### 6. Disconnect VPN and Compare Speed and IP

After disconnecting, another speed test was conducted. A comparison is shown below:

| Test Condition         | Download (Mbps) | Upload (Mbps) | Latency (ms) | Server Location     |
|------------------------|-----------------|----------------|---------------|----------------------|
| Without VPN            | 77.2            | 26.3           | 42            | New Delhi, India     |
| With VPN (Tokyo)       | 76.7            | 14.3           | 1¹            | Tokyo, Japan         |

> **Note ¹**: The 1 ms latency appears unusually low for a remote server. It may indicate latency between the VPN server and the speed test server, not the client’s connection to Japan.

## Research on VPN Encryption and Privacy Features

VPNs use tunneling protocols like OpenVPN, WireGuard, and IKEv2/IPsec to establish secure, encrypted connections. These protocols employ strong encryption algorithms (e.g., AES-256) to protect user data.

Key privacy and security features include:

- **No-Log Policy:** Reputable VPNs like ProtonVPN commit to not storing logs of your activity [5].
- **Kill Switch:** Disconnects your device from the internet if the VPN drops, preventing IP leaks.
- **DNS Leak Protection:** Ensures DNS queries stay within the encrypted VPN tunnel.
- **Secure Core (Multi-hop):** Routes traffic through multiple servers in privacy-friendly jurisdictions, adding extra security [6].

## Summary: VPN Benefits and Limitations

### Benefits

- **Enhanced Privacy:** VPNs mask your IP, making tracking by websites, ISPs, or advertisers more difficult.
- **Secure Communication:** VPNs encrypt traffic, especially important on public Wi-Fi.
- **Bypassing Geo-restrictions:** VPNs enable access to region-locked content by making you appear to browse from another country.
- **Protection Against Censorship:** VPNs help users access blocked websites and services in restrictive regions.

### Limitations

- **Reduced Speed:** Routing through remote servers can reduce speeds, particularly for upload bandwidth.
- **Cost:** Free tiers exist, but full-featured VPNs typically require a subscription.
- **Trust in Provider:** Users must trust the VPN provider to enforce privacy policies.
- **Not Complete Protection:** VPNs don't stop malware, phishing, or other direct attacks.
- **Potential for IP Leaks:** Misconfiguration or bugs may expose your real IP in rare cases.

## Conclusion

This hands-on experience confirmed that VPNs effectively alter your IP address, encrypt traffic, and enhance online privacy. While free VPNs like ProtonVPN provide a good introduction, understanding their limits and choosing a trustworthy provider is vital for long-term security.

---

## References

1. ProtonVPN Free Plan Overview – ProtonVPN Official Site  
2. OpenVPN Installation on Kali Linux – Kali.org Docs  
3. ProtonVPN OpenVPN Configuration Guide – ProtonVPN Support  
4. WhatIsMyIPAddress.com – IP Lookup Tools  
5. ProtonVPN Privacy Policy – No-Logs Commitment  
6. ProtonVPN Secure Core Technology – Multi-Hop Explained  

