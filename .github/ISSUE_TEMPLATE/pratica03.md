---
name: "Prática 03"
about: "Template para criar a issue da pratica03"
title: "[Prática 03] – Interatividade com JavaScript"
labels: ["pratica03"]
assignees: ''
---

## 📌 Contexto
Após estruturar e estilizar a interface do portal **Aluno Online**, é necessário permitir que o usuário interaja com o sistema.

Nesta etapa, você irá implementar a página de **Login**, adicionando validação básica com JavaScript para garantir que os campos sejam preenchidos antes do envio do formulário.

## 🎯 Objetivo
Nesta prática, você irá:
- Construir uma página de Login com HTML5 e CSS3;
- Implementar validação de campos utilizando JavaScript;
- Manipular eventos e o DOM para exibir mensagens de erro.

## 🖼️ Referência visual
Utilize as imagens abaixo como guia:

![Tela de Login](https://raw.githubusercontent.com/profjosereginaldo/tecweb-template/refs/heads/main/assets/login.png)

![Validação de Login](https://raw.githubusercontent.com/profjosereginaldo/tecweb-template/refs/heads/main/assets/validacao.png)

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
2. Desenvolva no arquivo `login.html` a página de Login:
- Utilize a tag `<main>` para conter o formulário;
- Crie um `<form>` com os campos `email` e `senha`, e o botão `Entrar`;
- Cada campo deve possuir um `<label>`, um `<input>` e um `<p>` para exibir mensagens de erro;
- Adicione um `<footer>` para exibir um texto de direitos autorais.
3. Desenvolva no arquivo `style.css` os estilos da página de Login;
- Centralize o formulário na página utilizando Flexbox;
- Defina largura máxima para o container do formulário;
- Estilize campos, botão e mensagens de erro;
- Utilize as variáveis CSS já definidas anteriormente (`--cor-fundo`, `--cor-texto`).
4. Desenvolva no arquivo `main.js` a validação de formulário:
- Selecione os elementos do formulário usando `document.getElementById`;
- Adicione um *listener* para o evento `submit`;
- Utilize `event.preventDefault()` para evitar recarregamento;
- Verifique se email ou senha estão vazios;
- Exibi a mensagem de erro alterando o `textContent` do parágrafo.

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
4. Acesse no navegador: `http://localhost:5173`.
5. Teste os seguintes cenários:
- Submeter com campos vazios;
- Preencher apenas um campo;
- Preencher ambos os campos.

4️⃣ **Checklist antes de enviar**
- [ ] Branch criada a partir da develop
- [ ] Página de login estruturada e estilizada corretamente
- [ ] Validação implementada
- [ ] Mensagens de erro exibidas corretamente
- [ ] Projeto executa sem erros

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
6. Na descrição, escreva: `Nesta prática, implementei a página de login com validação utilizando JavaScript. Fecha #ID`. Substitua `#ID` pelo número da Issue.
7. Clique em **Create pull request** e aguarde a correção do professor.

⚠️ **Erros comuns**
- Criar a branch de trabalho a partir de uma branch diferente da indicada na atividade;
- Selecionar elementos incorretamente no DOM;
- Esquecer de limpar mensagens de erro anteriores;
- Esquecer de iniciar o Docker;
- Enviar PR para a branch errada.