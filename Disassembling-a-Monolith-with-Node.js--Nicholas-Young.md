# Disassembling a Monolith with Node.js
*Nicholas Young*

http://bit.ly/nodevember-2014

## Who am I?

- I like getting things DONE.
- Tinkering is useless unless it teaches us something
- My passion isn't writing code for the sake of writing code

## Scalability

The process to handle a growing amount of work.

### Ruby

- Slow runtime
- Poor threading support
- Concurrent, long-running tasks

While everything happens in the background, your user thinks the app is doing nothing.

Why?

Because I built the monolith:

- public facing website
- feed generation
- embeddable, sharable player
- admin dashboard
- media analytics

Failed deploy = all services down

It doesn't mean ruby is inherantly awful, it just doesn't work well with our app.

### Node.js

- I started out in Node.js by trying to create a monolith.
- The deploy failed
- I went to the Node.js website and realized the point is to separate into modules

#### Applications and Dependencies

- CMS - Application
- Feed generation - Application
- Embeddable PLayer - Application
- Media Analytics - Application
- Models - Dependency
- Config - Dependency

### Common App Stack

- Express
- MongoDB
- ZeroMQ
- Distributor
- Storage
- Transport

## Takeaways

- Prototype relentlessly
- Break BEFORE you build
- Ask what do I need--can each function operate discreetly?
