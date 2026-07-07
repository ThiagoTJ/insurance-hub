# Sprint 0 — Foundation & Architecture
## Objetivo da Sprint
A Sprint 0 teve como objetivo estabelecer toda a base arquitetural e organizacional do projeto InsureHub antes do início da implementação da aplicação.

Durante esta etapa foram definidas as principais decisões relacionadas à arquitetura, organização do repositório, fluxo de desenvolvimento e documentação, garantindo que as próximas Sprints possam focar na construção do produto sobre uma fundação sólida.

## Objetivos planejados
- Definir a visão do produto
- Identificar os principais domínios de negócio
- Projetar a arquitetura em alto nível
- Registrar as primeiras decisões arquiteturais (ADR)
- Definir a estratégia de organização do monorepo
- Padronizar o fluxo de desenvolvimento com Git
- Estruturar a documentação técnica do projeto

## Entregas realizadas
### Product Vision
Definição do propósito do InsureHub, público-alvo, objetivos de negócio, MVP e visão de evolução do produto.

### Business Domains
Mapeamento dos domínios de negócio e definição clara das responsabilidades de cada módulo da aplicação.

### System Overview
Documentação da arquitetura de alto nível, incluindo diagramas de fluxo, autenticação e integração entre frontend, BFF e APIs.

### ADR-001 - Frontend Tecnology Stack
Registro da decisão arquitetural da stack principal, justificando as tecnologias escolhidas e os trade-offs considerados.

### Monorepo Strategy
Definição da organização do repositório, estrutura de aplicações, pacotes compartilhados e estratégia de crescimento.

### Git Workflow
Padronização da estratégia de branches, commits, Pull Requests, releases e versionamento do projeto.

## Principais decisões arquiteturais
Durante esta Sprint foram tomadas as seguintes decisões:
- Utilização do Next.js como framework principal
- React com Typescript como base da aplicação
- Organização da arquitetura orientada a domínios (Feature First)
- Preparação da arquitetura para evolução em Micro Frontends
- Utilização de Backend For Frontend (BFF) como camada intermediária
- Estrutura do projeto em Monorepo
- Adoção de Conventional Commits
- Estratégia de desenvolvimento baseada em Feature Branch, Develop, Release e Main

## Conhecimentos adquiridos
Ao longo da Sprint foram consolidados conhecimentos relacionados a:
- Arquitetura de aplicações frontend
- Organização por domínios de negócio
- Registro de decisões arquiteturais utilizando ADR
- Estratégias de organização de monorepo
- Fluxos profissionais de Git e GitHub
- Importância da documentação como parte da engenharia de software
- Relação entre requisitos de negócios e decisões técnicas

## Desafios encontrados
Os principais desafios durante esta Sprint foram:
- Definir uma arquitetura preparada para crescimento sem adicionar complexidade desnecessária
- Organizar a documentação de forma que os documentos complementassem e não permanecessem isolados
- Estruturar um fluxo Git semelhante ao utilizado em ambientes corporativos
- Registrar decisões técnicas considerando seus benefícios e trade-offs

## Lições aprendidas
As principais lições obtidas nesta Sprint foram:
- A Arquitetura deve ser planejada para suportar mudanças futuras
- Documentar decisões é tão importante quanto implementá-las
- Toda escolha técnica envolve vantagens e desvantagens
- Um bom fluxo de desenvolvimento reduz riscos e melhora a qualidade das entregas
- Uma documentação bem estruturada facilita a evolução e manutenção do projeto

## O que pode ser melhorado
Para as próximas Sprints, pretende-se:
- Expandir os diagramas arquiteturais
- Criar novas ADRs para decisões futuras
- Automatizar validações de documentação
- Evoluir continuamente a organização da documentação

## Próximos passos
Na Sprint 1 serão iniciadas as implementações do projeto, incluindo:
- Configuração do ambiente Next.js
- Estrutura inicial do monorepo
- Configuração do Typescript
- ESLint e Prettier
- Tailwind CSS
- shadcn/ui
- Estrutura Feature First
- Primeiros componentes compartilhados

## Resultado da Sprint
A Sprint 0 foi concluída com sucesso.

Ao final desta etapa, o InsuranceHub possui uma base arquitetural consistente,
documentação integrada e um fluxo de desenvolvimento padronizado,
proporcionando segurança para o ínicio da implementação da aplicação nas proóximas Sprints.