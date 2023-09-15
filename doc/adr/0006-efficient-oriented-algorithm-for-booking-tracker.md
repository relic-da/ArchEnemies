# 6. efficient oriented algorithm for booking tracker

Date: 2023-09-15

## Status

Accepted

## Context

The issue motivating this decision, and any context that influences or constrains the decision.

## Decision

We will create a 2 separate aproach for the data update.


**Near Real-Time Update**: This is responsible for near real-time updates for events with expiring dates within a specified timespan.

**Batch Update**: This is a periodic full updates of all events and runs as a background job with relaxed time constraints.

## Consequences

What becomes easier or more difficult to do and any risks introduced by the change that will need to be mitigated.
