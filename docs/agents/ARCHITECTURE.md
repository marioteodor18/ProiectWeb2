# Architecture — ProiectWeb2

<!-- graffino-agentic:begin v1 -->
> How this repo is built, generated from the code at backfill and kept current by
> whoever changes the structure. The code wins: when this page is wrong, fix it.
<!-- graffino-agentic:end -->

## Overview
Web application project (ProiectWeb2).
All server-side components and data persistence run in containerized environments.

```text
[Client / Browser]
        │
        ▼ (HTTP)
[Containerized Server Service]
        │
        ▼
[Containerized Database / Storage]
```

## Parts
| Part | Path | Responsibility | Talks to |
|---|---|---|---|
| Server | docker-compose.yml | Server runtime orchestration | Host, Network |

## Data flow
1. Client sends request to exposed server container port.
2. Server process handles request and accesses containerized storage if needed.
3. Server returns response to client.

## State and storage
| What | Where | Owner | Notes |
|---|---|---|---|
| Application data | Docker volume / container | Server service | Persisted via volume |

## Configuration
| Name | Where set | Used by | Notes |
|---|---|---|---|
| COMPOSE_PROJECT_NAME | .env / docker-compose.yml | Docker Compose | Service naming |

## Build, deploy, runtime
Server services built or pulled through Docker Compose. Runs as local containers.

## Boundaries
Container network boundary isolates server processes and databases from direct host exposure.
