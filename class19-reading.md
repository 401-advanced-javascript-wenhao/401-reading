# Reading 19 - Message Queues - 5/7/2020

## Message Queues
* Routing events and messaging between clients.
  * Any connected client can 'publish' a message into the server.
  * Any connected client can 'subscribe' to receive message by type.
* See which clients are connected, to which Queues they are attached and further, to which events they are subscribed.
* Receiving any published message and then distributing it out to all connected and subscribed clients.

## What is a message?
A message is a package of information, categorized by queue and event
* Queue - which bucket does this message belong to?
* Event - what event(CRUD, error etc) has happened?
* Payload - data associated with the event (record id, record information etc).

## Real Time vs Queued Messaging
* Real Time: If subscribers lose connection at any point, they won't receive messages they missed out.
* Queued Messaging: Queue will keep track of the delivery status of every event/message. 

## Use case
* An API server responds to a POST request - when DB run 'CREATE' operation, it will send back operation results (successful or unsuccessful) to the client.
* Logging application
* Web-based dashboard application
* Monitor application