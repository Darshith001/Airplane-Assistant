Airline AI Assistant (LLM + Tools + Multimodal UI)

An AI powered customer support assistant for an airline, built using OpenAI GPT models, tool/function calling, Text-to-Speech, image generation, and a Gradio multimodal interface.
This project demonstrates how to integrate LLMs with external tools, build conversational agents that perform real actions (like checking ticket prices), and enhance chat responses with speech and AI-generated images.

Features:
 Natural language conversational assistant for airline customers,
 LLM Tool Calling to fetch ticket prices dynamically,
 Automatic city-themed image generation (DALL-E 3),
 Text-to-Speech responses (OpenAI speech models),
 Gradio-based interactive UI with chatbot, image preview & audio,
 Clean pipeline architecture with modular functions,
 Supports future expansion (database queries, flight schedules, etc.)

Tech Stack:
Languages & Frameworks,
Python 3.10+,
Gradio – UI framework for multimodal apps,
SQLite3 (optional, for price database).

AI & LLM Tools:
OpenAI GPT-4.1-mini — core chat model,
OpenAI Function Calling — dynamic tool execution,
OpenAI DALL-E 3 — city-themed image generation,
OpenAI TTS (gpt-4o-mini-tts) — converts text replies to speech.

Utilities:
dotenv — environment variable management,
Pillow (PIL) — image decoding,
Base64 — handling image blobs.

UI Layout (Gradio)The interface includes:
Chatbot window,
City image preview,
Auto-playing audio module,
Textbox for user messages.

Workflow:
User sends message,
Added to chat history,
LLM responds,
Audio + image generated,
Gradio updates all outputs simultaneously.

Future Improvements:
Flight schedule lookup,
Real airline API integration,
Real-time pricing via external data,
User authentication,
Booking workflows.


Architecture:
User → Gradio UI → Chat Pipeline → OpenAI GPT Model
                                      │
                                      ├── Tool: get_ticket_price()
                                      │       (returns structured price info)
                                      │
                                      ├── Image Generator (DALL-E 3)
                                      │
                                      └── TTS Audio Generator

