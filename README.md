# My First Cybersecurity Lab

> **Goal:** Set up Kali Linux in VirtualBox and understand how its network connection works.
> **Time:** 20–30 minutes · **Level:** Beginner

## What you’ll need

- A computer with VirtualBox installed
- The official Kali Linux VirtualBox image
- At least 2 GB RAM available for the VM

## What the network modes mean

| Mode | What it lets the VM do | Good for |
|---|---|---|
| **NAT Network** | Connect to the internet and communicate with VMs on that NAT Network | This guided setup |
| **Internal Network** | Communicate with other VMs on the same internal network, without internet access | A more isolated practice lab |
| **Host-only** | Communicate with the host computer and other VMs on that network | Host-to-VM testing |

**Safety note:** Only test systems you own or have permission to use.

## Step 1: Install VirtualBox

Install VirtualBox for your computer. Then open it and make sure it starts successfully.

<details>
<summary>What should I see?</summary>

The VirtualBox Manager window should open. Your VM list may be empty.

</details>

## Step 2: Create a NAT Network

In VirtualBox, open **Tools / Preferences → Network** and create a NAT Network. Note its name; you’ll select it in the next step.

![VirtualBox NAT Network settings](2.Screenshot%20of%20NAT%20Networks%20setup.png)

**Check:** Can you see the NAT Network you created in the network list?

## Step 3: Import Kali Linux

Download the official Kali VirtualBox image and import it using **File → Import Appliance**.

![Kali imported in VirtualBox](3.import%20%20kali%20in%20virtual%20box.png)

## Step 4: Connect Kali to your NAT Network

Open the Kali VM’s **Settings → Network**. Set Adapter 1 to **NAT Network**, then choose the network you created.

![Kali network settings](4.screenshort-of%20kali-network-setting.png)

## Step 5: Start Kali and check its network

Start the VM and open a terminal:

```bash
ip a
```

Look for a network interface with an IP address. If you expected internet access, you can also try:

```bash
ping -c 4 8.8.8.8
```

**Remember:** A successful internet test confirms connectivity—not isolation.

<details>
<summary>Troubleshooting: I don’t see an IP address</summary>

- Check that the VM’s network adapter is enabled.
- Confirm Adapter 1 is set to the NAT Network you created.
- Restart the VM and run `ip a` again.

</details>

## Quick self-check

1. Which mode in this guide gives the VM internet access?
2. Which mode would you choose for VMs that should communicate without internet?
3. Does a successful internet ping prove that your lab is isolated?

<details>
<summary>Show answers</summary>

1. NAT Network  
2. Internal Network  
3. No

</details>

## Screenshots

Add one screenshot after each step. Use short, numbered filenames so readers can match them to the guide.

## What I learned

- How to import a virtual machine
- How NAT Network and Internal Network differ
- How to check a VM’s network interface
