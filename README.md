# Model Context Protocol (MCP) Configuration
Reference for servers: https://github.com/modelcontextprotocol/servers

This repository contains configuration for Model Context Protocol (MCP) servers. Currently configured servers:

## Time Server
A Docker-based MCP server for handling time-related queries and conversions.

## GitHub Server
A Docker-based MCP server for interacting with GitHub. This server requires a GitHub Personal Access Token for authentication.

## Setup

1. Make sure you have Docker installed
2. Pull the required MCP server images:
   ```bash
   docker pull mcp/time
   docker pull mcp/github
   ```
3. Configure your GitHub Personal Access Token in VS Code settings
4. The servers are configured to run with the following capabilities:
   - Time server: Handles time queries and conversions
   - GitHub server: Performs GitHub operations with authentication
   - Terminal server (custom): Runs command given in terminal

## Security Note
The GitHub Personal Access Token is stored securely using VS Code's input mechanism and is not committed to the repository.

## Usage
The servers can be used through the Model Context Protocol interface in VS Code. Example queries:
- Time-related queries (e.g., "What time is it in Tokyo?")
- GitHub operations (e.g., "List my repositories", "Create a new issue")
- Terminal operations (e.g, Execute echo Hello World in terminal)
