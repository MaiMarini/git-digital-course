Aqui está o texto com todos os comandos entre crases, conforme solicitado:

## Santander Coders - Módulo 01: Git e Versionamento

# Git:

É uma ferramenta de controle de versão. É um software instalado localmente que ajuda a gerenciar e acompanhar as mudanças no código.

# GitHub:

É um serviço baseado na web que hospeda repositórios Git, oferecendo uma interface amigável e ferramentas adicionais para facilitar a colaboração e a integração contínua.

# Arquivo .gitignore

É um arquivo de configuração usado em repositórios Git para especificar quais arquivos e diretórios devem ser ignorados pelo sistema de controle de versão Git. Ele é especialmente útil para evitar a inclusão de arquivos desnecessários ou sensíveis no repositório, como arquivos temporários, binários, credenciais, entre outros.

- Evitar Confusão: Previne que arquivos que não são relevantes para o código-fonte sejam rastreados, como arquivos de configuração locais, caches, e logs.
- Segurança: Impede que informações sensíveis, como chaves API e credenciais, sejam acidentalmente commitadas no repositório.
- Redução de Tamanho: Exclui arquivos grandes e gerados automaticamente, como binários e arquivos de compilação, que não são necessários para todos os colaboradores.

# Comandos:

Configurações
`git config --global user.name "Nome do autor"`  
`git config --global user.email <email-do-autor>`

Geral  
`git status` => Informa o status das alterações do projeto, se houverem, modified, unstage e etc.  
`git clone <url>` => Clona um repositório existente.  
`git add <nome-do-arquivo>` => adiciona uma alteração no diretório de trabalho à área de alterações preparadas (stage).  
Exemplos:  
`git add .\README.md`  
`git commit -m “mensagem de commit”` => Cria um novo commit que tenha todos os conteúdos atuais do índice e a mensagem informada no registro log descrevendo as alterações.  
`git diff` => Usado para visualizar as diferenças entre duas versões de um arquivo ou entre duas branches no repositório Git, arquivos ou inputs.  
`git diff -- staged` => Visualizar as diferenças entre duas versões na área de alterações preparadas (stage).  
`git remote` => Sem argumentos, exibe uma lista dos ramos remotos existentes.  
`git diff <REMOTE-NAME>/<BRANCH-NAME>` => Visualizar as alterações baixadas com o `git fetch`.  
`git log` => Permite que você liste e filtre o histórico do projeto e pesquise alterações específicas.

---

# Desfazer commit antes do push:

`git restore <nome-do-arquivo>` => O comando restaura os arquivos que estão visíveis (working tree) para serem idênticos aos do commit atual (HEAD).  
Exemplos:  
Antes do git add  
`git restore <nome-do-arquivo>` (.\README.md)  
Depois do git add
`git restore --staged <nome-do-arquivo>` (.\README.md)

`git reset HEAD^ --hard` => Descartando as alterações.  
`git reset HEAD^ --soft` => Sem descartar as alterações.

---

`git push <REMOTE-NAME> <BRANCH-NAME>` => Enviar seus commits locais para um repositório remoto, permitindo que você compartilhe seu trabalho ou faça backup das suas alterações em um servidor remoto.  
`git fetch` => Comando básico usado para baixar conteúdos de um repositório remoto. É possível visualizar as alterações antes de realizar o pull. Necessário realizar o `git pull` em seguida.  
`git pull` => Usado para buscar e baixar conteúdo de repositórios remotos e fazer a atualização imediata ao repositório local para que os conteúdos sejam iguais. É uma combinação de outros dois comandos, `git fetch` seguido por `git merge`.

---

# Trabalhando com diferentes branches

Uma branch (ou ramificação) é um conceito fundamental no controle de versão de software, especialmente em sistemas de versionamento distribuído como o Git. Vamos explorar a definição de branch no contexto do desenvolvimento de software:

Definição de Branch  
Branch é uma linha paralela de desenvolvimento que permite que você trabalhe em uma funcionalidade, correção de bug ou experimentação sem afetar a linha principal (ou outras linhas) de desenvolvimento do projeto.

Comandos:  
`git branch` => Lista as branches.  
`git checkout <branch>` => Alterna para uma branch específica.  
`git branch <Nome-da-nova-branch>` => Cria nova branch.  
`git checkout -b <Nome-da-nova-branch>` => Cria nova branch e entra (checkout) na nova branch.

Alterar nome da branch  
`git branch -m <old-branch> <new-branch>`  
`git push origin --delete <old-branch-name>`  
`git push origin -u <new-branch-name>`

Git pull  
`git checkout <BRANCH-NAME-PRINCIPAL>`  
`git pull`  
`git pull origin`  
`git log --pretty=oneline` => Log da branch  
`git checkout <BRANCH-NAME-LOCAL>`  
`git merge <BRANCH-NAME-PRINCIPAL>` => Mescla uma branch na branch atual.

---
