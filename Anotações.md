
# Anotações Sobre Git e Github 📔

## O que é Git?

Git é um sistema de controle de versões gratuito, open source e desentralizado, ou seja, existe um servidor que hospedará os arquivos, mas os usuários envolvidos no projeto também terão uma cópia dos arquivos em suas máquinas para realizarem alterações caso necessário.

## O que é Github?

Github é uma plataforma de hospedagem de código para o sistema de versão Git. Ele é muito utilizado como portifólio por programadores por ser uma plataforma que permite armazenar diversos projetos e trabalhar em conjunto com outros desenvolvedores.

## Comandos Básicos do Git:

###  git config

Comando que mostra as configurações do GIT. No git config é possível visualizar e definir variáveis de configurações.

**Configurações do usuário:** --[no-] global    use global config

**Configurações do sitema:** --[no-] system    use system config file

**Configurações de um repositório específico em que você se encontra de modo local:** --[no-] local    use repositóry config file

* Definição de um nome de usuário:

**git config --global user.name ""**
                    
git config (comando) --global (local onde será armazenada essa informação) user.name (qual informação vai ser definidida) "" (local onde será inserido o nome de usuário)

* Definição do email:

**git config --global user.email xxx**
                     
git config (comando) --global (local onde será armazenada essa informação) user.email(qual informação vai ser definidida) xxx (email escolhido do usuário)
      
* Verificação da informação:

Visualização da informação, e no caso de uma alteração a visualização se a informação foi alterada:

**git config user.name**

**git config user.email**

* Verificar ou alterar o nome de uma Branch: 

**git config init.defaultBranch** (visualização do nome da Branch)

**git config --global init.defaultBranch main** (alteração do nome da Branch)
                             
git config (comando) --global (local de armazenamento da informação) init.defaultBranch (o que será alterado) main (alteração/novo nome da Branch)

* Configurações armazenadas:

**git config --global --list**
                    
git config (comando) --global (local de armazenamento a ser visualizado) --list (uma lista de tudo armazenado dentro do local escolhido)

### git clone 

comando que irá clonar o repositório remoto para o repositório local.

**git clone**  url do repositório novo nome desse repositório local

### Criação de uma nova pasta no terminal:

**mkdir** (comando que criará uma nova pasta) nome da nova pasta.

### Entrar na nova pasta criada:

**cd** (change diretory - comando que irá mudar o diretório) nome do diretório a ser aberto.

### git init 

Comando que irá transformar o diretório em um repositório

### Criação de commits:

salvamento das informações insridas ou alteradas no diretório.

**git commit -m ""**

git commit (comando) -m (permite a criação do nome do commit) "" (nome do commit)

### Alteração no nome do commit

**git commit --amend**

### git log

comando que mostra o histórico de commits

### git status

comando que mostra o status da árvore de trabalho e da área de preparação/index (stage area).

### Conectando seu diretório local a um repositório remoto:

**git remote add origin**

git remote add origin (comando) url do repositório

### Criação de diretórios vazios:

**touch**

touch (comando) arquivo vazio a ser criado
        
ex: touch README.md

diretórios vazios são considerados como Untracked Files - arquivos que o GIT ainda não conhece, se encontram no diretório mas não estava presente em nenhum commit anterior e não está na área de preparação.

ex: touch/ aulas/ .git keep (o comando .git keep é utilizado para o GIT reconhecer que é um arquivo vazio)

### git pull

Comando que manda as atualizações feitas no repositório remoto para o local.

### git push
envia as alterações salvas do repositório local para o repositório remoto.
        
**git push -u origin main**
                 
git push (comando) -u (set upstream - vai dizer para o Git para configurar o Branch main que vai vai estar no repositório local, como a Branch upstream da Branch do repositório remoto)