# 1. Command Line

### `init` : Initialize and Healthcheck

- Sets up the project by importing the configuration folder, and makes necessary changes to `configure.jsonc`.
- If run inside an already initialized directory, it will create the necessary sub-folders as defined.

### `debug` : Compiles with full verbosity and traceability

- Verbose output
- Traceable class-names and properties.
- Larger output size
- Use `debug -w` for live compilation with identical output.

### `preview` : Optimized compilation for lightweight builds:

- Hashed class-names (≥ 3 characters)
- Minified CSS.
- Partial dependency resolution
- Optimized for minimal class footprint
- Use `preview -w` for live compilation.

## Developer Commands

### `server` : Starts language server

- Helps in active language assistance in editors.
- Start server, use `help` for available command list.
- Used by extension developers.

## Experimental Commands

### `iamai` : Communication bridge for AI Agents

- Helps in context aware styling by AI Agnets.
- This command is a combination of `preview` and `server` commands.
