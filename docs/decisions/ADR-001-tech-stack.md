# ADR-001: Technology stack for the FitFlow redesign

**Status:** Accepted
**Date:** 20 September 2026

## Context
FitFlow is a fitness app losing users. The redesign needs cross-platform delivery,
AI personalisation, real-time social features, offline support and strong
health-data security, delivered by a mid-sized team quickly and cost-effectively.

## Decision
React Native (Expo, TypeScript) with React Native Web; NestJS as the core backend;
a separate FastAPI microservice for AI; PostgreSQL as the primary database with
Redis for caching and pub/sub; Firebase Authentication for identity.

## Alternatives considered
Flutter, Kotlin Multiplatform, Swift/SwiftUI (frontend); Express, Go (backend);
Firestore, MongoDB, DynamoDB (data); Cognito, Auth0, Supabase (auth).

## Consequences
- (+) One TypeScript codebase for mobile, web and API
- (+) Relational, auditable storage suits health and social data
- (+) ML stays in Python, independent of the main API
- (-) Two backend runtimes to operate and monitor
- (-) Some native features need native modules
- (-) Firebase Auth adds some vendor lock-in, mitigated by standard JWT verification

## Review trigger
Revisit if user volume or AI workload outgrows the modular monolith, or if enterprise SSO is required.