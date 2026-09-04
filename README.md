# Bun + Base UI shadcn registry template

A template for running your own [shadcn registry](https://ui.shadcn.com/docs/registry) with [Bun](https://bun.com) and [Base UI](https://base-ui.com).

This repository is based on the official [shadcn registry template](https://github.com/shadcn-ui/registry-template). It is configured for the `base-nova` shadcn style and uses Base UI primitives instead of Radix UI.

## Requirements

- Bun 1.4.0 (the latest stable release when this template was created)

Install Bun on macOS, Linux, or WSL:

```bash
curl -fsSL https://bun.com/install | bash
```

## Getting started

Create a repository with GitHub's **Use this template** button, then run:

```bash
bun install
bun run dev
```

Open [http://localhost:3000](http://localhost:3000) to preview the registry.

## Build the registry

Edit `registry.json` and add source files under `registry/base-nova`, then generate the installable JSON files:

```bash
bun run registry:build
```

The generated registry items are written to `public/r`. Commit them whenever their source changes.

## Add shadcn components

The `components.json` file selects Base UI through the `base-nova` style. Add components with Bun:

```bash
bunx --bun shadcn@latest add button
```

See the [shadcn registry documentation](https://ui.shadcn.com/docs/registry) and [Base UI component documentation](https://base-ui.com/react/components) for more details.
