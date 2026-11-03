# Networkwalks-B084M-Week1-CyberSecurity_LabSetup

## 🎯 Objective
The primary objective of this project is to set up a secure, isolated virtualization environment for ethical hacking, penetration testing, and network analysis exercises using Oracle VirtualBox and Kali Linux.

---

## 🛠️ Tools & Technologies Used
* **Virtualization Platform:** Oracle VirtualBox
* **Operating System:** Kali Linux (Latest Release)
* **Networking Mode:** NAT Network (for secure internal communication and controlled internet access)

---

## 📋 Step-by-Step Lab Setup Guide

### Step 1: VirtualBox Installation
* Download and install the latest version of Oracle VirtualBox for your host operating system along with the VirtualBox Extension Pack.
* *Screenshot Reference:* `1.Screenshot of Virtual_Box.png`

### Step 2: Configuring NAT Networks
* Set up a dedicated virtual network switch in VirtualBox to allow future virtual machines to communicate with each other securely without exposing them directly to the physical host network.
* Navigate to **File > Preferences > Network** and create a new NAT Network.
* *Screenshot Reference:* `2.Screenshot of NAT Networks setup.png`

### Step 3: Importing Kali Linux Virtual Machine
* Download the official Kali Linux VirtualBox pre-configured image (.ova file) from the [Kali Linux Downloads page](https://www.kali.org/get-kali/#kali-virtual-machines).
* Import the appliance into VirtualBox via **File > Import Appliance** and allocate appropriate system resources (Recommended: at least 2 GB RAM and 2 CPU cores).
* *Screenshot Reference:* `3.import kali in virtual box.png`

### Step 4: Configuring Network Adapters
* Open the settings of your newly imported Kali Linux VM.
* Go to the **Network** tab, change Adapter 1 to **NAT Network**, and select the NAT network you created in Step 2.
* *Screenshot Reference:* `4.screenshort-of kali-network-setting.png`

### Step 5: Verifying Network Configuration
* Boot up Kali Linux and verify the internal network connection and IP address assignment via the terminal using command-line interface utilities.
```bash
ip a
ping -c 4 8.8.8.8
```
## 💡 What I Learned

Through setting up this cybersecurity lab environment, I gained hands-on experience and a deeper understanding of fundamental networking and virtualization concepts:

* **Hypervisor & Virtualization Basics:** Learned how to configure Oracle VirtualBox to host and isolate virtual operating systems safely away from the host machine.
* **Network Segmentation & Isolation:** Understood how **NAT Networks** function to allow internal virtual machines to communicate securely while controlling and restricting external exposure.
* **OS Deployment & Resource Allocation:** Gained practice in importing pre-configured virtual appliances (like Kali Linux) and properly allocating system hardware (RAM and CPU cores) for optimal performance.
* **Command-Line Verification:** Practiced using essential terminal networking utilities (such as `ip a` and `ping`) to troubleshoot interface connectivity and verify network configuration status.
### Repository Structure

 1.Screenshot of Virtual_Box.png

2.Screenshot of NAT Networks setup.png

3.import kali in virtual box.png

4.screenshort-of kali-network-setting.png

5.Screenshot of network-config-in kali.png

README.md
### Conclusion
This setup successfully establishes a foundational, safe, and repeatable lab environment ideal for executing subsequent cybersecurity assignments, vulnerability scans, and penetration testing walkthroughs.
