# Comandos Git

## Inicialização

---

## git init

Inicializa um novo repositório Git no diretório atual.

### Exemplo 1

```bash
git init
```

### Exemplo 2

```bash
git init projeto-checkin
```

---

## git clone

Cria uma cópia local de um repositório remoto.

### Exemplo 1

```bash
git clone https://github.com/user/projeto.git
```

### Exemplo 2

```bash
git clone https://github.com/user/api.git api-local
```

---

# Configuração

---

## git config

Define configurações do Git, como nome e email do usuário.

### Exemplo 1

```bash
git config --global user.name "Iago Orsi"
```

### Exemplo 2

```bash
git config --global user.email "iago@email.com"
```

---

## git remote add

Conecta o repositório local a um repositório remoto.

### Exemplo 1

```bash
git remote add origin https://github.com/user/projeto.git
```

### Exemplo 2

```bash
git remote add upstream https://github.com/original/projeto.git
```

---

# Versionamento

---

## git add

Adiciona arquivos para a área de stage.

### Exemplo 1

```bash
git add README.md
```

### Exemplo 2

```bash
git add .
```

---

## git commit

Salva alterações no histórico do projeto.

### Exemplo 1

```bash
git commit -m "feat: add login screen"
```

### Exemplo 2

```bash
git commit -m "fix: correct cpf validation"
```

---

## git status

Mostra o estado atual dos arquivos do projeto.

### Exemplo 1

```bash
git status
```

### Exemplo 2

```bash
git status -s
```

---

## git log

Exibe o histórico de commits.

### Exemplo 1

```bash
git log
```

### Exemplo 2

```bash
git log --oneline
```

---

# Branches

---

## git branch

Cria ou lista branches.

### Exemplo 1

```bash
git branch
```

### Exemplo 2

```bash
git branch develop
```

---

## git checkout

Troca de branch ou recupera arquivos.

### Exemplo 1

```bash
git checkout main
```

### Exemplo 2

```bash
git checkout -b feature/login
```

---

## git switch

Alternativa moderna ao checkout para troca de branches.

### Exemplo 1

```bash
git switch develop
```

### Exemplo 2

```bash
git switch -c feature/payment
```

---

## git merge

Une alterações de uma branch em outra.

### Exemplo 1

```bash
git merge develop
```

### Exemplo 2

```bash
git merge feature/boarding-pass
```

---

# Atualização

---

## git pull

Baixa e integra alterações do repositório remoto.

### Exemplo 1

```bash
git pull
```

### Exemplo 2

```bash
git pull origin main
```

---

## git push

Envia commits locais para o repositório remoto.

### Exemplo 1

```bash
git push
```

### Exemplo 2

```bash
git push origin develop
```

---

## git fetch

Busca alterações remotas sem fazer merge automático.

### Exemplo 1

```bash
git fetch
```

### Exemplo 2

```bash
git fetch origin
```

---

# Correções

---

## git stash

Armazena temporariamente alterações não commitadas.

### Exemplo 1

```bash
git stash
```

### Exemplo 2

```bash
git stash pop
```

---

## git restore

Restaura arquivos para o estado anterior.

### Exemplo 1

```bash
git restore README.md
```

### Exemplo 2

```bash
git restore .
```

---

## git revert

Desfaz um commit criando um novo commit de reversão.

### Exemplo 1

```bash
git revert HEAD
```

### Exemplo 2

```bash
git revert a1b2c3d
```

---

## git reset

Move o ponteiro do Git para um commit anterior.

### Exemplo 1

```bash
git reset --soft HEAD~1
```

### Exemplo 2

```bash
git reset --hard HEAD~2
```

---

# Tags

---

## git tag

Cria marcações de versões no projeto.

### Exemplo 1

```bash
git tag v1.0.0
```

### Exemplo 2

```bash
git tag -a v1.0.1 -m "Hotfix version"
```

---

# Conclusão

Os comandos apresentados são fundamentais para o controle de versão utilizando Git. Eles permitem inicializar projetos, criar branches, versionar arquivos, integrar alterações e manter o histórico organizado de forma profissional.