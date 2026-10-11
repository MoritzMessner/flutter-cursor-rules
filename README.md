# Flutter MVVM Cursor Rules Guide

> [!IMPORTANT]
> **This repository is outdated and no longer maintained.**
> The Flutter and Dart teams now ship official AI tooling (skills, rules, MCP server and agent plugins). Use those instead:
>
> - **Get started developing with AI:** https://docs.flutter.dev/ai/get-started
> - **Official Flutter agent plugins, skills and rules:** https://github.com/flutter/agent-plugins
> - **Official Dart skills:** https://github.com/dart-lang/skills
> - **AI rules overview:** https://docs.flutter.dev/ai/ai-rules

## Recommended: official Dart & Flutter tooling

### Cursor

Install the official **Dart and Flutter** plugin. It bundles the skills and configures the Dart and Flutter MCP server:

- Marketplace: https://cursor.com/marketplace/flutter (**Add to Cursor**), or
- In a Cursor chat, run `/add-plugin dart-flutter`

For file-scoped rules, download the `.mdc` files from [flutter/agent-plugins/rules](https://github.com/flutter/agent-plugins/tree/main/rules) into your project's `.cursor/rules/`.

### Claude Code

```bash
claude plugin marketplace add flutter/agent-plugins
claude plugin install dart-flutter@dart-flutter
```

Rules are not loaded automatically; copy the ones you want into your project's `CLAUDE.md`.

### Other agents (Codex, Copilot, Antigravity, ...)

Install the skills into `.agents/skills`:

```bash
npx skills add flutter/agent-plugins --skill '*' --agent universal --yes
npx skills add dart-lang/skills --skill '*' --agent universal --yes
```

See https://docs.flutter.dev/ai/get-started for agent-specific setup, including the Dart and Flutter MCP server (`dart mcp-server`).

### Architecture / MVVM

The topic this repo originally covered is now handled by the official skill [`flutter-apply-architecture-best-practices`](https://github.com/flutter/agent-plugins/tree/main/skills/flutter-apply-architecture-best-practices), based on Flutter's recommended app architecture:

- https://docs.flutter.dev/app-architecture
- https://docs.flutter.dev/app-architecture/case-study

## Legacy rules in this repo

The `.cursor/rules/` folder still contains the original MVVM-focused Cursor rules (architecture overview, UI layer, domain/data layer, design patterns, best practices, testing). They are kept for reference only and will not be updated.

## License

MIT License - see [LICENSE](LICENSE) for details.
