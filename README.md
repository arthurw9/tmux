# tmux
Tmux Tutorial / notes / cookbook

## Step 1
Organize your work:
* Socket:
  * Not used much?
* Session:
  * Can have many windows.
* Window:
  * Takes up the whole screen.
* Pane:
  * Part of the currently visible Window.

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
Edit `~/.tmux.conf` to customize tmux.

Then reload the config file with `Control-b :source-file ~/.tmux.conf`

| Feature | Command to put in `~/.tmux.conf` |
| ------- | ------- |
| Use control-left and control-right<br/>to navigate on the command line<br/>Doesn't work in copy mode. | `set-window-option -g xterm-keys on` |
| Drag the mouse to copy text to the tmux paste buffer<br/>Use shift drag for the normal system copy buffer | `set -g mouse on` |
| Use vi keys in tmux copy mode | `setw -g mode-keys vi` |

Scrollback and copy paste paste in tmux

| Action | Command |
| ------ | ------- |
| Enter tmux scrollback and copy paste mode. | `Control-b [` |
| Start selecting text to copy. | `<space>` |
| Copy selected text. | `<enter>` |
| Paste text. | `Control-b ]` |
