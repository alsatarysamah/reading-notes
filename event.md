# EventEmitter

 useful module  that allows us to get started incorporating Event-Driven Programming in our project right away. 

const EventEmitter = require('events').EventEmitter;
const myEventEmitter = new EventEmitter;

## Removing Listeners

To remove event listeners in EventEmitter we can use the removeListener or removeAllListeners method.

**simple EventEmitter instance with a single listener.**

const EventEmitter = require('node:events');

class MyEmitter extends EventEmitter {}

const myEmitter = new MyEmitter();

myEmitter.on('event', () => {

  console.log('an event occurred!');});

myEmitter.emit('event');



## Handling events only once

myEmitter.once('event', () => {

  console.log(++m);});

  ## Asynchronous vs. synchronous
  listener functions can switch to an asynchronous mode of operation using the *setImmediate()* or *process.nextTick()* methods.

  ## Error event

  myEmitter.emit('error', new Error('whoops!'));

  Event: 'removeListener'#

eventName <string> | <symbol> The event name
listener <Function> The event handler function
The 'removeListener' event is emitted after the listener is removed.

emitter.addListener(eventName, listener)#
Added in: v0.1.26

eventName <string> | <symbol>

listener <Function>

Alias for emitter.on(eventName, listener).

emitter.emit(eventName[, ...args])#
Added in: v0.1.26

eventName <string> | <symbol>

...args <any>

Returns: <boolean>

**emitter.getMaxListeners()#**

Returns: <integer>

Returns the current max listener value for the EventEmitter which is either set by emitter.

setMaxListeners(n) or defaults to events.defaultMaxListeners.

**emitter.listenerCount(eventName)#**

eventName <string> | <symbol> The name of the 

event being listened for


Returns: <integer>
Returns the number of listeners listening to the event named eventName.

