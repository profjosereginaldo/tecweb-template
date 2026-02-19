---
name: "Prática 01"
about: "Template para criar a issue da pratica01"
title: "[Prática 01] – Estrutura Semântica do HTML5"
labels: ["pratica01"]
assignees: ''
---

## 📌 Contexto
Uma instituição está modernizando o portal **Aluno Online**. A versão atual da página foi construída utilizando apenas `<div>`, o que dificulta manutenção, organização do código e acessibilidade.

Você faz parte da equipe responsável por reestruturar a página principal (Dashboard) utilizando corretamente os elementos semânticos do HTML5.

Seu desafio é transformar o layout apresentado em uma estrutura HTML organizada, semântica e bem definida.

## 🎯 Objetivo
Nesta prática, você irá:
- Aplicar corretamente as principais tags semânticas do HTML5 para estruturar a dashboard do portal Aluno Online.

## 🖼️ Referência visual
Utilize a imagem abaixo como guia estrutural para a construção da página:

![Wireframe](https://raw.githubusercontent.com/profjosereginaldo/tecweb-template/refs/heads/main/assets/wireframe.png)

A imagem serve como referência de organização dos blocos da página.  
O foco da prática é a **estrutura semântica**, não a estilização visual.

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
2. Desenvolva a estrutura no arquivo `index.html`.
3. Organize a página considerando os seguintes blocos:
- **Menu lateral**: Estruture uma área para navegação contendo o nome do sistema e os links do menu;
- **Área principal da página**: Estruture o conteúdo principal da dashboard;
- **Barra superior (Topbar)**: Área com saudação e avatar do usuário;
- **Blocos de conteúdo**: Mural de Avisos, Calendário Acadêmico e Minhas Disciplinas.

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
4. Acesse no navegador: `http://localhost:5173`.
5. Verifique se a página carrega corretamente e se a estrutura está organizada.

4️⃣ **Checklist antes de enviar**
- [ ] Branch criada a partir da develop
- [ ] Estrutura semântica implementada com as tags mais adequadas
- [ ] Projeto executa sem erros

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
6. Na descrição, escreva: `Nesta prática, implementei a estrutura semântica do portal utilizando HTML5. Fecha #ID`. Substitua `#ID` pelo número da Issue.
7. Clique em **Create pull request** e aguarde a correção do professor.

⚠️ **Erros comuns**
- Criar a branch de trabalho a partir de uma branch diferente da indicada na atividade;
- Usar `<div>` em excesso;
- Esquecer de iniciar o Docker;
- Enviar PR para a branch errada.