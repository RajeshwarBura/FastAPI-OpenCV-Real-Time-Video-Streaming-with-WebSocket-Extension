📌 Real-Time Video Event Detection System using Python & OpenCV 📖 Overview

This project is a real-time computer vision system built using Python, OpenCV, and FastAPI. It processes live video streams (webcam or camera feed), detects motion events from video frames, and streams detection events to connected clients in real time using WebSockets. All detected events are also stored in a SQLite database for later analysis.

The project demonstrates key concepts such as:

Real-time frame processing

Computer vision pipelines

Event-driven architecture

Backend communication using WebSockets

Structured data storage

This system is designed as a learning-oriented but production-style prototype, closely aligned with real-world vision-based backend systems.

🚀 Features

🎥 Live video streaming using OpenCV

🧠 Motion detection using frame differencing

⚡ Real-time event generation (MOTION_DETECTED)

🔌 WebSocket-based real-time event streaming

🗃 Event logging into SQLite database

🧩 Modular and clean Python code structure

📊 Simple frontend to visualize live events

🛠 Tech Stack

Language: Python

Computer Vision: OpenCV

Backend Framework: FastAPI

Real-time Communication: WebSockets

Database: SQLite

Version Control: Git

🏗 System Architecture

Camera / Video Stream

    ↓
Frame Capture (OpenCV)

    ↓
Image Processing Pipeline

    ↓
Motion Detection Logic

    ↓
Event Generator

    ↓
┌───────────────┬────────────────┐

WebSocket Stream Database Logger Live Video Output

📂 Project Structure project/ │

├── main.py # FastAPI app & video stream

├── motion.py # Motion detection logic

├── websocket.py # WebSocket event handling

├── database.py # SQLite database operations

│

├── templates/

│ └── index.html # Simple frontend UI

│

├── static/ # Static assets (if any)

├── events.db # SQLite database

├── requirements.txt

├── README.md

└── screenshots/

⚙️ Installation & Setup 

1️⃣ Clone the Repository git clone https://github.com/YOUR_USERNAME/FastAPI-OpenCV-Real-Time-Video-Streaming-with-WebSocket-Extension-.git

cd FastAPI-OpenCV-Real-Time-Video-Streaming-with-WebSocket-Extension-


2️⃣ Create Virtual Environment python -m venv venv

Activate:

Windows
venv\Scripts\activate

Linux / Mac
source venv/bin/activate

3️⃣ Install Dependencies pip install -r requirements.txt

4️⃣ Run the Application uvicorn main:app --reload

5️⃣ Open in Browser

Video Stream:

http://127.0.0.1:8000

WebSocket Endpoint:

ws://127.0.0.1:8000/ws/events

📡 WebSocket Event Format

When motion is detected, the system sends a real-time JSON event:

{ "event": "MOTION_DETECTED", "timestamp": "2026-01-07 14:45:32" }

🗄 Database Schema

Table: events

Column Type Description

id INTEGER Primary key

event TEXT Event type

timestamp TEXT Detection timestamp

🎯 Learning Outcomes

Understanding real-time video pipelines

Hands-on experience with OpenCV image processing

Working with FastAPI and WebSockets

Designing event-driven backend systems

Managing latency, frames, and throughput

Writing clean and modular Python code

🔮 Future Enhancements

Object detection using YOLO

Kafka-based message queue integration

RTSP camera support

Performance optimization (async + multiprocessing)

Dashboard with analytics

Docker containerization

👨‍💻 Author

Rajeshwar Bura Python | Computer Vision | Backend Development

⭐ Final Note

This project was built to simulate a real-world vision-based real-time system, focusing on fundamentals, scalability concepts, and clean architecture rather than heavy models. It reflects strong alignment with computer vision intern roles involving backend integrations and real-time data processing.
