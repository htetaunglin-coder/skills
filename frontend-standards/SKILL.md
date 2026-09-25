---
name: frontend-standards
description: "Opinionated house rules for React, Next.js, TypeScript, and Tailwind code in a feature-based layout, covering what the Vercel skills leave out: colocation and extraction, the Tailwind cva ladder, comments and TSDoc, file order, magic literals and `as const` unions, conditional rendering, and per-request state. Use when writing or reviewing frontend components, hooks, feature folders, className props, comments, file layout, literals, conditional branches, or stores and providers."
license: MIT
---

# Frontend Standards

House rules that complement the Vercel skills. Every reference to a Vercel rule or to another skill carries a one-line meaning, so the rules read without them installed.

Precedence, in order. On a conflict, follow the higher item and name the conflict in one line of the reply.

1. An instruction in the task that names a choice: "use an `enum`", "keep the reason in the PR", "put it in `lib/format.ts`". A request to match the file, or to follow a note in it, leaves the choice to these rules. The per-request store in [state](rules/state.md) holds against any instruction, because it prevents a data leak.
2. The repository's own standards (`AGENTS.md`, `CLAUDE.md`, and whatever they point at). These rules fill the room the repository leaves.
3. Vercel `react-best-practices` for measured performance, `composition-patterns` for component APIs, the Next.js docs bundled in `node_modules/next/dist/docs/` for framework mechanics, the `shadcn` skill for component-library conventions. Matt Pocock's `codebase-design` for the shape of a hook, data module, or lib function interface (small interface, much behavior behind it, tested through it). Read the rule the task touches, not the whole skill.
4. These rules for default code shape and for where the result lives.

## Rules

| Rule | One line |
|---|---|
| [colocation](rules/colocation.md) | Narrowest scope that matches ownership today. Extract on a named problem, share on shared ownership. |
| [tailwind](rules/tailwind.md) | Classes stay on the element. Repetition is evidence, not a command. `cn` → map → `cva` by count. |
| [comments](rules/comments.md) | Code says the what and the how first. A comment is the residue: why, why-not, warning, contract, coupling, reference. |
| [file-order](rules/file-order.md) | Newspaper order: imports, shared constants and types, main export, sub-components, helpers. A part's own constant sits above it. `function` declarations keep it top-down. |
| [magic-literals](rules/magic-literals.md) | A literal stays inline when its meaning is on the line. It takes a name when a reader must decode it or a second reader appears. `as const` unions, no `enum`. |
| [conditional-render](rules/conditional-render.md) | First row that holds the branch: early return → ternary → map → sub-component → variable before JSX → IIFE last. A ternary never nests. |
| [state](rules/state.md) | Tool choice and store shape are the repository's. A store holding request data is created per request, inside its provider. |

Lint rule names and options per rule: [TOOLING.md](TOOLING.md). Primary sources per rule: [SOURCES.md](SOURCES.md).
