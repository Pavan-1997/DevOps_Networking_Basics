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
