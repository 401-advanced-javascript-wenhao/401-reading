# Reading 18 - Socket.io - 5/6/2020

## Web Sockets
* Provides bi-directional communication between the client and the server over a TCP connection.
* Allows the real-time data transfer.

## Socket.io
* Enables real-time and full duplex communication between the client and the server.
* Also provides broadcasting, namespacing etc.
* Client side: it is the library that runs inside the browser.
* Server side: it is the library for Node.js

## Connections
* With TCP: connect to a server with a keep-alive type of connection.
* With Socket.io: connect over http, keep-alive by websocket protocol.

## Messaging
* Socket.io uses `emit()` send events and uses `on()` receive events.
* Socket.io has events shared between 'disconnecte' participants.
* clients connect, emit events, respond to events from the server.
* Socket.io work flow:
  1. Client connect to a Socket.io server (common pool, groups, subgroups)
  2. Client emits events
  3. Server listens events
  4. Server either braodcast or emit as response for events
  5. Other client may have a listener on that event can 'hear' it as well
* Not every client will have a listener for every event
* The server may not have a listener for every event a client sends
