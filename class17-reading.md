# Reading 17 - TCP Servers - 5/5/2020

## Event Queues
* A lot of NodeJS architecture is build around the use of events.
* All emit events in NodeJS are instance of the `EventEmitter`.
* Can emit events and pass the listener's data.

## OSI Model
* OSI - Open Systems Interconnection - this is how computer communicate.
* It has 7 layers:
  1. Physical
  2. Data Link
  3. Network
  4. Transport - TCP and UDP - This is where our TCP server operates
  5. Session
  6. Presentation
  7. Application

## Internet Protocol Suite (TCP/IP)
* Web developers often reference the TCP/IP model when discussing network communication and data exchange.
* It has 4 layers:
  1. Link Layer
  2. Internet
  3. Transport - TCP and UDP
  4. Application
### TCP - Transimission Control Protocol
* Creates a two way communication between two hosts.
* Provides reliable, ordered, and error checked byte streams between the application.
* Manage network congestion and use flow control to guarantee reliable delivery.

### TCP HEADER
* Control the type of interaction being sent at each end.

### Connection Establishment
1. Client(SYN) -> Server
2. Server(SYN-ACK) -> Client
3. Client(ACK) -> Server

### Connection Termination
1. Client(FIN) -> Server
2. Server(ACK) -> Client
3. Server(FIN) -> Client
4. Client(ACK) -> Server
