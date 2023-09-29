# 0x05. Processes and signals
## Project Requirements
- Scripts must pass Shellcheck standards
- First line of all scripts should be exactly `#!/usr/bin/env bash`
- All your files should end with a new line
- All your Bash script files must be executable

## File Descriptions
**0-what-is-my-pid:** a Bash script that displays its PID

**1-list_your_processes:** a Bash script that displays a list of currently running processes

**2-show_your_bash_pid:** a Bash script that displays line containing the `bash` word, this allowing you to easily get the PID of your Bash process

**3-show_your_bash_pid_made_easy:** a Bash script that displays the PID, along with the process name, of processes which name contains the word `bash`

**4-to_infinity_and_beyond:** a Bash script that displays `To infinity and beyond` indefinitely

**5-kill_me_now:** a Bash script that kills `4-to_infinity_and_beyond` process

**6-kill_me_now_made_easy:** a Bash script that kills `4-to_infinity_and_beyond` process

**7-highlander:** a Bash script that displays `to infinity and beyond` indefinitely, with a `sleep 2` in between each iteration, and `I am invincible!!!` when receiving a SIGTERM signal

**8-beheaded_process:** a Bash script that kills the process `7-highlander
* **9. Process and PID file**
  * [100-process_and_pid_file](./100-process_and_pid_file): Bash script that creates the file `/var/run/myscript.pid` containing its PID and displays `To infinity and beyond` indefinitely.
  * Displays `I hate the kill command` upon receiving a `SIGTERM` signal.
  * Displays `Y U no love me?!` upon receiving a `SIGINT` signal.
  * Deletes the file `/var/run/myscript.pid` and terminates itself upon receiving the `SIGQUIT` or `SIGTERM` signal.
**10. Manage my process**
  * [manage_my_process](./manage_my_process): Bash script that writes `I am alive!` to the file `/tmp/my_process` indefinitely.
    * Sleeps two seconds in between each write.
  * [101-manage_my_process](./101-manage_my_process): Bash script that manages the [manage_my_process](./manage_my_process) script.
  * When passed the argument `start`:
    * Starts [manage_my_process](./manage_my_process).
    * Creates a file containing its PID in `/var/run/my_process.pid`.
    * Displays `manage_my_process started`.
  * When passed the argument `stop`:
    * Stops [manage_my_process](./manage_my_process).
    * Deletes the file `/var/run/my_process.pid`.
    * Displays `manage_my_process stopped`.
  * When passed the argument `restart`:
    * Stops [manage_my_process](./manage_my_process).
    * Deletes the file `/var/run/my_process.pid`.
    * Starts `manage_my_process`.
    * Creates a file containing its PID in `/var/run/my_process.pid`.
    * Displays `manage_my_process started`.
  * Otherwise, displays `Usage: manage_my_process {start|stop|restart}`.
`
