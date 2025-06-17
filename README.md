# Real-Time Push Notification System

A production-ready real-time notification delivery system built with:

- **Django + Channels** (WebSockets)
- **Kafka** (event queue)
- **Redis** (channel layer)
- **Docker** (for infrastructure)

## Goal 
This system demonstrates an architecture that enables:
- Real-time WebSocket push to connected clients
- Decoupled, scalable event processing via Kafka
- Easy integration with microservices producing messages
- Extensibility for multi-user, role-based notification delivery
