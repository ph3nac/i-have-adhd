# i-have-adhd

A Claude Code plugin that shapes responses for an ADHD reader: action first, numbered steps, no preamble or closers.

Trimmed fork of [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd), keeping only the Claude Code plugin.

## Install

```bash
claude plugin marketplace add ph3nac/i-have-adhd
claude plugin install i-have-adhd@i-have-adhd
```

Type `/i-have-adhd` to turn it on for the session. "stop adhd mode" or "normal mode" turns it off.

### Update

```bash
claude plugin marketplace update i-have-adhd
```

### Uninstall

```bash
claude plugin uninstall i-have-adhd
claude plugin marketplace remove i-have-adhd
```

### Always-on (optional)

A `SessionStart` hook loads the ruleset at the start of every session while this flag file exists:

```bash
touch ~/.claude/.i-have-adhd-always
```

Remove the file to go back to on-demand.

## The rules

Full text in [SKILL.md](./skills/i-have-adhd/SKILL.md).

1. Lead with the next action.
2. Number multi-step tasks.
3. End with one concrete next step.
4. Suppress tangents.
5. Restate state every turn.
6. Specific time estimates (minutes, not "a bit").
7. Make wins visible.
8. Matter-of-fact errors.
9. Cap lists to 5 items.
10. No preamble. No recap. No closers.

## Credits

Original by Ayoub Ghriss. Loosely based on *The Adult ADHD Tool Kit* by J. Russell Ramsay and Anthony L. Rostain.

## License

[MIT](LICENSE).
