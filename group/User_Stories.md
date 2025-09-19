# Placeholder Group
**Goal statement:** Our app makes it easy to share and manage the correct contact info with the correct people.

## User Stories

- As a person with both a personal and professional life, I want to quickly and easily share and exchange the correct contact information with the correct people.
- As a college student I want to connect with my peers, both professionally and personally.
- As a business professional at a networking event, I want  to easily and quickly exchange my business contact info with someone I just met.
- As a person who just met a new friend I want to easily and quickly be able to share my personal contact info with them.
- As a content creator, I want to be able to share my many different social media profiles with a lot of people at social events.

## Design Diagrams

- **Box:** Actors
- **Solid Line:** Generic message
- **Dotted Line:** Response

### D0
User 1 inputs contact info into their app. That contact info can be sent to user 2's app. That same contact info is then the output of user 2's app. This process is the same but reversed for sending contact info from user 2 to user 1.

```mermaid
---
title: D0
---
flowchart LR
    input["contact info"]
    app1["User1's app"]
    app2["User2's app or phone"]
    user2["contact info"]

    input <--> app1
    app1 <--> app2
    app2 <--> user2

```

### D1
```mermaid
---
title: D1
---
sequenceDiagram

    User1 ->> Server: Initiates connection
    activate Server
    User2 ->> Server: Initiates connection

    User1 ->> Server: Send User1 contact info
    User2 ->> Server: Send User2 contact info
    
    Server -->> User1: Receives User2 contact info
    Server -->> User2: Receives User1 contact info
    deactivate Server

```

### D2
```mermaid
---
title: D2
---
sequenceDiagram

    User1 ->> Server: Initiates connection
    activate Server
    User2 ->> Server: Initiates connection

    User1 ->> Server: Selects the contact info to send and sends User1 contact info

    Server ->> User2: Asks if User2 would like to accept User1's contact info
    User2 ->> Server: Accepts User1's contact info

    User1 ->> Server: Send User1 contact info to server
    Server -->> User2: Receives User1 contact info from server
    User2 ->> Server: Agrees to share own contact info to User1 and sends
    
    Server -->> User1: Receives User2 contact info from server
    deactivate Server

```