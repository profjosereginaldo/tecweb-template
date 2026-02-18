---
name: "Prática 01"
about: "Template para criar a issue da pratica01"
title: "[Prática 01] – Estrutura Semântica do HTML5"
labels: ["pratica01"]
assignees: ''
---

## 🎯 Objetivo
Nesta prática, você irá:
- Aplicar tags semânticas do HTML5 para estruturar a dashboard do portal Aluno Online.

## 📝 Instruções da Atividade
1️⃣ **Preparação do ambiente**
1. Abra o **Visual Studio Code** na pasta do seu repositório.
2. Abra um terminal e certifique-se de que está na branch `develop`.
```bash
git checkout develop
```
3. Crie e alterne para a branch desta prática.
```bash
git checkout -b feature/pratica01
```

2️⃣ **Implementação do código**
1. No painel esquerdo do VSCode, localize a pasta `aluno-online-vanilla`.
2. Desenvolva no arquivo `index.html` a estrutura da página Dashboard:
- **Sidebar**: Criar um `<aside>` que conterá um `<header>` para o logo e um `<nav>` para o menu de navegação;
- **Área de Conteúdo**: Criar uma `<main>` para agrupar a barra superior e o conteúdo principal;
- **Topbar**: Criar um `<header>` para a saudação e o avatar do usuário;
- **Conteúdo Principal**: Usar a tag `<section>` onde ficarão os blocos de conteúdo;
- **Blocos de Conteúdo**: Usar a tag `<article>` para separar as áreas de conteúdo (ex.: Mural de Avisos, Calendário Acadêmico e Minhas Disciplinas).

🖼️ **Referência visual** (use como guia)
![Wireframe](https://raw.githubusercontent.com/profjosereginaldo/tecweb-template/refs/heads/main/assets/wireframe.png)

3️⃣ **Execução e teste**
1. No terminal, acesse a pasta do projeto.
```bash
cd praticas/aluno-online-vanilla
```
2. Suba o container e instale as dependências:
```bash
docker compose up -d
docker compose exec app npm install
```
3. Inicie o servidor de desenvolvimento:
```bash
docker compose exec app npm run dev
```
4. Acesse no navegador: `http://localhost:5173`

4️⃣ **Checklist antes de enviar**
- [ ] Branch criada a partir da develop
- [ ] Estrutura semântica implementada
- [ ] Projeto executa sem erros
- [ ] Commit realizado
- [ ] Pull Request criado para develop

## 📤 Entrega da Prática
1. Abra outro terminal do VSCode (isso garante que você esteja na pasta raiz).
2. Adicione os arquivos ao controle de versão e grave suas alterações. Substitua `#ID` pelo número da Issue (ex.: 10).
```bash
git add .
git commit -m "feat: conclui pratica01. Fecha #ID"
```
3. Envie suas alterações para o GitHub.
```bash
git push origin feature/pratica01
```
4. No GitHub, clique no botão **Compare & pull request**.
5. **Importante**: Certifique-se de que o **base repository** é o repositório do professor e a **base branch** é a `develop`.
6. Na descrição, escreva: `Nesta prática, implementei a estrutura do portal utilizando as tags semânticas do HTML5. Fecha #ID`. Substitua `#ID` pelo número da Issue.
7. Clique em **Create pull request** e aguarde a correção do professor.

⚠️ **Erros comuns**
- Criar a branch de trabalho a partir de uma branch diferente da indicada na atividade;
- Esquecer de iniciar o Docker;
- Enviar PR para a branch errada.