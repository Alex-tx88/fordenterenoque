# Projeto: EncomendasSmart

**Disciplina:** DevOps Tools e Gerência de Configurações e Dependências
**Instituição:** UNINASSAU
**Equipe:**
1. Alex Teixeira de Jesus
2. Thales Macêdo de Jesus Araújo
3. Enoque Pereira Santos Neto
4. José Heitor Batista dos Santos

---

## 1. Descrição do projeto
O **EncomendasSmart** é uma aplicação web desenvolvida para otimizar o gerenciamento e controle de correspondências e pacotes em condomínios. O sistema permite o registro detalhado de novas encomendas, o acompanhamento de seus status de entrega (pendente, notificado ou retirado) e a visualização de métricas operacionais e históricos através de um painel interativo (dashboard).

## 2. Objetivo da solução
O objetivo central do **EncomendasSmart** é digitalizar e modernizar o fluxo de recebimento e distribuição de pacotes em condomínios. A solução foi criada para resolver problemas comuns de portarias, como a perda de informações, o acúmulo desorganizado de caixas e a falta de rastreabilidade, substituindo os antigos cadernos de anotações por um controle digital rápido, seguro e eficiente.

## 3. Tecnologias utilizadas
As seguintes ferramentas e tecnologias foram aplicadas na construção deste projeto:
* **Frontend:** Angular CLI (versão 19.2.15), HTML, CSS, TypeScript, JavaScript
* **Controle de Versão:** Git e GitHub
* **Continuous Integration (CI):** GitHub Actions
* **Prototipação:** Figma
* **Gerenciamento do Projeto:** Trello

## 4. Estrutura do repositorio
O projeto segue a arquitetura padrão do Angular, organizada da seguinte forma:
* `/.github/workflows/`: Contém os arquivos de configuração do pipeline de CI (ex: `ci.yml`).
* `/src/app/auth/`: Componentes de autenticação (Login e Registro).
* `/src/app/components/main/`: Telas principais do sistema, como Dashboard e Histórico.
* `/src/app/core/`: Serviços e modelos de dados (ex: `entrega.service.ts`).
* `/src/app/shared/`: Componentes reutilizáveis, como cards de entrega e modais.
* `README.md`: Documentação principal do projeto.

## 5. Continuous Integration (CI) - Workflow e Pipeline
Para garantir a integridade do código, implementamos uma esteira de Continuous Integration utilizando o GitHub Actions.

### Explicação do Workflow (`ci.yml`)
O arquivo `ci.yml` define as regras de execução. O gatilho (trigger) configurado faz com que o pipeline seja executado **automaticamente sempre que ocorrer um evento de `push`** na branch principal (`main`) do repositório.

### Fluxo de execução do pipeline
Quando o pipeline é acionado, ele provisiona uma máquina virtual (runner) e executa sequencialmente os seguintes passos (jobs):
1. **Exibir mensagem no console:** Confirma o início do processo de validação.
2. **Executar script do projeto:** Realiza a instalação das dependências (ex: `npm install`) e tenta "buildar" o projeto para garantir que não há erros de compilação.
3. **Listar arquivos do projeto / Validar execução:** Verifica a estrutura do repositório e atesta que os arquivos de build foram gerados corretamente.

Dessa forma, a **explicação do pipeline** se resume a garantir de forma automatizada que nenhum código que quebre a aplicação seja integrado acidentalmente ao repositório principal, aplicando princípios modernos de DevOps.

---
## 6. Como rodar o projeto localmente (Ambiente de Desenvolvimento)

Siga os passos abaixo para configurar e executar o projeto em sua máquina:

1. **Instale as dependências:**
   Antes de rodar o projeto pela primeira vez, certifique-se de instalar todas as dependências do Node.js necessárias executando o comando abaixo na raiz do projeto:
   ```bash
   npm install
2. **Execute o servidor de desenvolvimento:**
   Para iniciar a aplicação localmente, utilize o comando:
   ```bash
   ng serve
