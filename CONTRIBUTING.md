# 🤝 Guia de Contribuição e Commits Convencionais

Os **Conventional Commits** são um conjunto de regras para formar um histórico de commits explícito e padronizado. Seguir esse padrão auxilia no trabalho em equipe durante o GitFlow, melhora o versionamento e facilita a geração automática de changelogs.

A estrutura básica de um commit deve seguir este formato:
`<tipo>[escopo opcional]: <descrição>`

---

## 📌 Principais Tipos de Commits

### ✨ 1. Feat (Feature)
Introdução de uma nova funcionalidade no código.
* **Simples:** `feat: adiciona barra de busca na tela inicial`
* **Com escopo:** `feat(products): implementa filtro por faixa de preço`

### 🐛 2. Fix (Bug fix)
Correção de um bug ou erro no sistema.
* **Simples:** `fix: corrige erro de digitação no título da página`
* **Com escopo:** `fix(database): resolve problema de conexões travadas no pool`

### 📚 3. Docs (Documentação)
Alterações exclusivas na documentação, como arquivos README, wikis ou comentários de código.
* **Simples:** `docs: adiciona link do deploy no README`
* **Com escopo:** `docs(api): documenta novos parâmetros do endpoint de login`

### 💎 4. Style (Estilização/Formatação)
Alterações que não afetam o significado ou a lógica do código (espaços em branco, formatação, ponto e vírgula faltando, linting).
> ⚠️ **Nota:** Não confunda com mudanças de CSS em uma interface. Alterações de design/layout costumam ser classificadas como `feat` ou `fix`.
* **Simples:** `style: remove linhas em branco duplicadas`
* **Com escopo:** `style(utils): ajusta a indentação de 4 para 2 espaços`

### ♻️ 5. Refactor (Refatoração)
Uma alteração no código que não corrige um bug nem adiciona uma nova funcionalidade, mas melhora a estrutura interna ou legibilidade do código.
* **Simples:** `refactor: melhora a legibilidade da função de cálculo de juros`
* **Com escopo:** `refactor(views): extrai lógica do controller para um service isolado`

### 🧪 6. Test (Testes)
Adição de testes que estavam faltando ou correção de testes existentes.
* **Simples:** `test: adiciona testes unitários para o service de usuários`

### 🔧 7. Chore (Tarefas Cotidianas)
Atualizações de tarefas de build, configurações de ferramentas, pacotes de dependências ou itens que não modificam o código de produção.
* **Simples:** `chore: atualiza a versão do pandas para 2.2.0`

---

## ⚙️ Outros Tipos Opcionais

* **`perf`**: Mudança de código focada em melhorar o desempenho.
* **`ci`**: Mudanças nos arquivos e scripts de configuração de CI/CD (ex: GitHub Actions, GitLab CI).
* **`build`**: Alterações que afetam o sistema de build ou dependências externas (ex: npm, pip, maven).