# Shell Scripts

To create a shell script:
- Create a new file (usually with extension `.sh` or without an extension)
- At the top, add `#!/bin/sh`, `#!/bin/bash`, or any other path to the executable to use
- Write the contents of the script
- Run the following command on the script to allow execution:
```bash
chmod +x ./SCRIPT_NAME
```
- Execute the script:
```bash
./SCRIPT_NAME
```
 

## Common Settings

```bash
set -e  # Exit upon first error
set -x  # Print out each command before it is executed
```

## Utility Functions

```bash
# Function which changes directory to the location of this script.
cdToScriptDirectory() {
    cd "$(dirname "$0")"
}
```

```bash
# Function which verifies that an environment variable is set; exits otherwise.
#
# Args:
#   $1: Name of the environment variable
#   $2: Environment variable itself
#
# Example:
#   requireEnvVariable USERNAME ${USERNAME}
#
requireEnvVariable() {
    if [[ -z ${2+set} ]]; then
        echo "Error: Environment variable $1 is required."
	exit 1
    fi
}
```
