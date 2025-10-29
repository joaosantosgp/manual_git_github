## 🧩 Introdução

O **Git** é um sistema de **controle de versão distribuído**, criado por **Linus Torvalds** em 2005.
Ele permite gerenciar o histórico de alterações de projetos, colaborar com outros desenvolvedores e versionar código de forma eficiente.

---

## ⚙️ Instalação e Configuração

### 🔧 Instalação

**Windows:**

```bash
https://git-scm.com/download/win
```

**Linux (Debian/Ubuntu):**

```bash
sudo apt update
sudo apt install git
```

**macOS (via Homebrew):**

```bash
brew install git
```

### ⚙️ Configuração Inicial

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
git config --global core.editor "code --wait"
git config --global init.defaultBranch main
```

Verificar as configurações:

```bash
git config --list
```

---

## 📘 Conceitos Fundamentais

| Conceito               | Descrição                                             |
| ---------------------- | ----------------------------------------------------- |
| **Repositório (repo)** | Diretório onde o Git armazena o histórico do projeto  |
| **Commit**             | Registro de alterações no histórico                   |
| **Branch**             | Linha de desenvolvimento independente                 |
| **Merge**              | Combina alterações de diferentes branches             |
| **Remote**             | Repositório hospedado na nuvem (GitHub, GitLab, etc.) |
| **HEAD**               | Ponteiro que indica o commit atual                    |

---

## 🧱 Fluxo Básico de Trabalho

1. **Inicializar o repositório:**

   ```bash
   git init
   ```
2. **Verificar o status dos arquivos:**

   ```bash
   git status
   ```
3. **Adicionar arquivos ao stage:**

   ```bash
   git add arquivo.txt
   # ou todos os arquivos
   git add .
   ```
4. **Fazer um commit:**

   ```bash
   git commit -m "Mensagem do commit"
   ```
5. **Ver histórico:**

   ```bash
   git log
   ```

---

## 🌿 Branches (Ramificações)

### Criar uma nova branch

```bash
git branch minha-feature
```

### Mudar de branch

```bash
git checkout minha-feature
# ou na versão mais nova
git switch minha-feature
```

### Criar e mudar de branch em um comando

```bash
git checkout -b nova-feature
```

### Mesclar branches

```bash
git merge minha-feature
```

### Excluir uma branch

```bash
git branch -d minha-feature
```

---

## 🌐 Repositórios Remotos

### Clonar um repositório

```bash
git clone https://github.com/usuario/repositorio.git
```

### Adicionar um repositório remoto

```bash
git remote add origin https://github.com/usuario/repositorio.git
```

### Enviar alterações

```bash
git push origin main
```

### Atualizar com alterações remotas

```bash
git pull origin main
```

---

## 🏷️ Tags e Versionamento

### Criar uma tag

```bash
git tag -a v1.0.0 -m "Versão 1.0.0"
```

### Listar tags

```bash
git tag
```

### Enviar tags

```bash
git push origin --tags
```

---

## 🕓 Trabalhando com Histórico

### Visualizar histórico resumido

```bash
git log --oneline --graph --decorate --all
```

### Desfazer alterações locais

```bash
git checkout -- arquivo.txt
```

### Reverter um commit

```bash
git revert <id_do_commit>
```

### Voltar para um commit anterior

```bash
git reset --hard <id_do_commit>
```

---

## ♻️ Rebasing e Cherry-Pick

### Rebase

```bash
git rebase main
```

> Reaplica commits sobre outro branch.

### Cherry-pick

```bash
git cherry-pick <id_do_commit>
```

> Copia um commit específico para outro branch.

---

## 🧰 Stash e Limpeza

### Salvar alterações não commitadas

```bash
git stash
```

### Recuperar alterações salvas

```bash
git stash pop
```

### Limpar arquivos não rastreados

```bash
git clean -fd
```

---

## 🪝 Hooks e Automatização

Hooks são scripts executados automaticamente em eventos do Git (como `commit`, `push` ou `merge`).

Exemplo: criar um hook de pré-commit em `.git/hooks/pre-commit`

```bash
#!/bin/bash
npm test
```

Torne-o executável:

```bash
chmod +x .git/hooks/pre-commit
```

---

## 🧠 Boas Práticas

* Use mensagens de commit claras e padronizadas.
  Exemplo:

  ```
  feat: adiciona autenticação JWT
  fix: corrige bug de login
  docs: atualiza README
  ```
* Crie branches por funcionalidade (`feature/login`, `fix/bug-123`).
* Evite commits grandes.
* Faça `pull` antes de `push`.
* Use `.gitignore` para arquivos desnecessários.

---

## 🚀 Recursos Avançados

### Submódulos

```bash
git submodule add https://github.com/outro/repositorio.git pasta/
```

### Bisect (localizar commits problemáticos)

```bash
git bisect start
git bisect bad
git bisect good <commit_id>
```

### Alias úteis

```bash
git config --global alias.lg "log --oneline --graph --decorate --all"
git config --global alias.st "status -sb"
```

---

## 🔗 Referências

* [Documentação Oficial do Git](https://git-scm.com/doc)
* [Pro Git Book (grátis)](https://git-scm.com/book/pt-br/v2)
* [Guia de Comandos Git - Atlassian](https://www.atlassian.com/git/tutorials)

---

Quer que eu **adicione exemplos práticos com um projeto fictício (ex: “meu-site”)**, mostrando cada comando em uso na prática? Isso tornaria o manual mais didático.
