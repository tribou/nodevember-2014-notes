# The Engineering Case for Node
*Dan Shaw*

- Rich clients
- Responsive services

> Users expect experiences to be cohesive among all devices

- Internet of things
- Embedded devices

---

> Javascript - An approachable, pervasive language that powers all platforms

## Rapid cycle time from ideation to implementation

Other languages like Java require too much prerequisite scaffolding before you can even start tackling your problem domain

> "By 2017, JavaScript will be the most in-demand language skill in application development (AD)." -Forrester Research 2014

## History of Node.js

- 2009: Hello, world! by Ryan Dahl to solve a problem
  - Node excels at the application development level
  - Golang excels at the systems level
- 2010: early adopters, package managers (kiwi, npm)
- 2011: it works (everywhere)
- 2012: realtime all the things! (socket.io)
- 2013: enterprise proof (walmart, paypal)
- 2014: large scale node.js

## The Engineering Challenge

- Monoliths
  - Slow--in responding to customer needs
  - Time--six months to two years behind
- Shipping code wins
  - Customers don't care about the backend, only the experience

## The Frontend Backend

- Monolithic services in the backend (or a plurality)
- Frontend user experience
- Lightweight Node.js "Frontend Backend" (in the middle)

> {} Backend Services <====> Node.js Frontend Backend <====> HTML5 Frontend

Some companies have tried Node.js for a "hack-day" and have been surprised that they were able to deliver an idea that had been a dream for years.

### Benefits of a Frontend Backend

- Frontline of Customer Experience
- Enabling developers to be masters of their own destiny
- Separate concerns
- Avoid excessive abstraction
- Avoid context switching (reduce mental fatigue)

## Embracing Node.js

### API or Die

  - Remove the multiple data storage abstractions from infrastructure
  - Allow you to focus on the important tiers of the application
  - Database-specific things in your data model creates noise

### Proxies All the Way Down

  - Layers talking to other layers
  - Adapt more flexibly

### Test Early and Often

  - Incorporate wholistic testing
  - Continuous Integration/Deployment because it requires developers to think about their code

### Automate

  - Empower your developers
  - Focus on the meaningful portions of code

> Node.js--Because...JavaScript

## Q&A

### How do you convince your manager?

- Shipping code wins--prove it with small projects first
- *The Business Case for Node*

### What do you do when the backend is SOAP?

- NPM view SOAP
- Proxy all the way down
- Lightweight layer in front of the SOAP to convert XML to JSON
