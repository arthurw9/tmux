# tmux
Tmux Tutorial / notes / cookbook

## Step 1
Organize your work:
* Socket: Not used much?
* Session: Can have many windows.
* Window: Takes up the whole screen.
* Pane: Part of the currently visible Window.

For now, lets use a new session for each project that we work on.
Each session can have many windows for each task/job in the project.

| Task | Key | Command
| ---- | --- | -------
| Create a new tmux session | | `tmux`
| Create a new window | `Control-b c`
| List and switch between windows | `Control-b w`
| Rename the current window | `Control-b ,`
| Detach from the tmux session. Everything stays running.| `Control-b d`
| What sessions are running? | | `tmux ls`
| Rename the current session | `Control-b $`
| Attach to the last session.<br/>Don't create a new one. | | `tmux a`
| Attach to a session called foo.<br/> Any unique prefix of the name will work. | | `tmux a -t foo`
| Is the session small? Do you see dots or periods?<br/> Are you attached somewhere else? Detach other clients. | | `tmux a -d -t foo`

## Step 2
Cut and paste  
Coming soon...
