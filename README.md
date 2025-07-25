# Claude Code Commands

Custom slash commands for Claude Code development workflows.

## Usage

Use these commands in Claude Code with `/command-name`:

- `/architect` - Systems architecture consultation
- `/critical:analyze` - Objective critical analysis
- `/critical:critique` - Critical code and design review
- `/critical:debate` - Structured debate and discussion
- `/explore` - Codebase exploration and understanding
- `/implement` - Feature implementation with TDD
- `/improve` - Code improvement and optimization workflows
- `/review:arch` - Architecture review and analysis
- `/review:code` - Code review and analysis
- `/secure` - Security analysis and hardening workflows
- `/setup` - Project setup and configuration
- `/tdd` - Test-driven development workflow
- `/ui` - UI/UX design and implementation
- `/workflow:base` - Base workflow patterns
- `/workflow:iter` - Iterative development workflow
- `/workflow:test` - Testing workflow patterns

## Installation

### Prerequisites

- [Claude Code](https://www.anthropic.com/claude-code) must be installed and configured

### Install Commands

1. Create the Claude Code commands directory if it doesn't exist:
   ```bash
   mkdir -p ~/.claude/commands/
   ```

2. Copy the commands to your Claude Code commands directory:
   ```bash
   cp -r commands/ ~/.claude/commands/
   ```

3. Verify the installation by checking that the commands directory contains the files:
   ```bash
   ls ~/.claude/commands/
   ```
   You should see the command files listed.

4. Restart Claude Code if it's currently running to load the new commands.

See the [slash commands documentation](https://docs.anthropic.com/en/docs/claude-code/slash-commands) for more details.

## Structure

Commands are organized in `commands/` with YAML front matter defining allowed tools and descriptions.