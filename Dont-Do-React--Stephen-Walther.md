# Don't Do, React!
*Meteor and Reactive Programming*

https://github.com/StephenWalther/Nodevember2014

## What is Meteor?

- JavaScript everywhere
- Run everywhere
- Database everywhere
- Realtime
- Reactive

## Transparent Reactive Programming

- Alternative to event-driven programming
  - Complex dependencies make your code hard to manage
  - You have to re-render the view after the data changes
- Reading data is the same as subscribing to changes
- Meteor Reactivity relies on tracker.js
  - Computation
  - Dependencies
- Batching - reactive changes are not made until the next flush cycle, calls:

```javascript
setTimeout(Tracker.flush(), 0)
```

- You can call Tracker.flush() to force the DOM to update

## Reactive Data Consumers

- Blaze - templating engine

## Reactive Data Sources

- Session
  - A reactive-dict that supports hot code pushes
  - get(), set(), setDefault(), equals()
  - Use equals() if you can.
- reactive-dict
- reactive-var
- Minimongo
- Meteor.user(), Meteor.status(), ...
