# System Overview

This diagram provides a high-level view of the platform architecture.
It focuses on the core runtime components (frontend + backend),
their responsibilities, and the external integrations involved.

The goal is to communicate the system boundaries clearly without exposing
proprietary infrastructure details, endpoints, or internal environments.

---

## High-Level Architecture

```mermaid
flowchart LR

U[User Browser] --> FE[Frontend (SPA)<br/>React 18 + TypeScript<br/>Vite + Tailwind + shadcn/ui]

FE -->|HTTP fetch<br/>credentials: include| BE[Backend API<br/>Express.js + TypeScript]

BE --> S[Storage Layer<br/>IStorage abstraction<br/>MemStorage (current)]
BE --> E[Email Integration<br/>Nodemailer (SMTP)<br/>SendGrid (provider)]

FE --> A[Static Assets<br/>Images / Fonts / CSS]
FE --> M[Embedded Google Maps<br/>iframe loading=lazy]