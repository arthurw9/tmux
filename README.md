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

Create a new tmux session
```
tmux
```

Create a new window inside the session
```
Control-b c
```

List and switch between windows in the current session
```
Control-b w
```

Rename the current window
```
Control-b ,
```

Detach from tmux, everything stays running.
```
Control-b d
```

What sessions are running?
```
tmux ls
```

Rename the current session
```
Control-b $
```

Attach to the last session, don't create a new one.
```
tmux a
```

Attach to a session called foo. Any unique prefix of the session name will work.
```
tmux a -t foo
```
