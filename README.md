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

## Files
real-time-push-notification-system/
│
├── notifier/                   # Django app for notification logic
│   ├── consumers.py            # Django Channels WebSocket consumer
│   ├── kafka_consumer.py       # Kafka message consumer
│   ├── routing.py              # App-specific WebSocket routing
│   ├── tests/                  # Unit tests
│   │   ├── test_consumers.py
│   │   └── test_kafka.py
│   └── __init__.py
│
├── notif_project/             # Main Django project
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py                # ASGI config for WebSockets
│   └── routing.py             # Top-level Channels router
│
├── docker-compose.yml         # Redis + Kafka services
├── requirements.txt           # Python dependencies
├── manage.py
├── README.md                  # Project overview and instructions
├── .env.example               # Environment variables template
├── .gitignore
└── frontend/                  # Optional: static JS/HTML/React app
    ├── index.html
    └── websocket.js
