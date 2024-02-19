# Clonando um repositório

O comando git clone é uma operação fundamental no Git que é usada para criar uma cópia local de um repositório Git existente. Quando você clona um repositório, você está essencialmente fazendo uma cópia completa de todo o histórico de commits, branches e arquivos desse repositório para o seu próprio sistema local.

A sintaxe básica do comando git clone é a seguinte:

```
git clone <URL_do_repositório>
```

Onde ```<URL_do_repositório>``` é o endereço do repositório remoto que você deseja clonar. Isso pode ser um URL HTTPS, um URL SSH ou outro tipo de URL suportado pelo Git.

Quando você executa git clone, o Git realiza várias etapas:

- `Criação de um novo diretório:` O Git cria um novo diretório no seu sistema de arquivos onde a cópia do repositório será armazenada.

Inicialização do diretório como um repositório Git: O Git inicializa o diretório recém-criado como um repositório Git local.

- `Recuperação de todo o histórico de commits:` O Git recupera todos os commits do repositório remoto, incluindo todos os branches e tags associados.

- `Criação de uma cópia dos arquivos:` O Git cria uma cópia local de todos os arquivos do repositório remoto no diretório recém-criado.

- `Configuração do repositório remoto:` O Git configura automaticamente o repositório remoto original como um "remoto" chamado "origin" no seu repositório local. Isso permite que você facilmente sincronize suas alterações com o repositório remoto original usando git push e git pull.

Nessa aula iremos clonar este repositório na máquina linux.

```
git clone git@github.com:filhotecmail/Curso-versionamento-GIT-Udemy.git
```
