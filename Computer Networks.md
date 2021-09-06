# Computer Networking

## 2021-09-01

### Introduction

* LAN (Local Area Network): LAN can be defined as one hop distance.
    1. Wired LAN(eg. Ethernet(802.3))
    1. Wireless LAN(eg. WiFi(802.11), Bluetooth(802.15))

* Address 
    1. Logical Address(IP Address)
    1. Physical Address(MAC Address)

* Port Number: Port number is used to identify different application

* Problems with electric transfer
    1. Signal Weakening with length/distance
    1. Noise

## 2021-09-03

### The OSI Model and TCP/IP Protocol Suite

#### Need for Protocol
* A protocol is required when two entities need to communicate. When communication is not simple, we can use protocols

#### The OSI Model

* (OSI model slide picture)

##### Layers in OSI model

* Layer 7: Application
* Layer 6: Presentation
* Layer 5: Session
* Layer 4: Transport
* Layer 3: Network
* Layer 2: Data Link
* Layer 1: Physical

(osi layers picture)

(comparison of tcp/ip and osi model)

###### Physical Layer

(physical layer image)

* Physical Layer is responsible for movement of individual bits from one hop(node) to the next

###### Data Link Layer

(data link layer image)

* Data Link Layer is responsible for moving frame from one node(hop) to next

* Data Link layer connects network layer to physical layer

* We add one header and one tail to the data and define frame

* header - src, destination, coding schema, etc

* tail - parity, error checks

* (Hop To Hop delivery)

(Hop to hop delivery image)

###### Network Layer

* The network layer is responsible for delivery of single packet from source host to destination host

(source to destination delivery image)

###### Transport layer

* The network layer is responsible for delivery of single packet from source host to destination host

###### Summary


#### Addressing