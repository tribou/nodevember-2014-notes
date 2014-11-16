# Ready for battle! - Hardening Node.js for the Enterprise
*Jeff Barczewski*

## Why build scalable, durable apps?

- Kmart's site November 2013
- HealthCare.gov

## Mastercard Caas

- July 2013 - asked to use Node.js to replace legacy, under-performing code
- December 2013 - completed the first major deployment
- Crypto as a Service
- Node.js, redis, postgres, plus add-on HSM
- REST API
- Highly scalable and available
- Reporting, administration

## Mastercard / Apple Pay Launch

- Complex deployment, many third parties
- Field testing
- US public launch - "It just worked"

## Other Enterprise Use

- Walmart
- PayPal, LinkedIn
- Yahoo, eBay, Uber, Netflix
- http://nodejs.org/industry/

## Legacy Code and Stagnation

- Reached a point in career where passion was gone
- Felt locked in to legacy environment (Java 1.4)
- Joined Ruby and Node.js communities and was refreshed
- Started focusing on only Node.js

> "If you feel stuck, inspire with your actions."

- If you feel stagnant, try Node.js and communicate out what you like
- Look for ways to use other technologies like Ruby and Node.js in the workplace

## How to Introduce Node.js

Simple beginnings

## Smart API Reverse Proxy

- SSO, batching
- Orchestration, caching
- Device specific content
- Migraiton, AB testing

## Inspired

- Aircraft - inspired me as a kid
  - F15 Eagle

## Life happens

- Things don't go as you'd expect
- F15 Single Wing Landing
- After-analysis of the numbers proved that it could fly with one wing

## Traits that inspire me

- Performant
- Adaptability
- Durability
- Trusted

## Design and Foundations

What frameworks and tools?

- Hapi, Express, Restify
- Is it battle tested?  Quality?  Community?  License?
  - Mastercard doesn't touch GPL.  Uses MIT, Apache licenses
- Prototype with API
  - Try it out to see if you enjoy it
- Joi, Wreck
  - Joi provides validation checking to eliminate overhead
  - Wreck is the HTTP client used by Hapi.  Edge cases are handled.
- Express and Hapi
  - Express is the stock car that's fast and not many extras
  - Hapi is the Corvette Stingray that's approachable by anyone

## How do we scale?

- Node.js is evented architecture
- Cluster, child processes, containers, zones
- Load balancer, nginx, HA proxy, apache

## How do we know it will scale?

- Load test, stress test, vary workload
- bench-rest, wrk, ab
- load runner, blitz.io
- benchmark frequently
- benchmark each commit

## Resilience

How do we make this durable?

- Child processes, cluster_master_ext
  - Child processes are better than cluster
  - All child processes are independent
  - If master goes down, you can reconnect
- Detect process exit, restart
- DB failures, reconnect generic-pool, backoff
- Monit, upstart, forever, nscale

## How to make this hot deployable?

- Rolling restart
- Handle shutdown, exit cleanly, fail-safe timeout
  - Put in hooks to listen for signal to shut things down
  - Remember timers
  - Handle shutdowns from the beginning
- Signals: TERM, INT - shutdown, HUP - rolling restart

## How do we monitor?

- Logging? Events?
- Bunyan, jeffbski/hapi-bunyan-lite
- Notifying, dtrace
- Charting, analytics

## True Friend

- What does that mean to you?
- What value would you put on that?
- That's the kind of software solutions I want to build

*See CodeWinds - Resilient Systems to learn more*
