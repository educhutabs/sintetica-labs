# S/NTÉTICA LABS

O **S/NTÉTICA LABS** é um laboratório técnico criado para transformar conhecimento em competência operacional demonstrável, focado em Cloud, DevOps, Platform Engineering e AI-assisted Operations.

---

## Objetivos

Ao final do projeto, o objetivo é conseguir:

- operar um ambiente Linux;
- trabalhar profissionalmente com Git e GitHub;
- compreender redes e HTTP;
- desenvolver pequenas ferramentas e serviços em Go;
- automatizar tarefas com Bash;
- containerizar aplicações com Docker;
- implementar pipelines CI/CD;
- provisionar infraestrutura com Terraform;
- operar workloads em AWS;
- executar aplicações em Kubernetes;
- empacotar deployments com Helm;
- utilizar GitOps;
- implementar observabilidade;
- aplicar fundamentos de DevSecOps;
- utilizar IA como ferramenta de engenharia e operações;
- investigar incidentes;
- documentar decisões, falhas e soluções.

---

## Modelo de profundidade

Cada competência será classificada em quatro níveis.

| Nível | Significado |
|---|---|
| **L1 — Reconhecer** | Entender o conceito, finalidade e contexto |
| **L2 — Utilizar** | Executar tarefas comuns com documentação |
| **L3 — Operar** | Trabalhar autonomamente e diagnosticar problemas comuns |
| **L4 — Dominar** | Conhecimento profundo, trade-offs e problemas complexos |

---

## Arquitetura do laboratório

O laboratório utiliza uma separação deliberada entre **workstation** e **ambiente de execução**.

```text
                     WORKSTATION
                 ┌─────────────────┐
                 │  MacBook / macOS│
                 │                 │
                 │ Git             │
                 │ GitHub          │
                 │ VS Code         │
                 │ Terminal        │
                 └────────┬────────┘
                          │
                       SSH / Git
                          │
                          ▼
                 ┌─────────────────┐
                 │ Fedora Server   │
                 │   Bare Metal    │
                 │                 │
                 │ S/NTÉTICA LABS  │
                 └────────┬────────┘
                          │
                    02 em diante
                          │
                    KVM / QEMU
                          │
                 ┌────────┴────────┐
                 │                 │
                VM01              VM02
```

### Workstation

O MacBook é utilizado para:

- desenvolvimento;
- edição;
- Git;
- GitHub;
- documentação;
- SSH;
- acesso aos serviços do laboratório.

### Lab Server

O Fedora Server em bare metal é o ambiente principal para:

- Linux;
- serviços;
- networking;
- virtualização;
- containers;
- infraestrutura experimental.

### Virtualização

KVM/QEMU será introduzido somente depois dos fundamentos de Linux e networking.

---

## Projeto principal

O S/NTÉTICA LABS será construído como **um único projeto evolutivo**.

Não serão criados diversos projetos pequenos e desconectados.

A aplicação inicial será simples e servirá como veículo para estudar engenharia de infraestrutura e operações.

O sistema deverá evoluir para incorporar:

- API;
- health checks;
- serviços;
- incidentes;
- eventos;
- persistência;
- workers;
- containers;
- CI/CD;
- cloud;
- Kubernetes;
- observabilidade;
- segurança;
- AI-assisted operations.

O objetivo é aprender a construir, executar, automatizar, observar e diagnosticar sistemas.

---

## Roadmap

| Mês | Tema | Resultado |
|---|---|---|
| **01** | Linux + Git | Linux Operations Lab |
| **02** | Networking + HTTP + Virtualização | Rede e primeira VM |
| **03** | Go + Bash + Automação | API + CLI + scripts |
| **04** | Docker | Aplicação containerizada |
| **05** | CI/CD | Pipeline automatizado |
| **06** | AWS + Terraform | Infraestrutura cloud como código |
| **07** | Kubernetes | Aplicação orquestrada |
| **08** | Helm + GitOps | Deployment declarativo |
| **09** | Observability + Reliability | Métricas, logs, traces e incidentes |
| **10** | Security + DevSecOps | Segurança integrada ao ciclo |
| **11** | AI-assisted Operations | IA aplicada a operações |
| **12** | Production Capstone | Plataforma consolidada |

---

## Estrutura do repositório

A estrutura evoluirá ao longo do programa.

```text
sintetica-labs/
│
├── README.md
│
├── docs/
│   ├── architecture/
│   ├── decisions/
│   ├── incidents/
│   ├── operations/
│   ├── runbooks/
│   ├── security/
│   └── troubleshooting/
│
├── 01-linux-git/
│
├── 02-networking-http/
│
├── 03-go-bash/
│
├── 04-docker/
│
├── 05-cicd/
│
├── 06-aws-terraform/
│
├── 07-kubernetes/
│
├── 08-helm-gitops/
│
├── 09-observability/
│
├── 10-security/
│
├── 11-ai-ops/
│
├── 12-capstone/
│
├── app/
├── scripts/
├── docker/
├── terraform/
├── kubernetes/
├── helm/
├── observability/
├── ai/
│
└── .github/
    └── workflows/
```

---

## Organização por mês

Cada diretório mensal deve responder a cinco perguntas:

1. O que foi estudado?
2. O que foi praticado?
3. O que foi implementado?
4. O que foi quebrado e diagnosticado?
5. O que foi aprendido?

Estrutura recomendada:

```text
XX-tema/
├── README.md
├── labs/
├── scripts/
├── troubleshooting/
└── notes/
```

Quando houver código compartilhado entre meses, ele poderá migrar para os diretórios estruturais do projeto, como `app/`, `scripts/`, `terraform/`, `kubernetes/` etc.

---

## Método de aprendizagem

Cada assunto seguirá o ciclo:

```text
TEORIA
   ↓
LABORATÓRIO
   ↓
SINTÉTICA LABS
   ↓
BREAK / FIX
   ↓
DOCUMENTAÇÃO
   ↓
EXPLICAÇÃO
```

### Teoria

Utilizar uma fonte principal e documentação oficial.

### Laboratório

Reproduzir o conceito em ambiente controlado.

### S/NTÉTICA LABS

Aplicar o conhecimento ao projeto.

### Break / Fix

Provocar uma falha e investigá-la.

### Documentação

Registrar o procedimento e o aprendizado.

### Explicação

Ser capaz de explicar o funcionamento sem depender do tutorial.

---

## 9. Troubleshooting

Troubleshooting é uma competência central do projeto.

Todos os incidentes devem seguir aproximadamente:

```text
Symptom
   ↓
Impact
   ↓
Hypotheses
   ↓
Evidence
   ↓
Investigation
   ↓
Root Cause
   ↓
Resolution
   ↓
Prevention
```

Não registrar apenas:

> "Comando X resolveu."

Registrar:

> "Qual era o sintoma, quais hipóteses foram consideradas, quais evidências eliminaram as hipóteses e qual foi a causa raiz."

---

## Incidentes

Incidentes serão deliberadamente introduzidos no laboratório.

Exemplos:

- serviço parado;
- permissão incorreta;
- processo encerrado;
- DNS quebrado;
- porta inacessível;
- timeout;
- container que não inicia;
- configuração incorreta;
- Pod em `CrashLoopBackOff`;
- deployment com regressão;
- aumento de latência;
- falha de banco;
- infraestrutura Terraform incorreta.

Cada incidente deve gerar documentação em:

```text
docs/incidents/
```

ou no diretório de troubleshooting correspondente ao mês.

---

## Runbooks

Problemas recorrentes devem gerar runbooks.

Exemplo:

```text
docs/runbooks/service-down.md
```

Estrutura:

```markdown
# Service Down

## Symptoms

## Impact

## Initial Checks

## Investigation

## Common Causes

## Resolution

## Validation

## Prevention
```

O objetivo é começar a desenvolver uma mentalidade de operação repetível.

---

## Architecture Decision Records

Decisões técnicas importantes devem ser registradas em:

```text
docs/decisions/
```

Exemplos:

```text
ADR-001 — Escolha do Go
ADR-002 — Escolha do PostgreSQL
ADR-003 — Containerização com Docker
ADR-004 — AWS como cloud principal
ADR-005 — Terraform como IaC
ADR-006 — Kubernetes
ADR-007 — Helm
ADR-008 — GitOps
ADR-009 — Observability
ADR-010 — DevSecOps
ADR-011 — AI-assisted Operations
```

Formato:

```markdown
# ADR-XXX — Título

## Context

## Decision

## Alternatives

## Consequences
```

---

## Documentação de arquitetura

A arquitetura deverá evoluir ao longo do projeto.

Inicialmente:

```text
Mac
 │
 SSH
 │
 ▼
Fedora Server
 │
 └── S/NTÉTICA service
```

Posteriormente:

```text
Mac
 │
 SSH
 │
 ▼
Fedora Server
 │
 └── KVM/QEMU
      ├── VM01
      └── VM02
```

Depois:

```text
On-Prem
   │
   ├── VMs
   │
   └── Kubernetes

Cloud
   │
   └── AWS
```

E finalmente:

```text
                    INTERNET
                        │
                      HTTPS
                        │
                 Load Balancer
                        │
                    Kubernetes
                        │
              ┌─────────┴─────────┐
              │                   │
           API Pods            Workers
              │                   │
              └─────────┬─────────┘
                        │
                    PostgreSQL
                        │
              ┌─────────┴─────────┐
              │                   │
         Observability          AI Ops
```

Os diagramas devem representar o estado real do projeto.

---

## Git workflow

O projeto será versionado desde o primeiro dia.

Workflow básico:

```text
main
 │
 ├── feature/...
 ├── fix/...
 └── docs/...
```

Pull Requests devem ser utilizados para mudanças relevantes.

Commits devem ser pequenos e explicativos.

Conventional Commits será utilizado quando fizer sentido:

```text
feat:
fix:
docs:
test:
refactor:
chore:
```

---

## Segurança do repositório

Nunca versionar:

```text
.env
credentials
private keys
API keys
passwords
tokens
cloud credentials
```

Antes de qualquer commit, verificar se informações sensíveis estão sendo adicionadas.

A segurança do repositório evoluirá posteriormente para:

- dependency scanning;
- secret scanning;
- IaC scanning;
- container scanning;
- supply-chain security.

---

## Recursos de estudo

Cada mês deverá possuir uma fonte principal.

A regra é:

> **Uma boa fonte principal é melhor do que dez cursos medianos.**

Fontes prioritárias:

### Linux

- Linux Foundation — LFS101
- The Linux Command Line

### Git

- Pro Git
- GitHub Docs

### Networking / HTTP

- Computer Networking: A Top-Down Approach
- MDN HTTP
- documentação oficial das ferramentas

### Go

- A Tour of Go
- Effective Go
- Let's Go

### Docker

- Docker Documentation
- Docker Deep Dive

### CI/CD

- GitHub Actions Documentation
- The DevOps Handbook

### Terraform

- HashiCorp Developer
- Terraform: Up & Running

### AWS

- AWS Skill Builder
- documentação oficial AWS

### Kubernetes

- Kubernetes Documentation
- Kubernetes: Up & Running

### Helm / GitOps

- Helm Documentation
- Argo CD Documentation

### Observability

- OpenTelemetry Documentation
- Prometheus Documentation
- Grafana Documentation
- Observability Engineering

### Reliability

- Google SRE Books

### Security

- OWASP DevSecOps Guideline
- OWASP Top 10

### AI

- Google Machine Learning Crash Course
- AWS Generative AI learning material

---

## Certificações

Certificações são complementares ao projeto.

Prioridade:

1. **Terraform Associate**
2. **AWS Cloud Practitioner**

A ordem de prioridade é:

```text
Conhecimento
   ↓
Laboratório
   ↓
Projeto
   ↓
Troubleshooting
   ↓
Certificação
```

Nunca:

```text
Certificação
   ↓
Conhecimento superficial
```

---

## Carreira

### Meses 1–3

Preparação:

- GitHub;
- LinkedIn;
- currículo;
- networking;
- análise de vagas.

### Meses 4–5

Começar a acompanhar processos seletivos e comparar requisitos.

### Mês 6

Iniciar candidaturas regulares.

Alvos:

- DevOps Intern;
- DevOps Junior;
- Cloud Junior;
- Infrastructure Junior;
- Cloud Support;
- SRE Intern;
- Platform Engineering Intern.

Meta inicial:

**5–10 candidaturas qualificadas por semana.**

A candidatura passa a fazer parte do processo de aprendizagem.

---

## Definition of Done do projeto

O SINTÉTICA LABS será considerado concluído quando for possível demonstrar:

### Linux

Um servidor Linux administrado e documentado.

### Networking

Comunicação entre workstation, servidor e VMs compreendida e diagnosticável.

### Software

Uma API e ferramentas auxiliares em Go.

### Automation

Scripts e operações automatizadas.

### Containers

Aplicação executada com Docker.

### CI/CD

Pipeline automatizado.

### Cloud

Infraestrutura AWS reproduzível.

### IaC

Terraform capaz de reconstruir a infraestrutura.

### Kubernetes

Aplicação executando e sendo diagnosticada em cluster.

### GitOps

Deployment controlado através de Git.

### Observability

Métricas, logs, traces e dashboards.

### Security

Controles básicos integrados ao ciclo.

### AI Operations

IA auxiliando análise operacional com human-in-the-loop.

### Incident Response

Incidentes reais de laboratório documentados.

---

## Critério de maturidade

O projeto não será avaliado pelo número de tecnologias utilizadas.

Será avaliado pela capacidade de responder:

> **O que é?**

> **Por que usamos?**

> **Como funciona?**

> **Como eu sei que está funcionando?**

> **Como ele falha?**

> **Como eu descubro a causa?**

> **Como eu corrijo?**

> **Como eu evito que aconteça novamente?**

Se essas perguntas puderem ser respondidas para uma competência dentro do nível esperado, ela está suficientemente aprendida para o estágio atual.

---

## Princípio do projeto

O S/NTÉTICA LABS não é um tutorial.

Não é uma coleção de certificados.

Não é uma coleção de projetos descartáveis.

É um **registro de evolução profissional**.

Cada mês deverá deixar uma evidência permanente de aprendizado:

```text
Conhecimento
    ↓
Implementação
    ↓
Falha
    ↓
Diagnóstico
    ↓
Correção
    ↓
Documentação
```

Ao final dos 12 meses, o repositório deverá contar uma história:

> **Comecei administrando um Fedora Server bare metal. Evoluí para construir, automatizar, provisionar, orquestrar, observar, proteger e operar uma aplicação em infraestrutura moderna.**

---

## Roadmap resumido

```text
01 ─ Linux + Git
 │
 ├── Fedora bare metal
 ├── SSH
 ├── systemd
 ├── logs
 ├── permissions
 └── Git workflow
       │
02 ─ Networking + HTTP + Virtualização
 │
 ├── TCP/IP
 ├── DNS
 ├── HTTP
 ├── KVM/QEMU
 └── primeira VM
       │
03 ─ Go + Bash
 │
 ├── API
 ├── CLI
 └── automação
       │
04 ─ Docker
 │
 ├── images
 ├── containers
 └── Compose
       │
05 ─ CI/CD
 │
 └── GitHub Actions
       │
06 ─ AWS + Terraform
 │
 ├── Cloud
 ├── IAM
 ├── VPC
 └── IaC
       │
07 ─ Kubernetes
 │
 ├── Pods
 ├── Deployments
 ├── Services
 └── troubleshooting
       │
08 ─ Helm + GitOps
 │
 └── Argo CD
       │
09 ─ Observability
 │
 ├── Prometheus
 ├── Grafana
 └── OpenTelemetry
       │
10 ─ Security
 │
 └── DevSecOps
       │
11 ─ AI Operations
 │
 └── AI-assisted engineering
       │
12 ─ Capstone
 │
 └── Production-ready demonstration
```
