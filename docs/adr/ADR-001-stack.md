# ADR-001 — Frontend Technology Stack

## Status
Accepted

## Context
O InsureHub é um projeto que tem como objetivo simular um ambiente corporativo moderno, aplicando práticas atuais de desenvolvimento frontend.

A stack escolhida deveria atender aos seguintes requisitos:

- Escalabilidade
- Componentização
- SSR
- SSG
- Server Components
- Type Safety
- Gerenciamento moderno de estado
- Cache de dados
- Design System
- Preparação para Micro Frontends

## Decision
A stack principal do projeto será composta por:

### Next.js (App Router)
- SSR
- SSG
- Server Components
- Metadata
- Server Actions

### TypeScript
- Segurança de tipos
- Melhor DX
- Escalabilidade

### TailwindCSS
- Velocidade
- Padronização
- Design Tokens

### shadcn/ui
- Componentes desacoplados
- Acessibilidade
- Alta customização

### Radix UI

### Zustand
- API simples
- Pouco boilerplate
- Escalável com slices

### TanStack Quer
- Cache
- Retry
- Invalidação
- Sincronização com servidor

### Framer Motion

## Alternatives Considered
### React + Vite
Vantagens
- Mais simples
- Build rápido

Motivo da não escolha
- O projeto exige SSR e Server Components

### Redux Toolkit
Vantagens
- Excelente para aplicações grandes

Motivo da não escolha
- O escopo atual favorece uma solução mais enxuta

### Styled Components
Motivo da não escolha
- O Tailwind oferece maior consistência com Design System baseado em tokens

### React Context
Motivo da não escolha
- Não é ideal para gerenciamento de estado global complexo

## Consequences
Benefícios

- Arquitetura moderna.
- Escalabilidade.
- Performance.
- Boa experiência de desenvolvimento.
- Fácil evolução.

Trade-offs

- Curva de aprendizado maior.
- Maior quantidade de ferramentas.
- Configuração inicial mais complexa.

## Future Revisions
Esta ADR deverá ser revisada quando:

- houver adoção de Micro Frontends;
- mudança na estratégia de gerenciamento de estado;
- alteração significativa na stack frontend.