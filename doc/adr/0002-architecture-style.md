# 2. Architecture style

Date: 2023-09-14

## Status

Accepted

## Context


After qualifying the  [requirements](/doc/architecture-characteristics.md) into valid architecture characteristics 
we found the following aspects be the driving characteristics.

- Performance
- Responsiveness
- Availability
- Elasticity

We reviewed different architecture style that could fit the Problem

## Decision

We will implement an **Event-driven** architecture.

## Consequences

What becomes easier or more difficult to do and any risks introduced by the change that will need to be mitigated.

### Positive

- Perfomance
- Responsiveness
- using event driven architecture we will have less moving parts

### Negative

- possible cost to
- error handling will be more difficult due to the asynchronous behavior.
