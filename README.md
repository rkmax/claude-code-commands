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
- `/review:arch` - Architecture review and analysis
- `/review:code` - Code review and analysis
- `/setup` - Project setup and configuration
- `/tdd` - Test-driven development workflow
- `/ui` - UI/UX design and implementation
- `/workflow:base` - Base workflow patterns
- `/workflow:iter` - Iterative development workflow
- `/workflow:test` - Testing workflow patterns

## Installation

Copy the `commands/` directory to your Claude Code commands directory:

```bash
cp -r commands/ ~/.claude/commands/
```

See the [slash commands documentation](https://docs.anthropic.com/en/docs/claude-code/slash-commands) for more details.

## Structure

Commands are organized in `commands/` with YAML front matter defining allowed tools and descriptions.