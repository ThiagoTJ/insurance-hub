# Monorepo Strategy

## Purpose
O objetivo deste documento é definir a estratégia de organização do repositório do InsuranceHub.

A estrutura foi projetada para suportar a evolução contínua do projeto, permitindo o compartilhamento de código, configurações e bibliotecas entre diferentes aplicações, além de facilitar futuras expansões, como a adoção de Micro Frontends e novos serviços.

Este documento deve servir como referência para a organização do código e para a criação de novas aplicações e pacotes dentro do monorepo.

## Why Monorepo?
O InsuranceHub será desenvolvido como uma aplicação escalável e preparada para evoluções arquiteturais ao longo do tempo.

Durante sua evolução, novos módulos e aplicações poderão ser adicionados, como Backend for Frontend (BFF), Storybook, aplicações administrativas e outros serviços auxiliares.

Utilizar um monorepo permite que todos esses projetos compartilhem dependências, configurações e bibliotecas reutilizáveis em um único repositório, reduzindo duplicação de código e simplificando o gerenciamento do projeto.

**Benefícios**
- Compartilhamento de código.
- Compartilhamento de Design System.
- Compartilhamento de tipos.
- Versionamento único.
- Build centralizado.
- Facilidade para CI/CD.
- Evolução para Micro Frontends.

## Repository Structure
```
insurehub/

├── apps/
├── packages/
├── services/
├── configs/
├── docs/
├── scripts/
└── .github/
```

**apps** - Aplicações executáveis do projeto

**packages** - Bibliotecas compartilhadas

**services** - Serviços auxiliares e APIs

**configs** - Configurações compartilhadas

**docs** - Documentaçao do projeto

**scripts** - Scripts de automação

**.github** - Configurações do GitHub


## Applications
**web** - Interface principal do sistema

**bff** - Camada Backend For Frontend

**storybook** - Catálogo do Design System

## Shared Packages
**ui** - Componentes reutilizáveis

**design-tokens** - Tokens de design

**utils** - Funções utilitárias

**types** - Tipos compartilhados

**eslint-config** - Configuração padrão do ESLint

**tsconfig** - Configuração compartilhada do Typescript

## Shared Configurations
- ESLint
- Prettier
- Tailwind
- Husky

## Future Evolution
A organização proposta foi planejada para suportar a evolução do InsureHub sem a necessidade de grandes reorganizações estruturais.

Novas aplicações poderão ser adicionadas ao diretório apps, enquanto novas bibliotecas compartilhadas serão centralizadas em packages.

Essa abordagem favorece a escalabilidade da plataforma e reduz o impacto da inclusão de novos módulos ou equipes de desenvolvimento.

## Related Documents
- ADR-001
- Business Domains