# Design for Retry
*Microservices, REST, message busses and why idempotency is the only way to scale.*

- Nobody likes pager duty
- You can't avoid errors
- Here's the secret: handle the errors instead

4xx Tell the user what they did wrong
5xx Store the error and do something else

## Causes

- Database down
- Bug in a service
- Deploy in progress
- Power failure
- Kicked a cable
- Network congestion
- Capacity exceeded
- QA tests in production

## You need a queue

- Database on the nodes (leveldb)
- Log file
- Queue server
  - gearman - queues built in, memcache of queues
- Three statuses:
  - OK (200)
  - FAIL (400)
  - ERROR (500)

## Design So ERROR Can Be Retried

gearmand automatically tries a job error again, and again, and again.

You cannot know if an error is a failure

## C = Consistency

Job queues are controlled inconsistency

## Things you can do

- Queue things in localStorage
- Use third-party storage
- Integrate with third-party services with this approach
- Use different strategies for available resources vs contended
