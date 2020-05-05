# Reading 16 - Event Driven Application - 5/4/2020

## Event Driven Programming
How can we leverage event driven in software application?
* Everything is JS is an object. Even arrays, functions, documents, windows are object.
* Most action in JS are event driven
  * UI Events - click, hover, zoom etc
  * Express routes
  * Model Lifecycle Hooks
  * React Components - class

## Emitting Events
* Modern browser comes with a lot of handy events we can use such as click, scroll, zoom, hover etc.
* In JS, we can use events module in Node.js to create custom events and use emit function to fire registered events.