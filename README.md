# A simple MCP server and client without any interaction with LLM
## MCP server
- MCP server name `String Reverser`
- A tool function called `reverse_string` that reverses a String and attaches my name pankaj to it
- mcp.run() in mcp_server.py runs the mcp server
## MCP client
- opens a session to mcp server using `stdio_client` in a read, write mode
- takes an input string and calls the tool `reverse_string` on mcp_server
- shows the result of tool call `reverse_string` back 
## Commands 
1. initialize the project with uv
```shell
uv init .
```
2. Install mcp[cli]
```shell
uv add "mcp[cli]"
```
3. Start mcp server

```shell
uv run mcp dev mcp_server.py
```
**Note**: In this example we don't need to manually start mcp_server or MCP inspector as we will use `mcp_client.py` to do take care of connecting to mcp server, take input string and call the tool `reverse_string` in `mcp_server.py` to reverse the string and send output result to the client.  
4. Start mcp_client
```shell
uv run mcp_client.py
```  
