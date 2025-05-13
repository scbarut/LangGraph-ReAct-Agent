# LangGraph React Agent for Tool-Augmented Reasoning

This project implements a LangGraph-based reactive agent powered by **Gemini 2.0 Flash**. It handles complex user queries using memory, conditional logic, and powerful external tools — including the ability to process content from files provided via URL.

## 🔍 Key Features

- 🌐 **Ask questions by providing a file URL**  
  Users can provide a direct URL to a Python script, MP3 audio file, or Excel spreadsheet. The agent automatically downloads and analyzes the content to respond accurately.

- 🛠️ **Integrated tools for enhanced reasoning**
  - **Wikipedia Search** – Retrieves relevant information from Wikipedia.
  - **Tavily Web Search** – Performs web searches for live content.
  - **Commutative Check Tool** – Verifies if two mathematical expressions are commutative.

- 🤖 **LLM-Powered with Gemini 2.0 Flash**  
  Responses are generated using Gemini 2.0 Flash, a fast and efficient large language model suited for real-time interactions.

- 🔄 **Graph-based flow** using LangGraph  
  Assistant decisions and tool calls are managed through conditional state transitions.

- 🧠 **Memory support** via `MemorySaver`  
  Maintains multi-turn conversation context throughout the session.

- 📊 **Graph visualization** using Mermaid diagrams

## ⚙️ How It Works

The agent is built using LangGraph’s `StateGraph`, consisting of:
- An `assistant` node powered by Gemini 2.0 Flash
- Conditional edges to transition to tool nodes based on user intent
- Support for looping between tool results and assistant follow-ups
- Automatic file downloading and parsing for supported formats (Python, MP3, Excel)

