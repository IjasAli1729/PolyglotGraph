# PolyglotGraph

PolyglotGraph is an automated, multi-language translation pipeline leveraging LangGraph to perform parallel text processing. By utilizing a state-based architecture, it translates input text into four target languages simultaneously and aggregates the final results[cite: 3].

## 🏗 Architectural Overview

The project uses a Directed Acyclic Graph (DAG) approach:
*   **Parallel Processing:** The input string is passed to four distinct translation nodes simultaneously[cite: 3].
*   **State Management:** A custom `state` (TypedDict) manages input and output strings for each language dynamically[cite: 3].
*   **Aggregation:** Once translation nodes complete, an `Aggregator` node compiles the results into a structured format[cite: 3].

## 📋 Features

*   **Multi-Language Support:** Translates to French, Spanish, Japanese, and Chinese in one execution flow[cite: 3].
*   **Asynchronous-ready:** Designed to scale by utilizing independent translation nodes[cite: 3].
*   **Robust State Handling:** Uses LangGraph's `StateGraph` to ensure data consistency across the pipeline[cite: 3].

## 🛠 Prerequisites

*   Python 3.12+
*   `langgraph`, `langchain-google-genai`
*   Google Gemini API Key

## 🚀 Installation & Usage

1. **Install Dependencies:**
```bash
   pip install langgraph langchain-google-genai python-dotenv
