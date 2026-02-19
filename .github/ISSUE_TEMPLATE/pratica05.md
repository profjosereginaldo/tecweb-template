---
name: "Prática 05"
about: "Template para criar a issue da pratica05"
title: "[Prática 05] – Props, Estado e Eventos em React"
labels: ["pratica05"]
assignees: ''
---

## 🎯 Objetivo
Nesta prática, você irá:
- Usar props para reutilizar componentes e useState para controlar dados digitados pelo usuário;
- Implementar e tratar eventos (onChange, onSubmit) para capturar e manipular interações do usuário.

## 📝 Instruções da Atividade
**1️⃣ Preparação do ambiente**
1. Abra o **Visual Studio Code** na pasta do seu repositório.
2. Abra um terminal e certifique-se de que está na branch `develop`.
```bash
git checkout develop
```
3. Crie e alterne para a branch desta prática.
```bash
git checkout -b feature/pratica05
```

**2️⃣ Implementação do código**
1. No painel esquerdo do VSCode, localize a pasta `aluno-online-react`.
2. Desenvolva os componentes solicitados. 
- **InputEmail**: Criar `InputEmail.jsx` contendo label, campo de email e um parágrafo para exibir mensagens de erro.
- **InputSenha**: Criar `InputSenha.jsx` contendo label, campo de senha  e um parágrafo para exibir mensagens de erro.
- Cada componente deve ser criado como função e exportado como `default`.
- Cada componente deve possuir seu próprio arquivo CSS.
- Os componentes devem receber **props** para exibir o valor do campo (`value`), atualizar o estado quando o usuário digitar (`onChange`) e exibir o erro de validação.
3. Desenvolva a página solicitada.
- **Login**: Criar `Login.jsx` e integrar todos os componentes.
- Crie quatro estados usando useState: `email`, `errorEmail`, `senha` e `errorSenha`.
- Passe os valores e funções de atualização para os componentes via props.
- Crie um evento `handleSubmit()` para evitar o recarregamento da página e validar os dados do formulário.
4. Crie o arquivo `Login.css` com os estilos da página de Login.
- Ajustar o `#root` para `display: flex` e `flex-direction: column`.
- **Área de Conteúdo**: Criar uma classe para o `<main>` com `border: 1px solid var(--cor-fundo)`, `border-radius: 0.5rem`, `display: flex`, `flex: 1`, `flex-direction: column`, `justify-content: center`, `margin: 2.0rem auto`, `max-width: 400px`, `padding: 1rem` e `width: 100%`;
- **Botão**: Definir `background-color: var(--cor-fundo)`, `border: none`, `border-radius: 0.25rem`, `cursor: pointer`, `font-size: 1.1rem`, `padding: 0.5rem 1rem`, `margin-top: 1rem` e `width: 100%`;
- **Mensagens de erro**: Definir `color: #a70000` e `margin-bottom: 1rem`;
- **Rodapé**: Definir `font-size: 0.9rem`, `margin-bottom: 0.5rem`, `margin-top: 0.5rem`, e `text-align: center`.
5. Renderize o componente `Login` no arquivo `App.jsx`.

🖼️ **Referência visual** (use como guia)
![Tela de Login](https://raw.githubusercontent.com/profjosereginaldo/tecweb-template/refs/heads/main/assets/login.png)
![Validação de Login](https://raw.githubusercontent.com/profjosereginaldo/tecweb-template/refs/heads/main/assets/validacao.png)

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
git commit -m "feat: conclui pratica05. Fecha #ID"
```
3. Envie suas alterações para o GitHub.
```bash
git push origin feature/pratica05
```
4. No GitHub, clique no botão **Compare & pull request**.
5. **Importante**: Certifique-se de que o **base repository** é o repositório do professor e a **base branch** é a `develop`.
6. Na descrição, escreva: `Nesta prática, implementei props e estado nos componentes React. Fecha #ID`. Substitua `#ID` pelo número da Issue.
7. Clique em **Create pull request** e aguarde a correção do professor.

⚠️ **Erros comuns**
- Criar a branch de trabalho a partir de uma branch diferente da indicada na atividade;
- Esquecer de iniciar o Docker;
- Enviar PR para a branch errada.