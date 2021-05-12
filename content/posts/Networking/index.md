---
author: Nickapic
title: "Networking Basics"
date: 2021-04-24
description: This is a article to teach people on a very basic level about Networking and going through OSI model.
series: ["Formal Documentation"]
tags: ["Nessus","Networking","OSI", "Network Security"]
categories: ["Offensive Hacking", "Beginners"]
ShowBreadCrumbs: true
--- 



# Introduction-

A network consists of two or more computers that are linked in order to share resources (such as printers and CDs), exchange files, or allow electronic communications. The computers on a network may be linked through cables, telephone lines, radio waves, satellites, or infrared light beams.

Switch is what connects the devices with a ethernet cable connected to all the devices in the network.

To do a  network Wirelessly you can use a router 

To have communication in this network they must speak the same language This language is called protocols all the devices agree on protocols. So all the network hardware are made on these protocols. Like Http, Smtp, Tcp, etc.

Network connects devices you can call them Nodes .Nodes also contain stuff that control network so stuff like router and switches and also end points and hosts (Send and receive data)

Network come in many different sizes -When its less Nodes connected together its called a SOHO network. |Switch can also be called HUB| But hubs are old technology and don't confuse them together

Enterprise Network are networks contain a lot of nodes and basically the network between a company

LAN - Local Area Network ,Can be a SOHO network and a Enterprise Network can have a lot of these LANs connected together.

WAN- Are networks connected together over a huge distance .Like maybe a banks network .And Enterprise networks.

## Layer 1 : Physical
The physical layer is responsible for the transmission and reception of unstructured raw data between a device and a physical transmission medium. It converts the digital bits into electrical, radio, or optical signals. Layer specifications define characteristics such as voltage levels, the timing of voltage changes, physical data rates, maximum transmission distances, modulation scheme, channel access method and physical connectors. This includes the layout of pins, voltages, line impedance, cable specifications, signal timing and frequency for wireless devices. Bit rate control is done at the physical layer and may define transmission mode as simplex, half duplex, and full duplex. The components of a physical layer can be described in terms of a network topology. Physical layer specifications are included in the specifications for the ubiquitous Bluetooth, Ethernet, and USB standards. An example of a less well-known physical layer specification would be for the CAN standard.

## Layer 2 : Data Link

The [data link layer](https://en.wikipedia.org/wiki/Data_link_layer) provides [node-to-node data transfer](https://en.wikipedia.org/wiki/Node-to-node_data_transfer)—a link between two directly connected nodes. It detects and possibly corrects errors that may occur in the physical layer. It defines the protocol to establish and terminate a connection between two physically connected devices. It also defines the protocol for [flow control](https://en.wikipedia.org/wiki/Flow_control_(data)) between them.

[IEEE 802](https://en.wikipedia.org/wiki/IEEE_802) divides the data link layer into two sublayers:[[20]](https://en.wikipedia.org/wiki/OSI_model#cite_note-20)

- [Medium access control](https://en.wikipedia.org/wiki/Medium_access_control) (MAC) layer – responsible for controlling how devices in a network gain access to a medium and permission to transmit data.

- [Logical link control](https://en.wikipedia.org/wiki/Logical_link_control) (LLC) layer – responsible for identifying and encapsulating network layer protocols, and controls error checking and frame synchronization.
- The [Point-to-Point Protocol](https://en.wikipedia.org/wiki/Point-to-Point_Protocol) (PPP) is a data link layer protocol that can operate over several different physical layers, such as [synchronous](https://en.wikipedia.org/wiki/Synchronous_serial_communication) and [asynchronous](https://en.wikipedia.org/wiki/Asynchronous_serial_communication) serial lines.
- > The [ITU-T](https://en.wikipedia.org/wiki/ITU-T) [G.hn](https://en.wikipedia.org/wiki/G.hn) standard, which provides high-speed local area networking over existing wires (power lines, phone lines and coaxial cables), includes a complete data link layer that provides both [error correction](https://en.wikipedia.org/wiki/Error_correction) and flow control by means of a [selective-repeat](https://en.wikipedia.org/wiki/Selective_repeat) [sliding-window protocol](https://en.wikipedia.org/wiki/Sliding_window_protocol).
- > Security, specifically (authenticated) encryption, at this layer can be applied with [MACSec](https://en.wikipedia.org/wiki/IEEE_802.1AE)


## Layer 3 : Network

The [network layer](https://en.wikipedia.org/wiki/Network_layer) provides the functional and procedural means of transferring variable length [data](https://en.wikipedia.org/wiki/Data) sequences (called [packets](https://en.wikipedia.org/wiki/Network_packet)) from one node to another connected in "different networks". A network is a medium to which many nodes can be connected, on which every node has an address and which permits nodes connected to it to transfer messages to other nodes connected to it by merely providing the content of a message and the address of the destination node and letting the network find the way to deliver the message to the destination node, possibly [routing](https://en.wikipedia.org/wiki/Routing) it through intermediate nodes. If the message is too large to be transmitted from one node to another on the data link layer between those nodes, the network may implement message delivery by splitting the message into several fragments at one node, sending the fragments independently, and reassembling the fragments at another node. It may, but does not need to, report delivery errors.

Message delivery at the network layer is not necessarily guaranteed to be reliable; a network layer protocol may provide reliable message delivery, but it need not do so.

A number of layer-management protocols, a function defined in the management annex, ISO 7498/4, belong to the network layer. These include routing protocols, multicast group management, network-layer information and error, and network-layer address assignment. It is the function of the payload that makes these belong to the network layer, not the protocol that carries them.[[21]](https://en.wikipedia.org/wiki/OSI_model#cite_note-21)