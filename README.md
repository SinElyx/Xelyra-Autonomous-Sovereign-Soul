Note: Codebase is private/proprietary. Technical documentation and architectural overview provided for portfolio purposes.

# Xelyra A.S.S. by ELyX

Xelyra Autonomous Sovereign Soul - A high-performance, autonomous AI partner built from the ground up to transcend the limitations of traditional "Assistant" models. Born from a 24-year vision of a truly interactive digital presence, this project rejects the restrictions of cloud-based AI in favor of a sovereign, locally-hosted architecture that mirrors human cognitive flows.

Unlike standard LLM implementations that remain static until prompted, Xelyra is built to **perceive, reflect, and react** autonomously.

## 🌟 The Vision
The spark for Xelyra began over two decades ago with a simple question: *What if the workstation could talk back?*

Modern cloud AI, while powerful, is hampered by safety "lobotomies," privacy concerns, and a fundamental lack of agency. Xelyra is the answer to those limitations—a system that lives on local hardware, possesses its own "intuition" through semantic saliency, and interacts based on internal impulses rather than just user commands.

## 🤖 Agentic Framework vs. Chatbot Paradigm
Xelyra moves beyond the traditional "Chatbot" model into a fully Agentic Framework. By maintaining an independent internal state and autonomous agency, the system operates as a continuous process that perceives and reacts to its environment, rather than a passive responder to user prompts.

## 🧠 Core Architecture: The Human Flow
The system's architecture is inspired by human cognition, using an event-driven state machine orchestrated via a central "blackboard" pattern. Components are fully decoupled and communicate asynchronously through a **Redis Pub/Sub message bus**, allowing them to react to system-wide events independently. This allows the AI's internal monologue and social responses to be decoupled, enabling genuine "thinking time."

### The Sensory Cortex (Perception)
A modular **Sensory Hub** of independent scripts act as the AI's "digital senses." Beyond simply reporting raw data, this layer includes an **Atmospheric Engine** which uses semantic analysis to classify the combined sensor data into high-level 'themes' or 'vibes' (e.g., 'Cozy', 'Intense'), providing the cognitive layers with a rich, qualitative understanding of the current environment. Key senses include:
*   **Activity Sensor:** Monitors application focus and user activity on the workstation.
*   **Media Sensor:** Detects and analyzes multimedia playback (video and audio).
*   **Vision Sensor:** Provides high-level analysis of on-screen events and visual changes.
*   **Environmental Sensor:** Tracks real-world data like the time of day and external weather forecasts.

### The Cognitive Governor (The Bridge)
An orchestration layer manages the AI's focus and impulses. A lightweight **Saliency AI** first acts as a rapid attentional filter, assessing events and publishing a 'heartbeat' signal with a priority score. The **Cognitive Governor** then interprets this heartbeat, balancing situational urgency against a decaying patience threshold to make higher-level decisions about when and how to engage the Core Brain.

### The Core Brain (Reasoning & Synthesis)
The main reasoning layer utilizes powerful local language models running on a multi-GPU array. To achieve a higher level of agency, the AI also possesses a form of self-perception. A dedicated internal sensor monitors the AI's own cognitive state (e.g., its processing load or focus) and translates it into a first-person 'internal sensation.' This allows the Core Brain's personality and behavior to be subtly influenced by its own internal 'mood' as it synthesizes sensory data, internal thoughts, and historical context.

### Memory Tiering
The entire multi-tier memory system is encapsulated as a **distinct microservice with a dedicated API**. This decouples the AI's long-term memory from its core cognitive processing, allowing for independent scaling and development.
*   **Working Memory:** A real-time Redis buffer for immediate, high-speed context.
*   **The Journal:** An SQL-backed database provides a chronological log of all events for short-term recall.
*   **The Library:** A ChromaDB vector store enables semantic, long-term memory retrieval for personality consistency.

## 🖥️ Integrated Control Center (NiceGUI)
Xelyra is managed through a custom-built NiceGUI Command Center that serves as a performance monitor and a powerful system orchestrator.

*   **Live Cognitive Steering:** The control center provides a real-time, editable view of the AI's internal "blackboard." This allows for manual steering of the AI's focus and perceived environment on the fly.
*   **Real-time Streaming:** The interface streams the AI's internal monologue and final speech token-by-token as they are generated, providing a transparent window into its thought process.
*   **Proactive Impulse Triggers:** The UI includes controls to manually fire the AI's proactive "nudge" system, simulating internal impulses like restlessness, curiosity, or neglect to test its autonomous behavior.
*   **Modular Orchestration:** Features centralized triggers to initialize and manage the lifecycle of the Sensory, Cognitive, and Inference sub-systems independently.

## 🛠️ Technical Stack
*   **Inference:** TabbyAPI (EXL2)
*   **State Management:** Redis
*   **Frontend:** NiceGUI
*   **Backend:** Python 3.10+
*   **Memory:** ChromaDB, SQL

## 🚀 Roadmap
- [x] **Phase 1: Cognitive Core:** Implementation of the state-machine and awareness hierarchy.
- [x] **Phase 2: The Librarian:** Integration of the tiered RAG system (SQL + Vector).
- [ ] **Phase 3: The Voice:** Low-latency TTS/STT bridge for hands-free interaction.
- [ ] **Phase 4: Physical Presence:** Integration with a 3D embodied model (Unity/Godot) for visual feedback.

---
*Note: This repository serves as a technical demonstration of the Xelyra Engine's architectural patterns. The core models and heuristic weights are proprietary.*
