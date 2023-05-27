

![alt text](https://i.imgur.com/LLLsARj.png)

# **Lab Exercise Projects**:
# In this tutorial we will practice performing activities on a network in an Azure virtual environment.
# We will see the actual raw traffic being transmitted between the 2 virtual machines. I hope this gives a better understanding of firewalls.

## What Azure resources will we be working with?

* Azure Virtual Machines (Windows and Linux [Ubuntu])
* Azure Network Security Groups (Firewall Resources)

## What Software Utilities and Tools will we be working with?

*  Wireshark 64 bit (A protocol analyzer)
*  Many command line tools
*  Powershell
*  Remote Desktop

## Operating Systems Used

* Windows 10
* Linux [Ubuntu]

## What this exercise will show?

 1. This tutorial will go over the basics of using Wireshark packet analyzer
 1. We will be working with 2 Azure VM's (one running Windows 10 and the other running Linux [Ubuntu]
 2. We will be working with Azure's network security group or it's firewall
 3. We'll be watching raw traffic 
 
 
![alt text](https://i.imgur.com/W0IMQx3.png)

## 1.  How can we start scanning for network data packets?
As the **above image** shows, select the adapter device that will capture the packets.  Afterwards, select the "blue shark fin" in the
upper left-hand corner. Press this icon to start capturing the data packets.


![alt text](https://i.imgur.com/p7TdjWl.png)

## 2. How to find traffic that is unencrypted?
As we can see in the **above image**, one way unencrypted data can be found is by clicking on Internet Control Message Protocol
and going through data in this area.

![alt text](https://i.imgur.com/UYIwtLR.png)
## 3. How can we start filtering Wireshark using **ICMP** protocol?
As shown in the **above image**, we can do this by typing the **ICMP** protocol in the filter area.

![alt text](https://i.imgur.com/mpEwgdF.png)
## 4. Using the image above, we can see everything in action using the **ICMP** protocol and the **Ping** and IP address through **PowerShell**.
After adding **ICMP** as a filter, open **PoweShell** and **ping 10.0.0.5** the (VM-2 IP address), as shown above.

![alt text](https://i.imgur.com/Fw2tvDx.png)
## 5. As we can see in the image above, a "Continuous Ping" response between VM-1 and VM-2 by using the "ping -t" command.

## 6. While still using the **Continuous Ping** between VM-1 and VM-2, how can we **Block ICMP** traffic from coming through the VM-2 firewall?


## 7. To make this change to the VM-2 firewall, we must make changes to the VM-2 **Inbound Security Rule**, as shown below.

![alt text](https://i.imgur.com/vBHzcwu.png)

## 8. Now, let's monitor this rule change, as seen below:

![alt text](https://i.imgur.com/N8kwOm0.png)
## 9. We now see that the "continuous" ping has started "timing out", as shown above.

## 10. Now, let's show the example of changing the **Inbound Security Rule** back to "ALLOWING" Continuous Ping traffic through VM-2 firewall, as shown below.
![alt text](https://i.imgur.com/M5jxx6J.png)

## 11. Now, let's monitor the captured traffic as the **Inbound ICMP** port is reopened, allowing data to come through VM-2 firewall once again as the data goes from "Request Timed Out" to "Reply from 10.0.0", as shown below.
![alt text](https://i.imgur.com/GhcYD2k.png)


## 12. Show how we can use **NSLOOKUP** to find the IP address of www.google.com

![alt text](https://i.imgur.com/BgIH8S2.png)








