# Sources

Primary sources behind each rule. Author blogs, official docs, and the skills on skills.sh; no AI-written summaries.

## colocation

Kent C. Dodds: AHA Programming, AHA Testing, Colocation, Inversion of Control, When to break up a component. Sandi Metz: The Wrong Abstraction. John Ousterhout: A Philosophy of Software Design, ch. 4 Modules Should Be Deep, ch. 7 Pass-Through Methods. Matt Pocock: codebase-design skill, the deletion test.

## tailwind

Tailwind docs: Styling with utility classes, Managing duplication; Theme variables; Detecting classes in source files. CVA docs: Variants. tailwind-merge: When and how to use it. shadcn skill rules: styling. Kent C. Dodds: AHA Programming. Sandi Metz: The Wrong Abstraction.

## comments

Kevlin Henney: Comment Only What the Code Cannot Say. John Ousterhout: A Philosophy of Software Design, ch. 12–16. Matt Pocock: codebase-design skill, interface as everything a caller must know. Steve McConnell: Code Complete, ch. 32. Martin Fowler: Refactoring, the Comments smell. Robert C. Martin: Clean Code, ch. 4. Hillel Wayne: Comment the Why and the What; Why Not Comments. antirez: Writing system software, code comments. Google: TypeScript Style Guide, Comments and documentation; Testing on the Toilet, To Comment or Not to Comment; Less Is More. Ellen Spertus: Best practices for writing code comments. sergiodxa: comments-meaningful-only. ASD-STE100 and plainlanguage.gov for wording.

## file-order

Robert C. Martin: Clean Code, ch. 3 The Stepdown Rule, ch. 5 Vertical Formatting. Steve McConnell: Code Complete, ch. 31.8 Laying Out Classes and Files. Google TypeScript Style Guide: Source file structure, Exports, Function declarations. Airbnb JavaScript Style Guide: Hoisting, Functions (the define-before-use position, resolved here by `function` declarations). MDN: Hoisting, Temporal dead zone, Modules. ESLint and typescript-eslint: `no-use-before-define`. Kent C. Dodds: Colocation. Dan Abramov: A Complete Guide to useEffect, hoisting functions that use no component scope.

## magic-literals

Martin Fowler: Refactoring, Replace Magic Literal. Robert C. Martin: Clean Code, ch. 17 G25 Replace Magic Numbers with Named Constants. Steve McConnell: Code Complete, ch. 12.1 Numbers in General. Google TypeScript Style Guide: Identifiers, Enums. Airbnb JavaScript Style Guide: Naming Conventions 23.10. TypeScript Handbook: Enums, Objects vs Enums; TypeScript 5.8 release notes, `--erasableSyntaxOnly`. Matt Pocock: enums vs `as const`. ESLint, typescript-eslint, Biome: `no-magic-numbers` rule docs. Tailwind docs: arbitrary values, theme variables.

## conditional-render

React docs: Conditional Rendering; Rules of Hooks. Kent C. Dodds: Use ternaries rather than && in JSX; When to break up a component into multiple components. Josh Comeau: Common Beginner Mistakes with React. Airbnb JavaScript Style Guide 15.6, 15.7; Airbnb React Style Guide, parentheses. ESLint `no-nested-ternary`; eslint-plugin-react `jsx-no-leaked-render`. Vercel `react-best-practices`: `rendering-conditional-render`, `rerender-no-inline-components`, `rendering-hoist-jsx`; `composition-patterns`: `patterns-explicit-variants`, `architecture-avoid-boolean-props`. The IIFE and map rows are house opinion; no primary source covers them.

## state

Zustand docs: Setup with Next.js (per-request store, no global stores, server components never touch the store); Initialize state with props. TkDodo: Zustand and React Context. Vercel `react-best-practices`: `server-no-shared-module-state`.
