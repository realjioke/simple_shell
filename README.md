# simple_shell

## Overview

**simple_shell** is a custom Unix shell implementation written in C. It provides a command-line interface that allows users to execute commands, manage processes, and utilize built-in functions, closely mimicking the behavior of the standard Unix shell.

## Features

- **Command Execution**: Executes commands located in the system's PATH.
- **Built-in Commands**: Includes `cd`, `env`, `setenv`, `unsetenv`, `exit`, and `alias`.
- **Input Handling**: Supports both interactive and non-interactive modes.
- **Environment Management**: Handles environment variables seamlessly.
- **Command Aliases**: Users can define and manage command shortcuts.
- **Error Handling**: Provides informative error messages for invalid commands or arguments.

## Files

- **main.c**: Entry point of the shell.
- **shell.h**: Header file containing function prototypes and macros.
- **_getline.c**: Custom implementation of the `getline` function.
- **execute.c**: Handles command execution.
- **builtins_env.c**: Built-in commands related to environment variables.
- **builtins_list.c**: List of all built-in commands.
- **builtins_more.c**: Additional built-in commands.
- **env_management.c**: Functions for environment variable management.
- **alias_management.c**: Functions to manage command aliases.
- **expansions.c**: Handles variable expansions.
- **find_in_path.c**: Searches for executable files in the PATH.
- **tokenize.c**: Tokenizes input strings.
- **helper_1.c**, **helper_num.c**, **helper_p.c**, **helper_str.c**: Utility functions.
- **macros.h**: Header file containing macros.
- **man_1_simple_shell**: Manual page for the shell.

## Installation

### Prerequisites

- GCC compiler

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/realjioke/simple_shell.git
   ```
2. Navigate to the project directory:
   ```bash
   cd simple_shell
   ```
3. Compile the source files:
   ```bash
   gcc -Wall -Werror -Wextra -pedantic *.c -o hsh
   ```

## Usage

- **Interactive Mode**:
  ```bash
  ./hsh
  ```
  After launching, type commands as you would in a standard shell.

- **Non-Interactive Mode**:
  ```bash
  echo "ls -l" | ./hsh
  ```
  or
  ```bash
  cat script.sh | ./hsh
  ```

## Built-in Commands

- `cd [directory]`: Change the current directory.
- `env`: Display the environment variables.
- `setenv [var] [value]`: Set an environment variable.
- `unsetenv [var]`: Remove an environment variable.
- `alias [name]='[value]'`: Define or display aliases.
- `exit [status]`: Exit the shell with a status code.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes. Ensure your code follows the project's coding standards and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

