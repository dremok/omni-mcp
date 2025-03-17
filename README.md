# OmniMCP

A Python-based Model Context Protocol (MCP) client that automatically discovers and connects to MCP servers, both local and remote.

## Features

- **Dynamic Server Discovery**: Automatically finds local and remote MCP servers
- **Multi-Server Support**: Connect to multiple MCP servers simultaneously
- **Tool Integration**: Aggregates tools from all connected servers
- **Claude Integration**: Seamless integration with Anthropic's Claude API
- **Convenient CLI**: Easy-to-use command-line interface

## Requirements

- Python 3.9+
- Anthropic API Key

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/omni-mcp.git
   cd omni-mcp
   ```

2. Create a virtual environment using uv:
   ```
   uv venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. Install dependencies:
   ```
   uv pip install -r requirements.txt
   ```

4. Create a `.env` file with your Anthropic API key:
   ```
   ANTHROPIC_API_KEY=your_api_key_here
   ```

## Usage

Run the client to discover and connect to available MCP servers:

```
python main.py
```

The client will:
1. Scan for local MCP servers in standard locations
2. Query remote MCP server registries
3. Connect to all available servers
4. Present a CLI interface for interacting with Claude using all available tools

## Architecture

- **Scanner**: Discovers MCP servers locally and remotely
- **Server Manager**: Handles connections to servers
- **MCP Client Core**: Manages tool registry and server communication
- **Claude API Handler**: Interfaces with the Anthropic API

## Roadmap

- [ ] Graphical user interface
- [ ] Server health monitoring and reconnection
- [ ] Custom server registry support
- [ ] Tool categories and filtering
- [ ] Security enhancements for remote servers

## License

MIT

## Acknowledgements

- [Model Context Protocol](https://modelcontextprotocol.io/)
- [Anthropic](https://www.anthropic.com/)
