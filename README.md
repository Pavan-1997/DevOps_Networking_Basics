# DevOps_Networking_Basics

### 1. **What is Networking?**

Networking involves the practice of connecting multiple computing devices together for the purpose of sharing resources, information, and services. It enables communication between devices like computers, servers, smartphones, and more.

### 2. **IP Address and Subnetting**

- **IP Address**: An IP (Internet Protocol) address is a unique identifier assigned to each device on a network. It can be either IPv4 (e.g., 192.168.1.1) or IPv6 (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334).

- **Subnetting**: Subnetting involves dividing an IP network into multiple sub-networks to improve performance and security. It helps in efficiently utilizing IP addresses.Subnetting is the process of dividing an IP network into sub-networks to improve performance and security. It involves creating smaller, more manageable network segments. Let's go through an example of subnetting an IPv4 address.

**Example:**

Suppose we have the IP address `192.168.0.0` with a subnet mask of `255.255.255.0` (or `/24` in CIDR notation).

1. **Understanding the Subnet Mask:**
   - The subnet mask `255.255.255.0` means that the first 24 bits are fixed for network identification, and the remaining 8 bits are available for host addresses.
   - This provides us with 2^8 (256) possible host addresses within this subnet.

2. **Dividing the Subnet:**
   - Let's say we want to divide this subnet into four smaller subnets.

3. **Determining the New Subnet Mask:**
   - Since we're dividing the subnet into 4 equal parts, we need to borrow 2 bits from the host part for the network part. This gives us a new subnet mask of `255.255.255.192` (or `/26` in CIDR notation).

4. **Calculating Subnet Ranges:**
   - With the new subnet mask, each subnet will have 64 addresses (2^6).
   - We'll have 4 subnets: `192.168.0.0/26`, `192.168.0.64/26`, `192.168.0.128/26`, and `192.168.0.192/26`.

   - **Subnet 1 (192.168.0.0/26):**
     - Network Address: `192.168.0.0`
     - Usable Host Range: `192.168.0.1 - 192.168.0.62`
     - Broadcast Address: `192.168.0.63`

   - **Subnet 2 (192.168.0.64/26):**
     - Network Address: `192.168.0.64`
     - Usable Host Range: `192.168.0.65 - 192.168.0.126`
     - Broadcast Address: `192.168.0.127`

   - **Subnet 3 (192.168.0.128/26):**
     - Network Address: `192.168.0.128`
     - Usable Host Range: `192.168.0.129 - 192.168.0.190`
     - Broadcast Address: `192.168.0.191`

   - **Subnet 4 (192.168.0.192/26):**
     - Network Address: `192.168.0.192`
     - Usable Host Range: `192.168.0.193 - 192.168.0.254`
     - Broadcast Address: `192.168.0.255`

   - **Note:** The first address in each subnet is reserved for the network address, and the last address is reserved for the broadcast address.

This is a basic example of subnetting. In practice, subnetting becomes more complex when dealing with different subnet masks, VLSM (Variable Length Subnet Masking), and routing between subnets. Understanding subnetting is essential for network administrators and engineers.

### 3. **MAC Address**

- A MAC (Media Access Control) address is a hardware address assigned to a network interface card. It's unique to each device and is used for communication within a local network.

### 4. **Protocols**

- **TCP/IP**: Transmission Control Protocol/Internet Protocol is the suite of communication protocols used for connecting hosts on the internet. It includes protocols like TCP (Transmission Control Protocol) and IP (Internet Protocol).

- **HTTP/HTTPS**: HyperText Transfer Protocol (HTTP) and Secure HTTP (HTTPS) are protocols used for transferring data over the internet. HTTPS is secured using SSL/TLS encryption.

- **FTP/SFTP**: File Transfer Protocol (FTP) and Secure File Transfer Protocol (SFTP) are used for transferring files over a network.

- **SMTP/POP3/IMAP**: Simple Mail Transfer Protocol (SMTP) is used for sending emails, while POP3 (Post Office Protocol version 3) and IMAP (Internet Message Access Protocol) are used for receiving emails.

### 5. **Ports**

- Ports are virtual endpoints used for communication between different processes on a network. They allow a single device to host multiple services.

- **Well-known Ports**: Ports ranging from 0 to 1023 are reserved for well-known services like HTTP (80), HTTPS (443), FTP (21), etc.

### 6. **Firewalls and Routers**

- **Firewall**: A firewall is a security device that filters incoming and outgoing network traffic based on a defined set of security rules. It helps protect a network from unauthorized access.

- **Router**: A router is a networking device that forwards data packets between computer networks. It acts as a central hub for data traffic in a network.

### 7. **DNS (Domain Name System)**

- DNS translates human-readable domain names (e.g., www.example.com) into IP addresses that are used by network devices to locate each other on the internet.

### 8. **OSI Model**

- The OSI (Open Systems Interconnection) model is a conceptual framework used to understand network interactions. It's divided into seven layers, each responsible for different functions in the communication process.

   1. Physical Layer
   2. Data Link Layer
   3. Network Layer
   4. Transport Layer
   5. Session Layer
   6. Presentation Layer
   7. Application Layer

These are some fundamental networking concepts and protocols that form the basis of understanding how data is transmitted and received over networks. It's essential for anyone working with networked systems or services.
