# Skills
A collection of skills I use in my day-to-day work, including custom skills I’ve created myself and useful resources I regularly rely on.

[![skills.sh](https://skills.sh/b/htetaunglin-coder/skills)](https://skills.sh/htetaunglin-coder/skills)

## frontend-standards

Opinionated house rules for React, Next.js, TypeScript, and Tailwind code in a feature-based layout: colocation and extraction, the Tailwind cva ladder, comments and TSDoc, file order, magic literals and `as const` unions, conditional rendering, and per-request state.

```bash
npx skills add htetaunglin-coder/skills
```

### Companion skills

The rules cite these skills by name, each with a one-line meaning, so they work without them. Install them for the full rule text:

```bash
npx skills add vercel-labs/agent-skills --skill vercel-react-best-practices vercel-composition-patterns
npx skills add shadcn/ui --skill shadcn
npx skills add mattpocock/skills --skill codebase-design
```

Framework mechanics come from the Next.js docs bundled in `node_modules/next/dist/docs/`, so no Next.js skill is needed. In Claude Code, the `vercel` plugin already ships the same `react-best-practices` rules, and the `mattpocock-skills` plugin ships `codebase-design`.
