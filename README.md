# Debugging NodeJS via Docker

These instructions assume following:
- Docker Engine and associated tools (e.g. docker and docker-compose) are present.
- VSCode is the development IDE in use.
- [Microsoft's Docker Extension](https://github.com/microsoft/vscode-docker) for VSCode is installed

Steps to demo debugging in docker-based NodeJS installation.
- Clone this repo
- Open VSCode against this cloned folder
- In the VSCode terminal, run `docker-compose --build up`
- `curl localhost:5000` to test server is running
- To attach the debugger to the running process:
  - Select the "Run And Debug" panel in VSCode
  - Select "Docker: Attach to Node" from the dropdown
  - Hit the green "Play" button to attach the debugger
  - Check the Debug Console window to confirm successful attachment
- To debug the code:
  - Open `src/server.js` in the editor and click in the margin of the line which reads `res.send('Hello world! \n');` to place a red breakpoint on it.
  - `curl localhost:5000` again to step into the `server.js` code
