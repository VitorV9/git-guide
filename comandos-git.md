# 💻 Comandos Essenciais do Git

Um guia de consulta rápida com os comandos mais utilizados no fluxo de desenvolvimento, organizados por etapas de trabalho.

## ⚙️ 1. Configuração Inicial
Antes de começar a versionar seu código, você precisa se identificar. Esses comandos configuram sua assinatura nos commits.

* `git config --global user.name "Seu Nome"`: Define o nome do autor.
* `git config --global user.email "seu-email@exemplo.com"`: Define o e-mail do autor.
* `git config --list`: Mostra todas as configurações atuais do seu Git.

## 🚀 2. Iniciando um Projeto
Comandos para criar um repositório do zero ou trazer um projeto existente para a sua máquina.

* `git init`: Transforma a pasta atual em um repositório Git local.
* `git clone <url-do-repositorio>`: Faz o download de um repositório remoto (do GitHub, por exemplo) para a sua máquina.

## 📝 3. O Fluxo Diário (Adicionar e Salvar)
Estes são os comandos que você mais vai usar para registrar suas alterações.

* `git status`: Exibe o estado atual do repositório (quais arquivos foram modificados, adicionados ou deletados).
* `git add <nome-do-arquivo>`: Prepara um arquivo específico para ser salvo (coloca na *staging area*).
* `git add .`: Prepara **todas** as alterações feitas no diretório atual de uma só vez.
* `git commit -m "mensagem do commit"`: Salva as alterações preparadas no histórico. *(Dica: Lembre-se de aplicar as regras do [Conventional Commits](./CONTRIBUTING.md) aqui!)*

## 🔀 4. Trabalhando com Branches (Ramificações)
Essencial para criar novas funcionalidades ou fazer testes sem quebrar o código principal, facilitando muito o trabalho em equipe.

* `git branch`: Lista todas as branches locais. A branch atual ficará marcada com um asterisco (*).
* `git checkout -b <nova-branch>`: Cria uma nova branch e já muda para ela imediatamente.
* `git checkout <nome-da-branch>`: Navega para uma branch já existente.
* `git merge <nome-da-branch>`: Junta as alterações da branch especificada para dentro da branch em que você está no momento.

## ☁️ 5. Sincronizando com o Remoto
Como enviar seu código para a nuvem e baixar as atualizações feitas por outras pessoas.

* `git remote add origin <url>`: Conecta o seu repositório local a um servidor remoto.
* `git push -u origin <branch>`: Envia seus commits locais para o repositório remoto. O `-u` é usado na primeira vez para vincular a branch local com a remota.
* `git pull`: Puxa as atualizações do servidor remoto e já tenta mesclar com o seu código local.
* `git fetch`: Apenas baixa as informações de atualizações do remoto, mas não altera seus arquivos locais (útil para verificar o que mudou antes de aplicar).

## ⏪ 6. Histórico e Correções Rápidas
Comandos úteis para ver o que aconteceu no projeto ou desfazer pequenos erros.

* `git log --oneline`: Mostra o histórico de commits de forma resumida, um por linha.
* `git commit --amend -m "nova mensagem"`: Substitui a mensagem do seu último commit (use apenas se o commit ainda não tiver sido enviado com `push`).
* `git reset HEAD <arquivo>`: Remove um arquivo da área de preparação (desfaz o `git add`), mas mantém as suas alterações no código.
* `git checkout -- <arquivo>`: **Cuidado!** Descarta todas as alterações locais feitas em um arquivo, voltando ao estado do último commit.

---
💡 **Dica sobre o `.gitignore`:**
Sempre crie um arquivo chamado `.gitignore` na raiz do seu projeto. Dentro dele, você pode listar nomes de arquivos ou pastas (como `__pycache__/`, `.env` ou `node_modules/`) que o Git deve ignorar e nunca enviar para o repositório.