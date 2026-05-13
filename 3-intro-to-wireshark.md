# WinPcap
WinPcap Capture Driver is the windows implementation of the pcap packet-capturing application programming interface. this driver interacts with your operating system to capture raw packet data, apply filters, and switch the NIC in and out of promiscuous mode.

##
**The Driver** (NPF): It includes a low-level kernel-mode driver called the Netgroup Packet Filter (NPF). This driver sits right on top of the Network Interface Card (NIC). Its job is to grab packets directly from the wire before the Windows networking stack even sees them.

**The API** (Packet.dll and wpcap.dll): These are the high-level libraries that programmers use. Instead of writing complex code to talk to the hardware, you just call a function like pcap_open() or pcap_next_ex().

# Npcap
**The Driver**: Instead of the old NPF, it uses a Lightweight Filter (LWF) driver based on the modern NDIS 6 framework. It still sits "below" the Windows TCP/IP stack to intercept raw frames.
**The API**: It provides the same familiar .dll files so that tools like Wireshark or Scapy don't have to be rewritten from scratch to support it.

*   **Normal:** Python (Scapy) --> Npcap API (wpcap.dll, Packet.dll) --> Npcap kernel Driver.
*   **Advanced/Custom:** C++ --> Npcap Driver (faster, lower level).
*   **Deep Modification:** WinDivert or custom NDIS drivers (allows for dropping/modifying traffic before it moves).

# bonus (build from source)
*   **Step 6 (`make`):** This is where the **compiling** happens.
*   **Step 7 (`sudo make install`):** This moves the built files to the right folders.
*   **Step 8 (`sudo ldconfig`):** This tells the system's "map" where the new library is.

# Wireshark Preference
### Capture packets in monitor mode on 802.11 devices
In normal Wi-Fi operation, your card must "associate" (connect) with a specific router to see data. It captures raw wireless frames flying through the air from any nearby network.

### Profiles
can share with others