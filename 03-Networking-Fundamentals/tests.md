# Networking Fundamentals: Self-Test.

## Concepts:
1. What is a packet?
- A small unit of data sent across a network, containing part of a message plus source and destination info.

2. Why is data split into packets?
- Because networks handle lots of traffic, so sending smaller pieces allows easier routing, retries, and faster delivery.

3. What problem does an IP address solve?
- It uniquely identifies a device on a network so other devices know where to send packets.

4. What is the role of a router?
- A router forwards packets between networks directing them toward their destination.
- Routers are usually the gateway to the internet.

5. What is a protocol?
- A set of rules that devices follow to communicate and exchange data reliably.
- Examples: TCP, UDP, HTTP, HTTPS.

## Thinking Questions:
1. What could happen if packets arrived out of order?
- The message might be 'jumbled' but protocols like TCP reorder the packets to reconstruct the original message.

2. Why might some packets be lost?
- Networks can be busy, congested, or unreliable. A packet might be dropped along the route.

3. Why is retrying a single packet better than retrying an entire message?
- It's faster, reduces network traffic, and avoids resending data that already arrived successfully.
