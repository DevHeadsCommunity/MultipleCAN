# MultipleCAN
This project demonstrate how to make STM32F303K8 Nucleo board as CAN Nodes

# CAN Bus (Normal Mode) Firmware Implementation on STM32 Cortex-M4 MCU

> 🎥 **Live Demo Available!**  
> Watch the full implementation on our YouTube channel and see it in action:  
> 🔗 [Watch Now](https://www.youtube.com/watch?v=appV7spFUJQ&ab_channel=DevHeads)  
>
> 📺 **Don’t forget to [subscribe](https://www.youtube.com/@DevHeads)** to our YouTube channel for more embedded systems tutorials and live demos!  
>
> **DevHeads System Integration Server**  
> Devheads.io – A place for every dev

---

## 📚 Table of Contents

- [OVERVIEW](#overview)
- [CAN BUS NETWORK](#can-bus-network)
- [NETWORK TOPOLOGY](#network-topology)
- [CAN CONTROLLER](#can-controller)
- [WHAT IS A CAN NODE?](#what-is-a-can-node)
- [MCP2551 CAN TRANSCEIVER](#mcp2551-can-transceiver)
- [CONNECTION DETAILS](#connection-details)
- [CAN BLOCK DIAGRAM](#can-block-diagram)
- [DATA FRAME FORMAT](#data-frame-format)
- [LIVE DEMO](#live-demo)
- [THANK YOU](#thank-you)


---

## OVERVIEW

The CAN (Controller Area Network) Bus is a robust communication protocol designed for real-time, multi-master applications. It offers configuration flexibility and enables seamless prioritization of messages between nodes. With guaranteed latency times, strong error detection and signaling mechanisms, and system-wide data consistency, CAN ensures reliable communication in complex systems. Its support for multicast reception and time synchronization makes it ideal for automotive, industrial, and embedded applications. 

---

## CAN BUS NETWORK
The CAN Bus network is a multi-bus system where multiple ECUs (Electronic Control Units) communicate over a shared two-wire differential bus. It supports multiple nodes connected together, allowing each node to send and receive messages without a central master. This decentralized approach makes the system scalable, reliable, and ideal for industrial and automotive environments.

   <img width="678" height="346" alt="image" src="https://github.com/user-attachments/assets/f8ba0466-5f56-49ce-ae17-1cb6f867522c" />
     

---

## NETWORK TOPOLOGY

<img width="678" height="346" alt="image" src="https://github.com/user-attachments/assets/9d5fe822-6a7b-47e8-a64c-2e7b18fb497d" />

---

## CAN CONTROLLER

<img width="678" height="346" alt="image" src="https://github.com/user-attachments/assets/f931fa69-b204-4caf-b321-e2bb892d62fb" />


---

## WHAT IS A CAN NODE?

- **CAN Transceiver**: Converts signal from physical bus into logic level high/low (voltage level), sends to CAN controller  
- **CAN Controller**:
  - Defines the baud rate  
  - Interprets CAN frames
 
  - <img width="270" height="373" alt="image" src="https://github.com/user-attachments/assets/e2d8340f-a6e3-41c4-b601-b5cd14032f2f" />


---

## MCP2551 CAN TRANSCEIVER

<img width="242" height="208" alt="image" src="https://github.com/user-attachments/assets/73f40d03-f98a-49ba-995f-f454a15f203e" />

- Handles bus connection  
- Two bus pins: CANH (High) & CANL (Low)  
- High noise immunity  
- Two types:
  - **High Speed** (up to 1 Mbit/s)  
  - **Low Speed** (up to 128 Kbit/s)  

---

## CONNECTION DETAILS

<img width="898" height="329" alt="image" src="https://github.com/user-attachments/assets/256bc58c-5894-4ffd-9f87-c5902a5ca009" />

The CAN network consists of multiple CAN nodes interconnected through a differential pair: CANH (High) and CANL (Low). Each node includes a microcontroller, a CAN controller, and a transceiver such as the MCP2551, which ensures reliable communication across the bus. Termination resistors (RT) are used at both ends of the network to prevent signal reflections. For practical implementation and debugging, a CAN frame analyzer can be connected, and status LEDs (e.g., D3 on PB0) may be used for visual feedback.

---

## CAN BLOCK DIAGRAM

<img width="620" height="349" alt="image" src="https://github.com/user-attachments/assets/cc7782b3-6512-494f-9399-1dd18a84fa2c" />


---

## DATA FRAME FORMAT

<img width="620" height="349" alt="image" src="https://github.com/user-attachments/assets/d1e611e4-3508-4fd5-95ad-d6d24ca49bb1" />

The CAN protocol uses structured data frames to ensure reliable communication. Each frame consists of several fields: the Arbitration Field (which includes the identifier and priority), the Control Field (which indicates data length), the Data Field (containing the actual payload), and error-checking fields like CRC, ACK, and delimiters. CAN supports both Standard (11-bit identifier) and Extended (29-bit identifier) formats, providing flexibility in addressing and message filtering.

---


## LIVE DEMO

Watch the live implementation of CAN Bus using bxCAN Firmware on STM32 Cortex-M4:  
🔗 [Watch on YouTube](https://www.youtube.com/watch?v=appV7spFUJQ&ab_channel=DevHeads)

---

## THANK YOU

**Thanks for being a DevHead!**  
Join our community: [https://discord.gg/DevHeads](https://discord.gg/DevHeads)  
'TIL NEXT TIME!  
Devheads.io – A place for every dev
