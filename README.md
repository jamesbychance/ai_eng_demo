# AI Agent Demo Notebooks

This repository contains two Jupyter notebooks demonstrating different approaches to building AI agents.

## Notebooks

### 1. agent_with_python.ipynb
A simple ReAct (Reasoning and Acting) agent built from scratch using Python and OpenAI's API. This notebook demonstrates:

- **Basic Agent Architecture**: Simple conversational AI wrapper with conversation history
- **ReAct Pattern**: Structured loop of Thought → Action → PAUSE → Observation → Answer
- **Custom Tools**: Calculator and dog breed weight lookup functions
- **Manual Loop Implementation**: Shows the step-by-step process of agent reasoning

**Key Features:**
- Built from scratch to understand core concepts
- Manual action parsing and execution
- Simple tool registry system
- Example queries about dog weights and calculations

### 2. agent_with_langGraph.ipynb
A more sophisticated agent implementation using LangGraph framework with advanced capabilities. This notebook demonstrates:

- **LangGraph Framework**: Professional-grade agent architecture using StateGraph
- **Tool Integration**: Tavily search API integration for web searches
- **State Management**: Typed state handling with message history
- **Error Handling**: Graceful handling of hallucinated tool calls
- **Conditional Logic**: Smart routing between LLM calls and tool execution

**Key Features:**
- Production-ready agent architecture
- Web search capabilities via Tavily API
- Visual graph representation of agent workflow
- Complex multi-step reasoning (e.g., Super Bowl winner → headquarters location → state GDP)

### 3. mcp_server_simple.ipynb
- A very simple MCP server for claude to communicate with
- Must not be run in the notebook!
- Code must be run as server.py (python file)

## Requirements

Both Agentic notebooks require:
- OpenAI API key
- Python environment with required packages
- `.env` file with API credentials

**For agent_with_python.ipynb:**
- `openai`
- `python-dotenv`
- `httpx`

**For agent_with_langGraph.ipynb:**
- `langgraph`
- `langchain-openai`
- `langchain-community`
- `python-dotenv`

## Usage

1. Set up your environment variables in a `.env` file
2. Install required dependencies
3. Run the agentic notebooks in Jupyter, the MCP notebook as a python file (server.py)
4. Follow the examples or modify queries as needed

## How to use these files

Start with `agent_with_python.ipynb` to understand the fundamentals, then explore `agent_with_langGraph.ipynb` to see how professional frameworks handle complexity and provide additional capabilities. Then have a look at `mcp_server_simple.ipynb` to see how a admittedly very simple MCP server is deployed.
