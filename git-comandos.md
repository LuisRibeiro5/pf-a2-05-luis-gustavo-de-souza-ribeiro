# Comandos Git essenciais

## 1. Configuração do repositório

### `git init`
Inicializa um novo repositório Git no diretório atual.
- Exemplo: `git init`
- Exemplo: `git init .`

### `git clone`
Clona um repositório remoto para um diretório local.
- Exemplo: `git clone https://github.com/usuario/repositorio.git`
- Exemplo: `git clone git@github.com:usuario/repositorio.git`

## 2. Trabalhando com branches

### `git branch`
Lista branches locais ou cria um novo branch.
- Exemplo: `git branch`
- Exemplo: `git branch develop`

### `git checkout`
Muda de branch ou restaura arquivos do histórico.
- Exemplo: `git checkout develop`
- Exemplo: `git checkout -b feature/login`

### `git switch`
Altera branches ou cria uma nova branch de forma moderna.
- Exemplo: `git switch main`
- Exemplo: `git switch -c hotfix/1.0.1`

### `git merge`
Integra um branch ao branch atual.
- Exemplo: `git merge feature/totem-checkin`
- Exemplo: `git merge --no-ff release/1.0.0`

### `git rebase`
Reaplica commits em outro ponto do histórico para manter linearidade.
- Exemplo: `git rebase develop`
- Exemplo: `git rebase --onto main release/1.0.0`

## 3. Preparação e commit

### `git add`
Adiciona mudanças à área de staging para commit.
- Exemplo: `git add .`
- Exemplo: `git add git-comandos.md gitflow-diretrizes.md`

### `git commit`
Cria um novo commit com as alterações de staging.
- Exemplo: `git commit -m "feat: documento inicial de comandos Git"`
- Exemplo: `git commit -am "docs: atualizar guia de comandos"`

### `git status`
Mostra o estado dos arquivos no repositório.
- Exemplo: `git status`
- Exemplo: `git status -s`

### `git diff`
Exibe diferenças entre o working tree, staging e histórico.
- Exemplo: `git diff`
- Exemplo: `git diff --staged`

## 4. Histórico e revisão

### `git log`
Mostra o histórico de commits.
- Exemplo: `git log --oneline --graph --decorate`
- Exemplo: `git log origin/main..HEAD`

### `git show`
Exibe detalhes de um commit ou objeto específico.
- Exemplo: `git show HEAD`
- Exemplo: `git show v1.0.0`

### `git reset`
Descarta mudanças ou move o ponteiro de branch.
- Exemplo: `git reset --soft HEAD~1`
- Exemplo: `git reset --hard HEAD`

### `git revert`
Cria um novo commit que desfaz um commit anterior.
- Exemplo: `git revert HEAD`
- Exemplo: `git revert --no-commit abc1234`

## 5. Trabalhando com repositórios remotos

### `git remote`
Gerencia repositórios remotos.
- Exemplo: `git remote -v`
- Exemplo: `git remote add origin https://...`

### `git fetch`
Baixa objetos e refs do repositório remoto.
- Exemplo: `git fetch origin`
- Exemplo: `git fetch --all`

### `git pull`
Busca e integra mudanças do remoto no branch atual.
- Exemplo: `git pull origin develop`
- Exemplo: `git pull --rebase`

### `git push`
Envia commits para o repositório remoto.
- Exemplo: `git push origin main`
- Exemplo: `git push -u origin develop`

## 6. Tags e lançamentos

### `git tag`
Cria tags para marcar releases.
- Exemplo: `git tag v1.0.0`
- Exemplo: `git tag -a v1.0.0 -m "Release 1.0.0"`

### `git push --tags`
Envia tags locais para o remoto.
- Exemplo: `git push origin --tags`
- Exemplo: `git push --tags origin`

## 7. Colaboração e recuperação

### `git stash`
Guarda temporariamente alterações não comitadas.
- Exemplo: `git stash`
- Exemplo: `git stash pop`

### `git cherry-pick`
Aplica um commit específico em outro branch.
- Exemplo: `git cherry-pick abc1234`
- Exemplo: `git cherry-pick --no-commit abc1234`

### `git bisect`
Localiza o commit que introduziu um bug.
- Exemplo: `git bisect start`
- Exemplo: `git bisect bad`

### `git blame`
Mostra autoria linha a linha de um arquivo.
- Exemplo: `git blame src/app.js`
- Exemplo: `git blame -L 10,30 docs/README.md`

## 8. Limpeza e reorganização

### `git gc`
Otimiza o repositório local e reduz espaço em disco.
- Exemplo: `git gc`
- Exemplo: `git gc --aggressive`

### `git clean`
Remove arquivos não rastreados do diretório de trabalho.
- Exemplo: `git clean -n`
- Exemplo: `git clean -f -d`
