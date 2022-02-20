# arduino_event_messager
Aiming to implement a message handling state machine class using interrupts for critical timing 



## Topology

1. Various events can be used to trigger ISR
2. ISR  adds message to event handling stream.
3. Event handling stream could be an arduino String, or char array
4. custom messages can be added to stream by generic ISR
5. reader loop is parsing the events in the stream, and triggering a state machine to handle the current event.
6. once state machine has moved back to waiting, next message is parsed?

This method has no way of assigning priority, it processes in a first in first out.

### Expand on the idea

Messages will contain 3 parts.

(MESSAGE_STRING, JSON_DATA, PRIORITY, STOP_WORD)


_Now parsing method can assign a PID to the tast, and save this in __Linked List__ _




[LINKED_LIST](https://www.bitdegree.org/learn/linked-list-c-plus-plus#:~:text=%2B%2B%3A%20Useful%20Tips-,What%20is%20a%20Linked%20List%20in%20C%2B%2B%3F,next%20and%20the%20previous%20node.)




### TODO:


[Example Event Handler Library](https://github.com/igormiktor/arduino-EventManager)



