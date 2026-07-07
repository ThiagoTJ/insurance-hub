# Documentation

## Vision
- Product Vision

## Architecture
- Business Domains
- System Overview
- Monorepo Strategy

## ADRs
- ADR-001

## Roadmap
- Project Roadmap

## Contributing
- Git Workflow

## Documentation Flow
```
                         Product Vision
                                │
                ┌───────────────┴───────────────┐
                │                               │
        Business Domains               System Overview
                │                               │
                └───────────────┬───────────────┘
                                │
                         ADR-001 Stack
                                │
                                ▼
                      Monorepo Strategy
                                │
                                ▼
                         Git Workflow
                                │
                                ▼
                        Coding Standards
```

## Decision Traceability - (Rastreabilidade de Decisões)
- A Product Vision define que o sistema precisa ser escalável.
- O System Overview mostra uma arquitetura preparada para isso.
- A ADR-001 justifica a escolha do Next.js e da stack.
- O Monorepo Strategy explica como a estrutura suporta essa escalabilidade.