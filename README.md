# My First Steps

## Questão 1: Meu repositório
https://github.com/SkyvengerLL/my_first_steps

## Questão 2: Vinculando repositório com o diretório local

Esses passos foram feitos em uma máquina windows 10.
Entrado no diretório da minha maquina que será vinculado, foi pressionado o botão direito e selecionado a opção "*Git Bash Here*". Então no Git Bash:

### Iniciando git no diretório:

> frp20@DESKTOP-6I1M3DP MINGW64 ~/OneDrive/Documentos/Lovelance/myfirststeps (master)
$ git init
  Initialized empty Git repository in C:/Users/frp20/OneDrive/Documentos/Lovelance/myfirststeps/.git/

### Vinculando ao repositório do github:

> frp20@DESKTOP-6I1M3DP MINGW64 ~/OneDrive/Documentos/Lovelance/myfirststeps (master)
$ git remote add origin git@github.com:SkyvengerLL/my_first_steps.git

### Vinculando chave ssh:
Após abrir o Power shell no modo admin, foi digitado o comando: 
> Get-Service -Name ssh-agent | Set-Service -StartupType Manual

Isso foi necessário pois no automático o ssh-agent estava bloqueado impedindo de criar uma chave ssh para conectar no github.


### Iniciando o ssh-agent

> $ eval "$(ssh-agent -s)"
#gerando chave:
ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (C:\Users\frp20/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in C:\Users\frp20/.ssh/id_rsa.
Your public key has been saved in C:\Users\frp20/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:d3zP/4qlUs/c3k/eYeb1V42qLOXDcw2eFT9kZuq/ptc frp20@DESKTOP-6I1M3DP
#Adicionando a chave para ser usável:
$ ssh-add
Enter passphrase for C:\Users\frp20/.ssh/id_rsa:
Identity added: C:\Users\frp20/.ssh/id_rsa (frp20@DESKTOP-6I1M3DP)

Pós isso tudo, registrar chave no github.

### Sincronizando com o repositório:

> frp20@DESKTOP-6I1M3DP MINGW64 ~/OneDrive/Documentos/Lovelance/myfirststeps (master)
$ git pull origin master --allow-unrelated-histories
From github.com:SkyvengerLL/my_first_steps
branch            master     -> FETCH_HEAD
Merge made by the 'recursive' strategy.
 README.md | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 README.md