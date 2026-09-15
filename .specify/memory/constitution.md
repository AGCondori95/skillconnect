<!--
Sync Impact Report
- Version change: 0.0.0 -> 1.0.0
- Modified principles: placeholder principles -> SkillConnect Mission, TypeScript Quality and Safety, Next.js Architecture Discipline, Tailwind-First UI Standards, Testability and Naming Discipline
- Added sections: Additional Constraints, Development Workflow, Governance
- Removed sections: all placeholder sections from the generic template
- Templates requiring updates: .specify/templates/plan-template.md ✅ updated, .specify/templates/spec-template.md ✅ updated, .specify/templates/tasks-template.md ✅ updated, .specify/templates/commands/*.md ⚠ pending (no command templates are present in this repository)
- Follow-up TODOs: none
-->

# SkillConnect Constitution

## Core Principles

### I. Learner-First Community Value
SkillConnect exists to connect learners with teachers in a trusted and useful way. Every product decision must support honest skill discovery, respectful collaboration, and safe growth for both people who teach and people who learn.

This principle is non-negotiable because the product's value depends on trust. Features that add friction, reduce clarity, or create confusion about skill fit are rejected unless the team can show a clear user benefit and a safer alternative.

### II. TypeScript Quality and Safety
All application code MUST use TypeScript in strict mode. Explicit `any` is prohibited in production code, and the team MUST prefer precise types, interfaces, unions, generics, and validation at boundaries.

This standard keeps the codebase predictable as the app grows. Every new module, API contract, UI component, and shared helper must be typed clearly enough that the compiler catches mistakes before they reach users.

### III. Next.js Architecture Discipline
The project MUST use Next.js with the App Router and TypeScript. Server components are the default for data fetching and static or shared rendering, while client components are allowed only when browser interactivity, event handlers, or client-side state are required.

File-based routing is mandatory, and route structure should reflect user-facing features. The team MUST keep routing, component boundaries, and data flow understandable and consistent with Next.js conventions instead of introducing custom app architecture patterns without clear justification.

### IV. Tailwind-First UI Standards
The app MUST use Tailwind CSS as the default styling system. Utility-first classes are required for layout, spacing, typography, and state styling unless a necessity for custom CSS is documented and justified.

This principle keeps the interface consistent, readable, and maintainable. When styling becomes complex, the team should prefer reusable component patterns and small, intentional utility composition over broad custom CSS or one-off overrides.

### V. Testability, Naming, and Maintainability
Every user-facing feature MUST be testable and clearly named. Teams MUST write or update tests for changed behavior, use descriptive component and function names, and keep file and folder naming consistent with the project conventions.

Naming conventions for this repo are:
- components: PascalCase
- functions and variables: camelCase
- constants: UPPER_SNAKE_CASE
- route folders and feature directories: lowercase kebab-case
- files: descriptive names that reflect responsibility, not implementation noise

This keeps the codebase easier to navigate and reduces the risk of accidental regressions during feature work.

## Additional Constraints

- Required stack: Next.js App Router, TypeScript, Tailwind CSS, Firebase (Firestore for data, Firebase Authentication for auth).
- No custom CSS should be introduced unless it is required for a specific cross-cutting design need.
- Client logic MUST be isolated to the smallest possible boundary; server-side work remains the default when it is sufficient.
- Data contracts, prop shapes, and request/response payloads MUST be validated and kept explicit.
- Accessibility, responsiveness, and clear user feedback are required for all core user flows.
- Feature work MUST prioritize the learner-teacher matching experience over unrelated abstraction or speculative architecture.

## Development Workflow

- Work MUST be completed on feature branches named `feature/<short-description>`.
- Branches MUST be scoped to a single concern or user story whenever possible.
- Pull requests are REQUIRED before any merge into `main`.
- Every pull request MUST receive at least one approving review before merge.
- Changes MUST include relevant tests, lint validation, and evidence that they satisfy the feature requirements.
- Large or risky changes MUST be split into smaller, reviewable increments.
- The team MUST update relevant documentation when behavior or workflow changes materially.

## Governance

This Constitution governs all SkillConnect engineering and product work. It supersedes informal practices, local shortcuts, and undocumented exceptions when those practices conflict with the rules below.

Amendments require a documented change in the constitution, a review by the team, and a pull request with clear rationale for the update. Major governance changes MUST include a migration or implementation note so contributors understand what changed and how to comply.

Compliance is reviewed during pull request assessment. A pull request may not be merged if it violates the required stack, TypeScript standards, testing expectations, naming conventions, or collaboration workflow. The team MUST prefer simple, understandable solutions over clever ones that hide complexity.

**Version**: 1.0.0 | **Ratified**: 2026-09-15 | **Last Amended**: 2026-09-15
