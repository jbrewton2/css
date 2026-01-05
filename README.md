# Contract Security Studio (CSS) — Hub

This repo is the top-level entry point for the CSS project.

## Repositories
- **Backend (API / FastAPI / Container Apps):**
  https://github.com/jbrewton2/css-backend

- **Frontend (React/Vite SPA):**
  https://github.com/jbrewton2/css-frontend

- **Infra (local Docker Compose + notes):**
  https://github.com/jbrewton2/css-infra

## Current Azure Dev Deployment (working)
- **UI:** https://css-dev.shipcom.ai
- **API health:** https://css-dev.shipcom.ai/api/health

## Current Architecture (dev)
- Frontend: Azure Storage Static Website
- Edge routing + TLS: Azure Front Door
- Backend: Azure Container Apps (FastAPI)
- Auth: Entra ID (MSAL in frontend) + JWT validation in backend
- Routing:
  - /* -> static website
  - /api/* -> backend

## Target Enterprise Ingress (planned)
Option A (cleaner): Internal-only Container Apps ingress behind enterprise chain (Palo Alto / App Gateway / Private Endpoint).
(See architecture diagram and delta table in project documentation.)
