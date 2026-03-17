# pi-hole-homelab

# Home Lab: Network-Wide DNS Sinkhole (Pi-hole)

## Overview
As part of my career pivot into **Cybersecurity**, I have deployed a dedicated network-wide ad blocker and DNS sinkhole using a **Raspberry Pi Zero 2W**. This project demonstrates hands-on experience with Linux administration, networking fundamentals, and proactive network defense.

## Hardware & Environment
* **Device:** Raspberry Pi Zero 2W
* **Storage:** 16GB MicroSD (SanDisk)
* **Operating System:** Raspberry Pi OS Lite (64-bit) - *Headless Setup*
* **Location:** Home Lab (Sydney, Australia)

## Technical Implementation

### 1. Provisioning & Headless Setup
* Flashed the OS using the **Raspberry Pi Imager** with custom pre-configurations.
* Enabled **SSH** for remote CLI management.
* Configured **WPA2-PSK** Wi-Fi authentication via the backend to allow for a true headless boot.
* Updated the system repository and upgraded all packages:
    `sudo apt update && sudo apt upgrade -y`

### 2. Networking & Static Addressing
* Identified the device hardware address (MAC) to ensure network persistence.
* Configured a **DHCP Static IP Reservation** on a Netcomm Cloudmesh gateway.
* Verified local connectivity using `ssh` and `arp -a` network scanning.

### 3. Pi-hole Configuration
* Deployed the Pi-hole core software using the automated install script.
* Configured **Cloudflare (1.1.1.1)** as the upstream DNS provider for encrypted, high-speed resolution.
* Established a **Web Admin Interface** to monitor real-time traffic and blocklist performance.

## Cybersecurity Lessons Learned
* **DNS Filtering:** Understanding how a sinkhole intercepts requests for known malicious/ad-serving domains before they reach the browser.
* **Network Visibility:** Using the Query Log to identify "chatty" IoT devices and unwanted telemetry from mobile applications.
* **Asset Management:** Practiced the "Identify" function of the NIST framework by managing hardware IDs and IP assignments within a local network.

---

## Dashboard Preview

**Created by Tom** *Aspiring Cybersecurity Analyst | Sydney, NSW*
