---
name: "Prática 02"
about: "Template para criar a issue da pratica02"
title: "[Prática 02] – Layout com CSS/Flexbox"
labels: ["pratica02"]
assignees: ''
---

## 🎯 Objetivo
Nesta prática, você irá:
- Aplicar layout com CSS e Flexbox para estruturar visualmente a Dashboard do portal Aluno Online.

## 📝 Instruções da Atividade
**1️⃣ Preparação do ambiente**
1. Abra o **Visual Studio Code** na pasta do seu repositório.
2. Abra um terminal e certifique-se de que está na branch `develop`.
```bash
git checkout develop
```
3. Crie e alterne para a branch desta prática.
```bash
git checkout -b feature/pratica02
```

**2️⃣ Implementação do código**
1. No painel esquerdo do VSCode, localize a pasta `aluno-online-vanilla`.
2. Desenvolva no arquivo `style.css` os estilos da página Dashboard:
- **Root**: Definir as variáveis `--cor-fundo: #e9e9e9` e `--cor-texto: #303030` e definir `font-family: system-ui, Avenir, Helvetica, Arial, sans-serif`, `font-weight: 400` e `line-height: 1.6`;
- **Reset**: Resetar `margin` e `padding` e definir `box-sizing: border-box`;
- **Body**: Definir `color: var(--cor-texto)`, `display: flex` e `min-height: 100vh`;
- **Sidebar**: Definir `background-color: var(--cor-fundo)`, `flex: 0 0 250px` e `padding: 1rem`;
- **Área de Conteúdo**: Definir `flex: 1` e `padding: 1.5rem`;
- **Menu**: Definir `padding: 1rem`. Para cada item do menu, definir   `color: var(--cor-texto)`, `display: block`, `font-weight: bold`, 
`padding: 0.5rem` e `text-decoration: none`;
- **Topbar**: Definir `display: flex`, `align-items: center`, `gap: 0.5rem`, `margin-bottom: 2rem` e `justify-content: space-between`;
- **Conteúdo Principal**: Definir `display: flex`, `flex-direction: column`, `gap: 1.5rem` e `padding-top: 1rem`;
- **Blocos de Conteúdo**: Definir `border: 1px solid var(--cor-fundo)`, `border-radius: 0.5rem` e `max-width: 50vw`. Para o título do bloco, definir `background-color: var(--cor-fundo)`, `border-top-left-radius: 0.5rem`, `border-top-right-radius: 0.5rem` e `line-height: 1.8`.

🖼️ **Referência visual** (use como guia)
![Tela de Dashboard](https://raw.githubusercontent.com/profjosereginaldo/tecweb-template/refs/heads/main/assets/dashboard.png)

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
- [ ] Estilização implementada
- [ ] Projeto executa sem erros
- [ ] Commit realizado
- [ ] Pull Request criado para develop

## 📤 Entrega da Prática
1. Abra outro terminal do VSCode (isso garante que você esteja na pasta raiz).
2. Adicione os arquivos ao controle de versão e grave suas alterações. Substitua `#ID` pelo número da Issue (ex.: 10).
```bash
git add .
git commit -m "feat: conclui pratica02. Fecha #ID"
```
3. Envie suas alterações para o GitHub.
```bash
git push origin feature/pratica02
```
4. No GitHub, clique no botão **Compare & pull request**.
5. **Importante**: Certifique-se de que o **base repository** é o repositório do professor e a **base branch** é a `develop`.
6. Na descrição, escreva: `Nesta prática, implementei a estilização da página Dashboard utilizando CSS e Flexbox. Fecha #ID`. Substitua `#ID` pelo número da Issue.
7. Clique em **Create pull request** e aguarde a correção do professor.

⚠️ **Erros comuns**
- Criar a branch de trabalho a partir de uma branch diferente da indicada na atividade;
- Esquecer de iniciar o Docker;
- Enviar PR para a branch errada.