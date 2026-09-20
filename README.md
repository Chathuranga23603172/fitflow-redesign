# FitFlow Redesign

AI-powered fitness tracking app: personalised workouts, private social circles,
and camera-based nutrition logging. Built for IT3060 HCI Lab Exercise 05.

## Problem
FitFlow lost users (rating 4.6 to 3.8, 68% dropped after onboarding). Research
showed a personalisation gap, social isolation, high logging friction and low motivation.

## Tech Stack
| Layer | Technology |
|---|---|
| Mobile/Web | React Native (Expo, TypeScript) + React Native Web |
| Backend API | NestJS (Node.js, TypeScript) |
| AI service | FastAPI (Python), TensorFlow Lite on-device |
| Database | PostgreSQL (+ pgvector), Redis |
| Auth | Firebase Authentication (Identity Platform) |
| Storage | S3-compatible object storage |
| Push | FCM / APNs |

## Repository Structure
- `frontend/` mobile and web client
- `backend/` core API and real-time gateway
- `ai-service/` workout engine and food recognition
- `database/` schema and migrations
- `docs/` comparison matrix, architecture, ADRs

## Documentation
- [Tech stack summary](docs/tech-stack-summary.md)
- [Technology comparison matrix](docs/comparison/technology-comparison-matrix.md)
- [Architecture diagram](docs/architecture/architecture-diagram.png)
- [ADR-001](docs/decisions/ADR-001-tech-stack.md)

## Security and Privacy
GDPR/CCPA-aligned: consent management, encryption in transit and at rest,
data minimisation, right to erasure.

## Course
IT3060 Human Computer Interaction, SLIIT, Semester 2 2026.