# mcp-notes-server

A small MCP server exposing my notes to Claude Desktop

Started as a weekend hack, grew on me.

## Highlights

- Includes a Claude Desktop config snippet with absolute paths
- Atomic saves (temp file + os.replace) behind a write lock
- Every tool carries a real docstring, so clients get descriptions
- A missing note raises instead of returning the string 'not found'
- Notes path set by MCP_NOTES_FILE or --notes-file
- Five tools: add / get / update / delete / list notes

## Installation

```bash
pip install -r requirements.txt
```

## Usage

```bash
# claude_desktop_config.json  (use ABSOLUTE paths: Claude does not
# run from the repo directory, so a bare "server.py" is not found)
# {
#   "mcpServers": {
#     "notes-box": {
#       "command": "python",
#       "args": ["/abs/path/to/mcp-notes-server/server.py"],
#       "env": {"MCP_NOTES_FILE": "/abs/path/to/notes.json"}
#     }
#   }
# }
python server.py --help
```

## Project structure

```text
├── .github/
│   ├── workflows/
│   │   └── ci.yml
│   └── pull_request_template.md
├── docs/
│   ├── development.md
│   ├── roadmap.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── tests/
│   └── test_notes.py
├── .gitignore
├── CHANGELOG.md
├── LICENSE
├── requirements.txt
└── server.py
```

## FAQ

**Is this production ready?**  
It works for my use case; review the code before relying on it.

**Why no framework?**  
The stdlib covers what this project needs.

## License

MIT. Do whatever you want.
