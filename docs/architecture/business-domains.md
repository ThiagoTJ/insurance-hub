# Business Domains

## Purpose
 Este documento define os domínios de negócios do InsuranceHub e estabelece os limites de responsabilidade entre cada módulo da aplicação.

 A adoção de uma arquitetura orientada a domínio (Feature First) tem como objetivo organizar o sistema de acordo com as funcionalidades do negóciom, em vez de sua implementação técnica. Essa abordagem favorece alta coesão, baixo acoplamento e facilita a evolução da aplicação para arquiteturas mais complexas, como Micro Frontends.

 Cada domínio representa uma área funcional independente do sistema e possui responsabilidades, componentes, serviços e regras de negócios próprias.

## Domain Overview
O InsuranceHub será inicialmente composto pelos seguintes domínios:

- **Auth:** Gerenciamento da autenticação, autorização e sessão do usuário.

- **Dashboard:** Exibição consolidada das principais informações do usuário autenticado.

- **Products:** Catálogo de produtos de seguros disponiveis para contratação.

- **Quotes:** Simulação e geração de cotações de seguros.

- **Profile:** Gerenciamento dos dados do usuário autenticado.

- **Shared:** Recursos reutilizáveis compartilhados entre todos os domínios.

*O domínio **Admin** não fará parte do MVP e será implementado em uma versão futura*.

## Domain Responsibilities
### Auth
**Responsabilidades**
- Login
- Logout
- Refresh Token
- Recuperação de senha
- Cadastro de usuário
- Controle da sessão
- Controle de permissões

**Não é responsável por**
- Gerencimento do perfil
- Produtos
- Cotações

### Dashboard
**Responsabilidades**
- Consolidar informações do usuário
- Exibir resumo de contratos 
- Exibir últimas cotações
- Exibir indicadores rápidos

**Não é responsável por**
- Alterar dados do usuário
- Executar regras de negócio
- Gerenciar produtos

### Products
**Responsabilidades**
- Listagem de seguros
- Consulta de detalhes
- Categorias
- Busca
- Filtros

**Não é responsável por**
- Simulações
- Contratações
- Sessão do usuário

### Quotes
**Responsabilidades**
- Simulação de seguros
- Cálculo de valores
- Histórico de cotações
- Seleção de coberturas

**Não é responsável por**
- Cadastro de produtos
- Gerenciamento do usuário
- Autenticação

### Profile
**Responsabilidades**
- Dados pessoais
- Atualização cadastral
- Alteração de senha
- Preferências do usuário
- Avatar

**Não é responsavel por**
- Login
- Produtos
- Simulações

### Shared
**Responsabilidades**
- Design System
- Componentes reutilizáveis
- Hooks compartilhados
- Tipos globais
- Utilitários
- Constantes
- Helpers

*O domínio **Shared** não possui regras de negócio. Seu objetivo é centralizar recursos reutilizáveis utilizados pelos demais domínios.*

## Domain Dependencies
Os domínios deverão possuir o menor número possível de dependências entre si.

A comunicação entre eles ocorrerá por contratos bem definidos, evitando dependências circulares.

### Dependências previstas
- **Domain:** Depends On
- **Auth:** Shared
- **Dashboard:** Auth, Products, Quotes, Shared
- **Products:** Shared
- **Quotes:** Auth, Products, Shared
- **Profile:** Auth, Shared
- **Shared:** Nenhum

## Future Evolution
A arquitetura foi planejada para suportar crescimento contínuo.

Conforme o sistema evoluir, novos domínios poderão ser adicionados, como:
- Admin
- Contracts
- Notifications
- Payments
- Reports

Além disso, cada domínio poderá ser extraído para um Micro Frontend independente,
mantendo comunicação por contratos definidos e compartilhando apenas recursos comuns, como o Design System e bibliotecas utilitárias.

Essa estratégia permitirá deploys independentes, maior escalabilidade e autonomia entre equipes de desenvolvimento.

## Design Principles
A arquitetura do InsuranceHub seguirá os seguintes princípios:
 - **Single Responsibility:** cada domínio tem uma responsabilidade principal.
 - **High Cohesion:** elementos relacionados permaneceram juntos.
 - **Low Coupling:** minimizar dependências entre domínios.
 - **Feature First:** organização baseada em funcionalidades.
 - **Reusability:** componentes, hooks, tipos e utilitários comuns deverão ser compartilhados por meio do domínio Shared.
 - **Scalability:** estrutura preparada para crescimento.
 - **Maintainability:** o código deverá permanecer legível, previsível e de fácil evolução ao longo do tempo.
 - **Separation of Concerns:** Cada camada da aplicação deverá possuir responsabilidades claramente definidas, evitando mistura entre regras de negócios, interface e infraestrutura.