---
name: "Prática 04"
about: "Template para criar a issue da pratica04"
title: "[Prática 04] – Componentes com React"
labels: ["pratica04"]
assignees: ''
---

## 🎯 Objetivo
Nesta prática, você irá:
- Transformar o layout estático do portal Aluno Online em uma aplicação React organizada em componentes reutilizáveis.

## 📝 Instruções da Atividade
**1️⃣ Preparação do ambiente**
1. Abra o **Visual Studio Code** na pasta do seu repositório.
2. Abra um terminal e certifique-se de que está na branch `develop`.
```bash
git checkout develop
```
3. Crie e alterne para a branch desta prática.
```bash
git checkout -b feature/pratica04
```

**2️⃣ Implementação do código**
1. No painel esquerdo do VSCode, localize a pasta `aluno-online-react`.
2. Crie uma nova pasta chamada `src/components`.
3. Desenvolva os componentes solicitados. 
- **Sidebar**: Criar `Sidebar.jsx` com o logo e a navegação lateral.
- **Topbar**: Criar `Topbar.jsx` com a saudação e o avatar do usuário.
- **DashboardCard**: Criar `DashboardCard.jsx` para os cartões de informação (Mural de Avisos, Calendário Acadêmico, etc.).
- Cada componente deve ser criado como função e exportado como `default`.
- Cada componente deve possuir seu próprio arquivo CSS.
- Não há uso de state ou eventos nos componentes.
4. Crie uma nova pasta chamada `src/pages`.
5. Desenvolva a página solicitada.
- **Dashboard**: Criar `Dashboard.jsx` e integrar todos os componentes.
6. Renderize o componente `Dashboard` no arquivo `App.jsx`.
7. No arquivo `App.css` crie um estilo para o id `#root`.
- Definir `display: flex` e `flex: 1`.
8. No arquivo `index.css`, mantenha apenas os estilos globais da aplicação:
- **Root**: Definir as variáveis `--cor-fundo: #e9e9e9` e `--cor-texto: #303030` e definir `font-family: system-ui, Avenir, Helvetica, Arial, sans-serif`, `font-weight: 400` e `line-height: 1.6`;
- **Reset**: Resetar `margin` e `padding` e definir `box-sizing: border-box`;
- **Body**: Definir `color: var(--cor-texto)`, `display: flex` e `min-height: 100vh`.
- **Área de Conteúdo**: Definir `flex: 1` e `padding: 1.5rem`; 

🖼️ **Referência visual** (use como guia)
![Tela de Dashboard](https://raw.githubusercontent.com/profjosereginaldo/tecweb-template/refs/heads/main/assets/dashboard.png)

**3️⃣ Execução e teste**
1. No terminal, acesse a pasta do projeto.
```bash
cd praticas/aluno-online-react
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
- [ ] Componentes importados e renderizados corretamente
- [ ] Cada componente possui seu próprio arquivo CSS
- [ ] Projeto executa sem erros
- [ ] Commit realizado
- [ ] Pull Request criado para develop

## 📤 Entrega da Prática
1. Abra outro terminal do VSCode (isso garante que você esteja na pasta raiz).
2. Adicione os arquivos ao controle de versão e grave suas alterações. Substitua `#ID` pelo número da Issue (ex.: 10).
```bash
git add .
git commit -m "feat: conclui pratica04. Fecha #ID"
```
3. Envie suas alterações para o GitHub.
```bash
git push origin feature/pratica04
```
4. No GitHub, clique no botão **Compare & pull request**.
5. **Importante**: Certifique-se de que o **base repository** é o repositório do professor e a **base branch** é a `develop`.
6. Na descrição, escreva: `Nesta prática, implementei os componentes de um portal utilizando React. Fecha #ID`. Substitua `#ID` pelo número da Issue.
7. Clique em **Create pull request** e aguarde a correção do professor.

⚠️ **Erros comuns**
- Criar a branch de trabalho a partir de uma branch diferente da indicada na atividade;
- Esquecer de iniciar o Docker;
- Enviar PR para a branch errada.