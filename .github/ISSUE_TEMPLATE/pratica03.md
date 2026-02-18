---
name: "Prática 03"
about: "Template para criar a issue da pratica03"
title: "[Prática 03] – Interatividade com JavaScript"
labels: ["pratica03"]
assignees: ''
---

## 🎯 Objetivo
Nesta prática, você irá:
- Construir um formulário de login e validar o preenchimento dos campos antes de "entrar" no portal.

## 📝 Instruções da Atividade
**1️⃣ Preparação do ambiente**
1. Abra o **Visual Studio Code** na pasta do seu repositório.
2. Abra um terminal e certifique-se de que está na branch `develop`.
```bash
git checkout develop
```
3. Crie e alterne para a branch desta prática.
```bash
git checkout -b feature/pratica03
```

**2️⃣ Implementação do código**
1. No painel esquerdo do VSCode, localize a pasta `aluno-online-vanilla`.
2. Desenvolva no arquivo `login.html` um formulário da página Login:
- **Área de Conteúdo**: Usar a tag `<main>` onde ficará o formulário e o rodapé;
- **Formulário**: Criar um `<form>` com os campos `email` e `senha`, e o botão `Entrar`. Cada campo deve possuir um `<label>`, um `<input>` e um `<p>` para exibir mensagens de erro;
- **Rodapé**: Criar um `<footer>` para exibir um texto.
3. Desenvolva no arquivo `style.css` os estilos da página de Login;
- **Body**: Criar uma classe para o `<body>` com `flex-direction: column`;
- **Área de Conteúdo**: Criar uma classe para o `<main>` com `border: 1px solid var(--cor-fundo)`, `border-radius: 0.5rem`, `display: flex`, `flex: 1`, `flex-direction: column`, `justify-content: center`, `margin: 2.0rem auto`, `max-width: 400px`, `padding: 1rem` e `width: 100%`;
- **Campos**: Definir `border: 1px solid var(--cor-fundo)`, `border-radius: 0.25rem`, `font-size: 1rem`, `padding: 0.5rem`, `margin-bottom: 0.5rem` e `width: 100%`;
- **Botão**: Definir `background-color: var(--cor-fundo)`, `border: none`, `border-radius: 0.25rem`, `cursor: pointer`, `font-size: 1.1rem`, `padding: 0.5rem 1rem`, `margin-top: 1rem` e `width: 100%`;
- **Mensagens de erro**: Definir `color: #a70000` e `margin-bottom: 1rem`;
- **Rodapé**: Definir `font-size: 0.9rem`, `margin-bottom: 0.5rem`, `margin-top: 0.5rem`, e `text-align: center`.
4. Desenvolva no arquivo `main.js` a validação de formulário:
- Selecionar os elementos do formulário usando `document.getElementById`;
- Escutar o evento de envio `formLogin.addEventListener('submit', ...)`;
- Usar `event.preventDefault()` para a página não recarregar;
- Criar uma condição `if/else` para verificar se o email OU a senha estão vazios;
- Exibir a mensagem de erro alterando o `textContent` do parágrafo.

🖼️ **Referência visual** (use como guia)
![Tela de Login](https://raw.githubusercontent.com/profjosereginaldo/tecweb-template/refs/heads/main/assets/login.png)
![Validação de Login](https://raw.githubusercontent.com/profjosereginaldo/tecweb-template/refs/heads/main/assets/validacao.png)

**3️⃣ Execução e teste**
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
- [ ] Validação implementada
- [ ] Projeto executa sem erros
- [ ] Commit realizado
- [ ] Pull Request criado para develop

## 📤 Entrega da Prática
1. Abra outro terminal do VSCode (isso garante que você esteja na pasta raiz).
2. Adicione os arquivos ao controle de versão e grave suas alterações. Substitua `#ID` pelo número da Issue (ex.: 10).
```bash
git add .
git commit -m "feat: conclui pratica03. Fecha #ID"
```
3. Envie suas alterações para o GitHub.
```bash
git push origin feature/pratica03
```
4. No GitHub, clique no botão **Compare & pull request**.
5. **Importante**: Certifique-se de que o **base repository** é o repositório do professor e a **base branch** é a `develop`.
6. Na descrição, escreva: `Nesta prática, implementei a validação de um formulário utilizando JavaScript. Fecha #ID`. Substitua `#ID` pelo número da Issue.
7. Clique em **Create pull request** e aguarde a correção do professor.

⚠️ **Erros comuns**
- Criar a branch de trabalho a partir de uma branch diferente da indicada na atividade;
- Esquecer de iniciar o Docker;
- Enviar PR para a branch errada.