# Tooling

What a linter or formatter holds for each rule, and what stays review work. The repository's own linter and config win; these are the names to look for. Checked 2026-09 against ESLint 9.39, typescript-eslint 8, Biome 2.3, eslint-plugin-react 7.37, Next 16.2, Tailwind 4, tailwind-merge 3.7, React types 19.2.

| Rule | Linter holds | ESLint | Biome | Review work |
|---|---|---|---|---|
| colocation | Layer direction: shared → features → app, features never import each other | `eslint-plugin-boundaries`, or `no-restricted-imports` patterns, with three element types and one allow-list | `noRestrictedImports` | The scopes, the two questions, the options gate |
| colocation | File size limit, generated and static-data files excluded | `max-lines` at 1,000 | `style/noExcessiveLinesPerFile` with `maxLines: 1000`; off by default, 300 when turned on bare | Which responsibility moves |
| comments | A doc that restates the name; a type in a tag | `jsdoc/informative-docs`; `jsdoc/no-types` | none | The delete test, the six kinds, the level |
| comments | A TODO whose bracketed condition is met, `TODO [2027-01-01]` or `TODO [-legacy-parser]` | `unicorn/expiring-todo-comments`; `no-warning-comments` reports every TODO with no view of an issue | none | A prose trigger, the issue reference, the wording |
| conditional-render | A bare boolean variable on the left of `&&` | `react/jsx-no-leaked-render`, off in `plugin:react/recommended`; on with `validStrategies: ["ternary", "coerce"]` it accepts comparisons and `!!` | none | The ladder |
| conditional-render | A nested ternary | `no-nested-ternary` | `style/noNestedTernary` | Which row replaces it |
| file-order | A `const` or `class` read at import time before its line; a `function` below its caller and a body reading a later `const` are allowed | `no-use-before-define` with `{ functions: false, classes: true, variables: false, allowNamedExports: false }` (`variables: false` ignores a reference from an inner function scope and still reports one in the same scope); or `@typescript-eslint/no-use-before-define` with the same plus `typedefs: false, ignoreTypeReferences: true` | `correctness/noInvalidUseBeforeDeclaration`, no options | The slots, ownership |
| file-order | Import order | formatter or import sorter | formatter | none |
| file-order | `perfectionist/sort-modules` orders by kind and name and conflicts with the ownership slot | off | n/a | n/a |
| magic-literals | Nothing. `no-magic-numbers` is frozen; it allows JSX numbers, variable initializers, and object values by default and reports every other literal in an expression or a call, so `radius * 2` and `5 * 60 * 1000` fail under any option set | `no-magic-numbers`, warning level when a repository wants it | `style/noMagicNumbers`, no options, ignores `2`, `10`, `24`, `60` | The whole gate; strings in every case |
| tailwind | Class order | `prettier-plugin-tailwindcss` with `tailwindFunctions: ["cn", "cva"]` | same plugin | The ladder, the three kinds of variable |
| state | Nothing | | | The per-request store |
