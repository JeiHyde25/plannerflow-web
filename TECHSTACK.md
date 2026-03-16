
# PlannerFlow Frontend Technology Decisions

This document explains the architectural and technology choices for the **PlannerFlow Web** repository.
The goal is to document *why* certain tools and frameworks were chosen so future contributors understand the reasoning behind the stack.

---

# Project Goals

PlannerFlow is an AI-powered system that converts handwritten planner pages into structured digital schedules.

The frontend application is responsible for:

- scanning planner images
- sending images to the PlannerFlow API
- displaying extracted schedule data
- allowing users to edit planner entries
- exporting schedules to calendar systems

The frontend must therefore support:

- rapid UI development
- structured data editing
- strong typing for API contracts
- long-term maintainability

---

# Selected Technologies

## Next.js

Chosen as the primary web framework.

Reasons:

- Industry-standard React framework
- Built-in routing and server-side capabilities
- Excellent developer experience
- Strong ecosystem and community support
- Ideal for SaaS dashboards and productivity tools

Next.js also provides:

- optimized builds
- automatic code splitting
- API routes if needed later

---

## App Router

PlannerFlow uses the **Next.js App Router** instead of the legacy Pages Router.

Reasons:

- modern architecture supported by Next.js
- better layout and component composition
- improved data-fetching patterns
- future-proof for long-term development

---

## TypeScript

The project uses **TypeScript** for type safety.

Reasons:

PlannerFlow processes structured data such as:

- schedule blocks
- time ranges
- task lists
- planner extraction responses

TypeScript provides:

- compile-time error detection
- safer API integrations
- improved developer productivity
- clearer data contracts between frontend and backend

This is particularly important when working with AI-generated structured data.

---

## Tailwind CSS

Chosen as the primary styling framework.

Reasons:

- rapid UI development
- utility-first styling approach
- easier component styling
- small final bundle size due to tree-shaking
- ideal for MVP and iterative design

Tailwind allows fast creation of:

- forms
- dashboards
- timeline components
- planner editing interfaces

---

## ESLint

ESLint is included for code quality.

Reasons:

- enforces coding standards
- detects potential bugs early
- keeps code consistent across contributors

---

## Import Alias (@/*)

An import alias is configured:

@/*

Reasons:

Without aliases:

import Component from "../../../components/ui/Button"

With alias:

import Component from "@/components/ui/Button"

This improves readability and maintainability as the project grows.

---

# Technologies Not Included (Yet)

## Progressive Web App (PWA)

PWA support will be added later.

Reason:

Early development should focus on core functionality before adding installability and offline features.

---

## State Management Libraries

Libraries such as Redux or Zustand are not included initially.

Reason:

Next.js state and component state are sufficient for the MVP.

Additional state management will only be introduced if complexity increases.

---

# Backend Integration

The frontend communicates with the **PlannerFlow API**, which is implemented using FastAPI.

Example flow:

User scans planner
→ image sent to API
→ AI extraction performed
→ structured schedule returned
→ user edits schedule

---

# Long-Term Architecture Considerations

Future enhancements may include:

- drag-and-drop timeline editor
- real-time calendar sync
- planner analytics
- mobile camera optimizations
- offline planner editing

The chosen stack allows these features to be implemented without major architectural changes.

---

# Author

Harold Tago

GitHub: https://github.com/JeiHyde25
