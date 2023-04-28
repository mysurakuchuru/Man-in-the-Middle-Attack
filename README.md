# Man-in-the-Middle Attack

This repository contains the implementation of a man-in-the-middle attack, which is a type of cyber attack where the attacker intercepts the communication between two parties and can eavesdrop on the conversation, modify the messages, or impersonate one or both parties.

## Overview

The attack is implemented using Python and the scapy library, which is a packet manipulation tool for computer networks. The attacker acts as a middleman between the two parties and intercepts the traffic by sniffing the network packets. The attacker can then modify the packets and forward them to the intended destination without either party knowing.

The implementation includes two scripts:

- `arp_spoof.py`: This script performs an ARP spoofing attack to redirect the traffic from the victim machine to the attacker's machine.

- `mitm.py`: This script performs the actual man-in-the-middle attack by intercepting the traffic, modifying the packets, and forwarding them to the intended destination.

## Prerequisites

To run the scripts, you need to have the following prerequisites installed on your machine:

- Python 3.x
- scapy library
- Linux or macOS operating system

## Usage

To use the scripts, follow the steps below:

1. Clone the repository:

   ```
   git clone https://github.com/mysurakuchuru/Man-in-the-Middle-Attack.git
   ```

2. Change to the repository directory:

   ```
   cd Man-in-the-Middle-Attack
   ```

3. Run the `arp_spoof.py` script with the victim's IP address and the gateway's IP address:

   ```
   sudo python3 arp_spoof.py -t <victim_ip_address> -g <gateway_ip_address>
   ```

4. Open a new terminal and run the `mitm.py` script with the victim's IP address and the attacker's IP address:

   ```
   sudo python3 mitm.py -t <victim_ip_address> -a <attacker_ip_address>
   ```

5. The script will intercept the traffic between the victim and the gateway and display the packets on the screen. You can modify the packets by changing the values in the script.

## Disclaimer

This repository is for educational purposes only. The author is not responsible for any misuse of the information and code provided in this repository. It is recommended to use this code only with the permission of the parties involved and for ethical purposes only.
