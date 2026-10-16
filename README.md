# NETCORE SYSTEM LTD Network Topology Project

This project focuses on designing and configuring a departmental network for **NETCORE SYSTEM LTD** using Cisco networking technologies. The network connects the **IT, Sales, and HR departments**, provides automatic IP address allocation through DHCP, enables HTTP and FTP services, and implements an Access Control List (ACL) to restrict ICMP connectivity between Sales and IT while allowing access to the web server.

## Table of Contents
- [Project Overview](#project-overview)
- [Network Topology](#network-topology)
- [Tools and Technologies](#tools-and-technologies)
- [Configuration Steps](#configuration-steps)
- [Results and Findings](#results-and-findings)
- [Author](#author)

## Project Overview

The purpose of this project is to design, configure, and test a company network that supports communication between three departments while enforcing specific network access restrictions.

The main objectives were to:

- Establish network connectivity between the **IT, Sales, and HR departments**.
- Connect two computers in each department to departmental switches.
- Configure a router to provide connectivity between the three departmental networks.
- Assign a **static IP address** to the IT server.
- Enable the **DHCP service** to automatically assign IP addresses to all six computers.
- Enable and test the **HTTP and FTP services** on the server.
- Configure an **Access Control List (ACL)** to block ICMP Echo traffic from Sales to IT.
- Verify network connectivity, IP address allocation, and web server accessibility.

## Network Topology

The network consists of three departmental networks connected through a router. Each department contains two computers connected to a departmental switch using copper straight-through cables. The switches connect to the router, and the server is located in the IT department.

### Network Layout

- **IT Department**
  - Two computers connected to a departmental switch.
  - One server configured with a static IP address.
  - DHCP, HTTP, and FTP services configured on the server.
- **Sales Department**
  - Two computers connected to a departmental switch.
  - Configured to obtain IP addresses automatically through DHCP.
  - Restricted from sending ICMP Echo traffic to the IT network by an ACL.
  - Permitted to access the IT server's HTTP service.
- **HR Department**
  - Two computers connected to a departmental switch.
  - Configured to obtain IP addresses automatically through DHCP.
  - Connectivity to IT computers verified successfully.
- **Router**
  - Connects the three departmental networks.
  - Configured with an interface for each department.
  - Each interface assigned an appropriate IP address and subnet mask.
  - All three interfaces enabled.
  - ACL configured to enforce the required traffic restriction.

### IP Addressing

- The IT server uses a **static IP address** with a configured subnet mask and default gateway.
- The six departmental computers obtain their IP addresses through **DHCP**.
- A separate range of IP addresses is assigned to each department.
- The router interfaces use IP addresses and subnet masks appropriate to their respective departmental networks.

**Note:** The project document does not specify the exact IP addresses, subnet masks, DHCP ranges, or router interface addresses.

## Tools and Technologies

- **Cisco Packet Tracer:** Network topology design, device configuration, and connectivity testing.
- **Cisco Router:** Interdepartmental routing and ACL implementation.
- **Network Switches:** Connecting computers within each department.
- **Server:** Hosting DHCP, HTTP, and FTP services.
- **Desktop Computers:** Six client PCs distributed across IT, Sales, and HR.
- **Copper Straight-Through Cables:** Connecting computers and switches, and switches to the router.
- **DHCP (Dynamic Host Configuration Protocol):** Automatically assigning IP addresses to client computers.
- **HTTP (Hypertext Transfer Protocol):** Providing web server access.
- **FTP (File Transfer Protocol):** Providing file transfer functionality with a configured username and password.
- **ACL (Access Control List):** Restricting ICMP Echo traffic from Sales to IT.
- **Router Command-Line Interface (CLI):** Configuring router interfaces and access control rules.
- **Command Prompt:** Verifying IP configuration with `ipconfig` and testing connectivity with `ping`.
- **Web Browser:** Testing access to the server's HTTP service.

## Configuration Steps

1. **Design the network topology.**
   - Create three departmental networks for IT, Sales, and HR.
   - Add two computers and one switch for each department.
   - Add a router to connect the departmental networks.
   - Place the server in the IT department.

2. **Connect the network devices.**
   - Connect each computer to its departmental switch.
   - Connect the switches to the router using copper straight-through cables.
   - Connect the server to the IT departmental network.

3. **Configure the router interfaces.**
   - Access the router through its command-line interface.
   - Assign the appropriate IP address and subnet mask to each of the three departmental interfaces.
   - Enable all three interfaces to establish network connectivity.

4. **Configure the IT server with a static IP address.**
   - Assign a static IP address to the server.
   - Configure the appropriate subnet mask and default gateway.
   - Ensure that the server has consistent network addressing for its hosted services.

5. **Enable DHCP on the server.**
   - Turn on the DHCP service.
   - Configure a separate IP address range for each department.
   - Set the appropriate network parameters for each DHCP range.
   - Enable automatic IP address assignment for all six client computers.

6. **Configure the client computers.**
   - Set the computers in IT, Sales, and HR to obtain IP addresses automatically through DHCP.
   - Verify the assigned addresses using the command `ipconfig` in the Command Prompt.

7. **Enable the HTTP service.**
   - Turn on the HTTP service on the IT server.
   - Open a web browser on a client computer.
   - Test access to the server's web page.

8. **Configure the FTP service.**
   - Enable FTP on the server.
   - Create an FTP username and password.
   - Test the FTP configuration and confirm that the response is successful.

9. **Test interdepartmental connectivity.**
   - Use the `ping` command to test connectivity between computers in different departments.
   - Verify successful communication between HR and IT computers before applying the access restriction.

10. **Configure the Access Control List (ACL).**
    - Access the router CLI.
    - Configure an ACL to block **ICMP Echo traffic from the Sales network to the IT network**.
    - Apply the ACL to the appropriate router interface and direction.
    - Preserve access to the HTTP service while enforcing the ICMP restriction.

11. **Verify the ACL and web server access.**
    - Attempt to ping an IT computer from a Sales computer and confirm that the request fails.
    - Verify that Sales computers can still access the server's HTTP service through a web browser.
    - Confirm that the network restriction operates as intended.

## Results and Findings

The project successfully demonstrated departmental network configuration, automatic IP address allocation, server service deployment, and traffic filtering.

The following results were documented:

- **Network topology:** Three departmental networks were connected through a router, with two computers per department and the server located in IT.
- **DHCP configuration:** All six client computers successfully received IP addresses through DHCP.
- **Router configuration:** The three departmental router interfaces were configured with IP addresses and subnet masks and were enabled.
- **HR-to-IT connectivity:** A ping test from an HR computer to an IT computer was successful, demonstrating basic connectivity between the departments.
- **Sales-to-IT restriction:** A ping test from a Sales computer to an IT computer failed after the ACL was applied, as intended.
- **HTTP service:** A Sales computer successfully accessed the IT server's web service despite the ICMP restriction.
- **FTP service:** An FTP username and password were configured, and the service test returned a successful response.

### Key Findings

The project demonstrates that **network reachability and application access are not the same thing**. The ACL restricted ICMP Echo traffic from Sales to IT without preventing Sales users from accessing the server's HTTP service.

The configuration illustrates the importance of:

- Centralized network management through a router.
- Automatic client addressing through DHCP.
- Static addressing for a server that hosts network services.
- Access control rules to enforce departmental network policies.
- Testing both connectivity and application-level services after implementing network security restrictions.

## Author

**Name:** Samuel Ackom

**Student ID:** CS C26 09 EU 001

**Project:** NETCORE SYSTEM LTD Network Topology

**Contact Information:** Not provided in the project document.
