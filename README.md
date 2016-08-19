# Advanced PS1
Example output:
```
some stdout output
✓ [2m16s] 08:57:05 raymond.schouten@mc16:~/github/advanced-ps1 $
```
```
some stdout output
✓ [2m16s] 08:57:05 raymond.schouten@mc16:~/github/advanced-ps1 (master) $
```
```
some terminated stdout output▼
✗ (1) [2m16s] 08:57:05 raymond.schouten@mc16:~/github/advanced-ps1 (master) $
```
```
some terminated stdout output▼
✗ (1: Catchall for general errors) [2m16s] 08:57:05 raymond.schouten@mc16:~/github/advanced-ps1 (master) $
```

# Features
- Configurable and colorized advanced PS1
- Adds a newline and marker to terminated stdout output if needed
- Shows last command status
- Shows last command exit code (with message if possible when enabled)
- Shows last command duration in human readable format
- Shows 12/24-hour formatted time
- Shows user (root has differently color), host and path
- Shows Git repository information (using __git_ps1)
- Shows prompt (root has different prompt)

# Options
- **ADVANCED_PS1_SHOWNEWLINE** - Show "newline" character and place prompt on new line when prompt was appended to last command output.
- **ADVANCED_PS1_SHOW0EXITCODE** - Always show exit code, even when it is 0.
- **ADVANCED_PS1_SHOWEXITCODEMESSAGE** - Show message if possible for exit code.
- **ADVANCED_PS1_SHOW0DURATION** - Always show duration, even when it is 0 seconds.
- **ADVANCED_PS1_SHOWTIME12H** - Show time in 12-hour format.

# Installation
Put the following lines in your ~/.bashrc file:
```sh
# Source advanced PS1.
source '/path/to/advanced-ps1';

# Enable advanced PS1 duration measurement.
trap '__advanced_ps1_debug_trap' DEBUG;

# Enable advanced PS1.
PROMPT_COMMAND='__advanced_ps1';
```
