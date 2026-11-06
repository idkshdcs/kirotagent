# Advanced MCP and Custom Tooling — Optional

Load only when the user asks about MCP/custom tooling or a recurring capability gap is materially blocking work. This is not part of the default web workflow.

## Discover and reuse first

1. Inspect only the MCP tools and local capabilities actually exposed to the current host. Read their real names, descriptions, schemas, and permission scope; never invent a tool or argument.
2. Prefer a direct existing tool or project command when it safely completes the task.
3. Compose existing primitives only when the combination adds clear value. Keep adapters narrow and task-focused.
4. Consider creating or registering an MCP server only when the host demonstrably supports local process execution, writable configuration, server loading/restart, and the necessary user permissions. Do not assume one capability proves another.
5. Validate the actual handshake/tool listing and one focused operation before relying on a new server. A generated server file is not a connected server.

Do not build or install an MCP server for a one-off operation that an available tool can already perform. Do not modify host-level configuration, install software, authenticate accounts, grant permissions, or restart services without the user's explicit action where required.

## Report limits plainly

State which tools/capabilities were actually available, what was tested, and what remains unsupported. Never claim that a tool is connected or authorized merely because its configuration or source file exists.
