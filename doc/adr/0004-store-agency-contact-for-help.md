# 4. store Agency contact for Help

Date: 2023-09-14

## Status

Proposed

## Context

The **Help** service allow user to get direct access to a prefered travel agency.
The contact, phone or mail should be provided by the app to allow a quick redirection of possible request.

## Decision

We will store the contact and details of all the agencies we have booking for.

```bash
                                 +---------+      <=========>             +--------+
   +------+        +------+      | Booking |      | Booking |             | Travel |
   | User |        | Help |      |  crud   |      |  Db     |             | agency |
   +------+        +------+      +---------+      <=========>             +--------+
      .               .               .               .                       .
      .-------------->.               .               .                       .
      .               .               .               .                       .
      .               .-------------->.               .                       .
      .               .               .               .                       .
      .               .               .-------------->.                       .
      .               .               .               .                       .
      .               .               .               .                       .
      .               .               .<--------------.                       .
      .               .               .               .                       .
      .               .<--------------.               .                       .
      .               .               .               .                       .
      .<--------------.               .               .                       .
      .               .               .               .                       .
      .---------------------------------------------------------------------->.
      .               .               .               .                       .
      .               .          +---------+      <=========>             +--------+
   +------+        +------+      | Booking |      | Booking |             | Travel |
   | User |        | Help |      |  crud   |      |  Db     |             | agency |
   +------+        +------+      +---------+      <=========>             +--------+

```


## Consequences

### Positive

- easy access to the data without making new calls via the **Collector Agency**.
- data related to help operation can be stored to the db for further **Analytics**

### Negative

- one more external dataset to be store and kept up to date
