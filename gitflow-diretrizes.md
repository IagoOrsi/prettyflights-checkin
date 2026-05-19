# GitFlow - PrettyFlights Totem de Check-in

# Objetivo

Este documento apresenta a aplicação da estratégia GitFlow no desenvolvimento da versão 1.0.0 do módulo de Totem de Check-in da empresa PrettyFlights.

O objetivo é organizar o fluxo de desenvolvimento utilizando branches permanentes e temporárias, aplicando boas práticas de versionamento com Semantic Versioning e Conventional Commits.

---

# Estratégia GitFlow

O GitFlow é uma estratégia de branching utilizada para organizar o desenvolvimento de software de maneira estruturada.

O fluxo é dividido em:

- Branches permanentes
- Branches temporárias

---

# Branches Permanentes

## main

A branch `main` representa o ambiente de produção.

Ela contém apenas versões estáveis e prontas para publicação.

Exemplo:

```bash
git checkout main
```

---

## develop

A branch `develop` é utilizada para integração contínua das funcionalidades em desenvolvimento.

Todas as features são integradas nela antes da publicação.

Exemplo:

```bash
git checkout -b develop
```

---

# Inicialização do Projeto

O projeto foi iniciado com a criação do repositório Git local.

Comando utilizado:

```bash
git init
```

Após isso, foi criado o primeiro commit do projeto.

```bash
git add .
git commit -m "chore: initial project structure"
```

O repositório remoto também foi configurado no GitHub.

```bash
git remote add origin https://github.com/user/prettyflights-checkin.git
```

---

# Desenvolvimento da Feature

Foi criada uma branch de feature para implementar a funcionalidade de emissão de cartão de embarque.

Nome da branch:

```text
feature/boarding-pass
```

Comando utilizado:

```bash
git checkout -b feature/boarding-pass
```

Durante o desenvolvimento, foram realizados commits utilizando Conventional Commits.

Exemplo:

```bash
git commit -m "feat: add boarding pass generation"
```

---

# Integração da Feature

Após o desenvolvimento da funcionalidade, a feature foi integrada à branch `develop`.

Comandos utilizados:

```bash
git checkout develop
git merge feature/boarding-pass
```

Depois do merge, as alterações foram enviadas ao repositório remoto.

```bash
git push origin develop
```

---

# Criação da Release 1.0.0

Após a conclusão das funcionalidades necessárias, foi criada a branch de release.

Nome da branch:

```text
release/1.0.0
```

Comando utilizado:

```bash
git checkout -b release/1.0.0
```

Nessa etapa foram realizados ajustes finais e preparação para produção.

Commit realizado:

```bash
git commit -m "release: prepare version 1.0.0"
```

---

# Publicação da Release

A release foi integrada à branch `main`.

Comandos utilizados:

```bash
git checkout main
git merge release/1.0.0
```

Foi criada a tag da versão oficial utilizando Semantic Versioning.

```bash
git tag -a v1.0.0 -m "Version 1.0.0"
```

Depois disso, a versão foi enviada ao GitHub.

```bash
git push origin main
git push origin v1.0.0
```

---

# Integração da Release na Develop

Após a publicação da versão, a branch `develop` também recebeu as alterações da release para manter o histórico sincronizado.

Comandos utilizados:

```bash
git checkout develop
git merge release/1.0.0
```

---

# Correção Emergencial com Hotfix

Após a publicação da versão 1.0.0, foi identificado um problema na validação de CPF dos passageiros.

Para corrigir rapidamente o erro, foi criada uma branch de hotfix a partir da `main`.

Nome da branch:

```text
hotfix/cpf-validation
```

Comando utilizado:

```bash
git checkout -b hotfix/cpf-validation
```

O problema foi corrigido e um commit de correção foi realizado.

```bash
git commit -m "fix: correct cpf validation"
```

---

# Publicação do Hotfix

O hotfix foi integrado à branch `main`.

Comandos utilizados:

```bash
git checkout main
git merge hotfix/cpf-validation
```

Foi criada uma nova tag representando a correção da versão.

```bash
git tag -a v1.0.1 -m "Hotfix version 1.0.1"
```

Envio para o GitHub:

```bash
git push origin main
git push origin v1.0.1
```

---

# Integração do Hotfix na Develop

Para manter o ambiente de desenvolvimento atualizado, o hotfix também foi integrado à branch `develop`.

Comandos utilizados:

```bash
git checkout develop
git merge hotfix/cpf-validation
```

---

# Conventional Commits

Durante o projeto foram utilizados Conventional Commits para padronizar o histórico.

Principais tipos utilizados:

| Tipo | Objetivo |
|---|---|
| feat | Nova funcionalidade |
| fix | Correção de bugs |
| chore | Configurações e manutenção |
| docs | Documentação |
| release | Preparação de versão |

Exemplos:

```bash
git commit -m "feat: add boarding pass generation"
```

```bash
git commit -m "fix: correct cpf validation"
```

---

# Semantic Versioning

O projeto utilizou Semantic Versioning no formato:

```text
MAJOR.MINOR.PATCH
```

Exemplos aplicados:

| Versão | Descrição |
|---|---|
| 1.0.0 | Primeira versão oficial |
| 1.0.1 | Correção emergencial |

---

# Estrutura Final das Branches

```text
main
 ├── release/1.0.0
 ├── hotfix/cpf-validation
 └── develop
      └── feature/boarding-pass
```

---

# Conclusão

A utilização do GitFlow permitiu organizar o desenvolvimento do módulo de Totem de Check-in da PrettyFlights de maneira estruturada e segura.

O uso de branches específicas para features, releases e hotfixes facilitou o controle das alterações, enquanto o Semantic Versioning e os Conventional Commits padronizaram o versionamento e o histórico do projeto.