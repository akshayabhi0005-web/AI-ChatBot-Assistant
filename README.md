# AI-ChatBot-Assistant
🤖 Intelligent Voice-Controlled AI Assistant with Dual Display Feedback
An advanced always-listening AI assistant built on Raspberry Pi, designed to deliver hands-free voice interaction, real-time visual feedback, and lifelike animated expressions.
This project blends AI, speech processing, embedded systems, and human-computer interaction into a single continuously running system.

🎙️ How It Works

The assistant operates fully autonomously, without manual input:

🎧 Listens continuously to user speech through a microphone

📝 Converts speech to text using real-time speech recognition

🧠 Processes queries via a large language model using the Groq API

🗣️ Responds using offline text-to-speech synthesis

🔁 Automatically resets after every interaction for uninterrupted operation

No freezing, no manual restarts — just seamless conversation.

🖥️ Dual-Display Visual Feedback
📺 ST7735 TFT Display (SPI)

Used for textual interaction and system status:

💬 Displays user questions and AI responses

📜 Automatically wraps and scrolls long messages

⚙️ Shows system states like:

Listening

Recognizing

Thinking

Speaking

Optimized to fit limited screen resolution while remaining readable and responsive.

👀 SSD1306 OLED Display (I2C)

Provides expressive animated eyes, giving the assistant personality:

😐 Idle / Sleeping

👂 Listening

🧠 Thinking

😊 Happy responses

😴 Sleep & blink animations

Animations dynamically change based on assistant state, creating a natural and intuitive human-machine interaction.

🧩 Software Architecture

The system follows a modular and fault-tolerant design:

🎛️ Controller Layer

Manages system flow and state transitions

Starts and stops animations dynamically

Prevents I2C conflicts and display crashes

🧠 AI Processing Module

Handles Groq API communication

Formats prompts and responses

🎤 Speech Recognition Module

Continuous microphone input

Robust noise calibration

🔊 Text-to-Speech Module

Offline speech synthesis using espeak

Synchronized with animations

🖼️ Display Modules

TFT text rendering and scrolling

OLED eye animations

External animation scripts are launched and terminated dynamically, ensuring smooth performance and stable hardware communication.

📦 Libraries & Technologies Used
🧠 AI & Networking

requests – API communication

Groq API – Large Language Model processing

🎙️ Voice Interface

speech_recognition – Speech-to-text

espeak – Offline text-to-speech

🖥️ Display & Graphics

st7735 – TFT display control

luma.oled – OLED display and animations

Pillow (PIL) – Text rendering and graphics

⚙️ System & Control

threading, subprocess – Process and animation control

dotenv – Secure API key management

🔌 Hardware Interfaces

SPI – TFT display

I2C – OLED display

Carefully optimized to avoid bus collisions and runtime crashes.

🚀 Key Features

🔁 Continuous, non-blocking operation

👀 Animated eyes for lifelike interaction

📜 Auto-scrolling text on TFT

⚡ Fast AI responses via Groq

🧠 Modular, extensible codebase

🛠️ Designed for resource-constrained systems

🧪 Learning & Use Cases

This project is ideal for:

🧑‍💻 Embedded AI experimentation

🤝 Human-Computer Interaction (HCI) research

🧠 Voice-based interfaces

🏫 Engineering mini / major projects

🤖 Smart assistants & robotics prototypes

🔮 Future Enhancements

🗣️ Wake-word detection

🌐 Offline language models

🎭 More facial expressions

🎚️ Custom personalities

📡 IoT and sensor integration

⭐ Final Note

This project demonstrates practical AI deployment on embedded hardware, combining speech, vision, animation, and intelligence into a compact Raspberry Pi system.
