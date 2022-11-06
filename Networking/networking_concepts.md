# Types of networks:
   - peer-to-peer - every computer can communicate with all others
   - client/server - using a central computer (server) to fascilitate communications with other computers (clients). To function as a server       computer needs to run an NOS (Network Operation System)

## LANs, MANs  and WANS
- LAN - Local area Network - realtively small place (e.g. one office)
- MAN - Metropolitan Area Network - network larger than one building which connects clients and servers from multiple buildings
- WAN - Wide Area Network - Network that connects multiple geographically distinct networks

## Network Topologies
- Bus
- Ring
- Star
- Hybrid

# OSI - Open Systems Interconnection - Model

## Application layer
    Application layer facilitates communication with programs and lower-layer network services. 
    HTTP is one of application level protocols, which formats and sends the request to server, same with the response from the server.

## Presentation layer
    Formatting the data. Encryption-decryption. SSL and TLS are some of presentation layer protocols

## Session Layer
    Coordinates and maintains communications between two nodes on the network. Includes establishing and termination of communications.
    Synchronisation. 
    Determines whether communication has been cut off, and if so tries to restart it. 
    Ensures identification and authorisation of participants

## Transport Layer - operates with SEGMENTS
    Manage end-to-end delievery of data. Flow control. TCP is one of Transport layer protocols. 
    TCP is connection oriented and performs and three-way hadshake. 
    Transport layer performs segmentation and reassembly of data. Sequencing identifies what group segments belong to. 
    Also, sequencing indicates where data unit begins and the order in which groups of data were issued, and therefore, should be interpreted.

## Network Layer - operates with PACKETS
    Translates network addresses into their physical counterparts and decides how to rout data from the sender to the reciever. 
    Accepts data segments and adds logical addressing information in a network header. IP protocol is one of the Network layer protocols.
    Performs fragmentation (TCP/IP connections)

## Data Link Layer - operates with FRAMES
    Data link protocols divide data they recieve from the Network Layer int distinct frames that can be transmitted using physical layer.
    Frame includes payload, sender's and reciever's network addresses, error checking and control information. 
    Performs Cyclic Redundancy Check - basically check hash of the data. 
    Also, data link layer waits for acknowledgement and retransmits if does not get some in some specific period of time.
### LLC - Logical Link Control sublayer
    Provides an interface to the Network Layer Protocols, manages flow control and issues requests for retransmission for data that suffered errors
### MAC - Media Access Control sublayer
    Manages access to physical layer. Appends physical address of the destination computer onto the data frame.

## Physical Layer
    Manages transportation of Frames through physical media such as copper wires, radio waves, etc.
