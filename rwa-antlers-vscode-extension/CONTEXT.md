# RWA Antlers VS Code Extension docs context

Use this context only when working on extension docs under:

- `rwa-antlers-vscode-extension/**`
- `statamic/rwa-antlers-vscode-extension.mdx`

## Source of truth

Before documenting extension behavior, inspect the actual extension source.

- Local source: `~/documents/RWA-Statamic-plugin`
- GitHub: `https://github.com/ShentoHendriks/RWA-Statamic-plugin`

Useful source files:

- `README.md` — product overview and high-level behavior
- `features.md` — feature inventory and behavior notes
- `package.json` — commands, keybindings, extension contribution points
- `src/features/**` — extension-side implementation behavior
- `server/features/**` — diagnostics and language server behavior
- `test/extension.test.ts` — expected behavior examples

Do not invent extension behavior. If behavior is unclear, inspect the source or ask the user.

## Mint formatting preferences

Use the most scannable Mint component for the job:

- `<Steps>` / `<Step>` for workflows and command sequences
- `<Tree>` for file and directory structures
- Tables for mappings, comparisons, and conventions
- `<Info>` for helpful context and mental models
- `<Warning>` for caveats, limitations, and shortcut requirements
- `<Note>` for small reminders
- `<Card>` / `<CardGroup>` for navigation or summaries
- Avoid heavy accordions unless details are optional

Prefer code blocks for Antlers, YAML, shell commands, and exact file contents.

## Current extension docs order

1. `rwa-antlers-vscode-extension/overview`
2. `rwa-antlers-vscode-extension/getting-started`
3. `rwa-antlers-vscode-extension/project-aware-intellisense`
4. `rwa-antlers-vscode-extension/working-with-partials`
5. `rwa-antlers-vscode-extension/page-builders-with-replicator-sets`

## Documentation checklist

Before finishing an extension docs change:

- Verify behavior against `~/documents/RWA-Statamic-plugin` when documenting extension functionality.
- Use Mint components where they improve scanning.
- Add new pages to `docs.json` when they should appear in navigation.
- Remove or update links to deleted pages.
- Run `npm run broken-links` from the docs repo.
