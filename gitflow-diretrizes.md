# GitFlow Diretrizes para o Módulo do Totem de Check-in do PrettyFlights

## 1. Visão geral
Este documento descreve as atividades realizadas para estruturar o projeto usando GitFlow e versionar a entrega da release `1.0.0` do módulo Totem de Check-in do PrettyFlights.

## 2. Cenário de aplicação do GitFlow
O módulo Totem de Check-in é um componente crítico que precisa chegar rapidamente à produção com qualidade e rastreabilidade.

Branches permanentes:
- `main`: código estável em produção.
- `develop`: integração contínua das features.

Branches temporárias:
- `feature/*`: desenvolvimento de recursos e melhorias.
- `release/*`: preparação de release sem interromper desenvolvimento.
- `hotfix/*`: correção emergencial no código em produção.

## 3. Passos realizados

### 3.1 Inicialização do repositório
Criei o repositório local com a documentação inicial e confirmei a conexão com o remoto GitHub configurado como `origin`.

### 3.2 Estrutura GitFlow
Defini os branches permanentes `main` e `develop` e criei o fluxo para futuras features, releases e hotfixes.

### 3.3 Desenvolvimento de feature
Implementei a feature `feature/totem-checkin` para representar o desenvolvimento do módulo de check-in do Totem. A branch incluiu um artefato inicial de especificação funcional no arquivo `totem-checkin.md`.

### 3.4 Integração da feature na `develop`
A feature foi integrada na branch `develop` usando merge sem fast-forward para preservar o histórico de fluxo.

### 3.5 Release `1.0.0`
A branch `release/1.0.0` foi criada a partir de `develop`, revisada e validada com foco na estabilidade do Totem de Check-in. O release incluiu a primeira versão formal do módulo, pronta para produção.

### 3.6 Hotfix emergencial
Um hotfix `hotfix/1.0.1` foi criado a partir de `main` para corrigir um problema urgente e depois integrado em `main` e `develop`.

## 4. Estrutura de versão
- `main`: contém os lançamentos oficiais.
- `develop`: contém a integração de recursos para a próxima versão.
- `release/1.0.0`: preparação e testes para a primeira entrega.
- `hotfix/1.0.1`: correção emergencial aplicada após o lançamento.

## 5. Histórico de commits e merges
Todos os commits relevantes e merges foram documentados, versionados e enviados para o repositório remoto.

## 6. Notas finais
Este documento deve ser mantido atualizado sempre que a estratégia GitFlow for aplicada no projeto do Totem de Check-in do PrettyFlights.
