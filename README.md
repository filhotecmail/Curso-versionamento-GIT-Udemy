# Curso-versionamento-GIT-Udemy
Repositório criado para treimanento e aulas do curso de GIT da Udemy

## Ambiente de Testes e Aprendizado

Ubuntu 22.04 TLS 

O Ubuntu é um sistema operacional baseado em linux kernel.
O "22.04 LTS" se refere à versão específica do Ubuntu. "22.04" significa que foi lançado em abril de 2022. "LTS" significa "Long Term Support" (Suporte de Longo Prazo). 
Isso significa que essa versão do Ubuntu receberá atualizações e correções de segurança por um período prolongado, geralmente cerca de 5 anos. 
Isso é importante porque garante que o sistema seja seguro e estável por um longo tempo.
Por padrão ao instalar o Ubuntu, o Git já vem instalado.

Verificando a versão instalada do git

```bash
 git -- version


$ git version 2.25.1
```

## Arquivo de Configuração do Git:
O Git armazena suas configurações em um arquivo de configuração. Esse arquivo pode ter configurações específicas para o sistema, usuário ou repositório. Aqui estão os principais arquivos de configuração do Git:
- **Global:** Armazena configurações específicas do usuário e se aplicam a todos os repositórios Git em um sistema. Geralmente está localizado em `~/.gitconfig`.
- **Local:** Armazena configurações específicas de um repositório Git específico. Está localizado dentro do diretório `.git` do repositório.
- **Sistema:** Armazena configurações específicas do sistema que se aplicam a todos os usuários e repositórios Git em um sistema. Está localizado em `/etc/gitconfig`.

## Comando `git config`:
O comando `git config` é usado para definir, visualizar ou modificar configurações do Git. Ele oferece várias opções para manipular as configurações. Aqui estão algumas das opções mais comuns:
- `git config --global <chave> <valor>`: Define uma configuração global do Git.
- `git config --local <chave> <valor>`: Define uma configuração local específica para um repositório.
- `git config --system <chave> <valor>`: Define uma configuração do sistema do Git.
- `git config --get <chave>`: Obtém o valor de uma chave específica.
- `git config --unset <chave>`: Remove uma configuração específica.
- `git config --list`: Lista todas as configurações.

## Propriedades do Arquivo de Configuração:
O arquivo de configuração do Git consiste em pares de chave e valor. As chaves representam as configurações e os valores são suas respectivas configurações. Algumas das propriedades mais comuns incluem:
- `user.name`: Nome do usuário.
- `user.email`: Endereço de e-mail do usuário.
- `core.editor`: Editor de texto padrão para mensagens de commit.
- `alias`: Atalhos para comandos Git.

## Vamos configurar seu Arquivo de configuração GIT de forma Global
 Após a instalação do Git, é recomendável configurar alguns elementos, como a identificação do usuário, que será associada a cada commit feito no Git.
 Para evitar a necessidade de configurar essa identificação em cada repositório Git individualmente, o texto sugere que você pode fazer essa configuração de forma global. Isso significa que você pode definir suas informações de identificação uma vez e elas serão 
 aplicadas a todos os repositórios Git em sua máquina.

Para realizar essa configuração global, você pode criar um arquivo chamado .gitconfig na raiz do diretório do seu usuário home. Neste arquivo, você pode definir configurações como seu nome de usuário e endereço de e-mail associado ao seu perfil Git. Essas configurações serão então aplicadas a todos os seus repositórios Git, garantindo consistência em seus commits e facilitando o trabalho em vários projetos.

```bash
git config --global user.name "Seu Nome e Sobrenome"
git config -- global user.email "seuemail@mail.com"
```
## Nota
No arquivo de configuração do Git (geralmente chamado .gitconfig), você pode definir propriedades personalizadas, além das propriedades padrão fornecidas pelo Git. Isso permite que você armazene informações adicionais que podem ser úteis para seu fluxo de trabalho ou para a integração com outras ferramentas.

por exemplo
```bash
git config --global user.phone "99999999"

[user]
        name = Seu Nome e Sobrenome
        email = seuemail@mail.com
        phone = 9999999999
```

### Visualizando conteúdo do arquivo

```bash
 cat .gitconfig
```
A saída deverá ser equivalente á

```bash
$ cat .gitconfig
 
[user]
	name = Firstname Lastname
	email = firstname.lastname@mail.com
        phone = 9999999999
```
# Aula 2 - Assinatura dos commits

Nesta aula, aprenderemos sobre a configuração avançada de commits assinados no Git. Assinar seus commits é uma prática altamente recomendada para garantir a integridade e autenticidade do código que você está contribuindo para um repositório. 
Usaremos o utilitário gpg para gerar uma chave e assinar nossos commits.

### Por que assinar commits?
A assinatura de commits é importante por várias razões:

- `Integridade dos Commits:` Garante que os commits não foram adulterados desde que foram criados, fornecendo uma camada adicional de segurança.
- `Autenticidade:` Confirma que os commits foram realmente feitos por você e não por outra pessoa, impedindo a falsificação de identidade.
- `Confiança na Colaboração:` Ao assinar seus commits, você constrói confiança com outros colaboradores e mantenedores de projetos, mostrando que você é o verdadeiro autor das alterações.

### Aula: Introdução ao GnuPG (GNU Privacy Guard)

#### Visão Geral:
O GNU Privacy Guard (GnuPG), comumente referido como `gpg`, é uma ferramenta de criptografia de dados e assinatura digital de código aberto amplamente utilizada. Nesta aula, vamos explorar o GnuPG e aprender como ele é usado para garantir a segurança dos dados por meio de criptografia e assinaturas digitais.

#### Objetivos:
- Compreender o que é o GnuPG e suas funcionalidades.
- Aprender a criar e gerenciar chaves de criptografia.
- Explorar o processo de criptografia de dados e assinatura digital usando o GnuPG.

> "O GnuPG é uma ferramenta poderosa para garantir a segurança dos dados por meio de criptografia e assinaturas digitais."

### Criação de Chaves de Criptografia

```
 gpg --full-generate-key

Email address: email@email@gmail.com
You selected this USER-ID:
    "sudo gpg --full-generate-key <email@email@gmail.com>"

```

Ele vai perguntar se você quer também criar a propriedade Realname, em seguida vai pedir para voce criar uma senha para a chave.

```
Change (N)ame, (E)mail, or (O)kay/(Q)uit? n
Real name: Carlos Alberto Dias da Silva Filho
You selected this USER-ID:
    "Carlos Alberto Dias da Silva Filho <email@email@gmail.com>"

Change (N)ame, (E)mail, or (O)kay/(Q)uit? o
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.

gpg: /home/carlos/.gnupg/trustdb.gpg: trustdb created

gpg: key XXXXXXXXXX7DEBB3 marked as ultimately trusted
gpg: directory '/home/carlos/.gnupg/openpgp-revocs.d' created
gpg: revocation certificate stored as '/home/carlos/.gnupg/openpgp-revocs.d/XXXXXXXXXXXC772F53F9901B28200FDD5DA7DEBB3.rev'
public and secret key created and signed.

pub   rsa3072 2024-02-18 [SC] [expires: 2026-02-17]
      XXXXXXXXXXXC772F53F9901B28200FDD5DA7DEBB3
uid                      Carlos Alberto Dias da Silva Filho <email@email@gmail.com>
sub   rsa3072 2024-02-18 [E] [expires: 2026-02-17]

```

Verifique a chave criada.

```bash
gpg --list-secret-keys --keyid-format=long

gpg: checking the trustdb
gpg: marginals needed: 3  completes needed: 1  trust model: pgp
gpg: depth: 0  valid:   1  signed:   0  trust: 0-, 0q, 0n, 0m, 0f, 1u
gpg: next trustdb check due at 2026-02-17
/home/carlos/.gnupg/pubring.kbx
-------------------------------
sec   rsa3072/XXXXXXXXXX7DEBB3 2024-02-18 [SC] [expires: 2026-02-17]
      XXXXXXXXXXC772F53F9901B28200FDD5DA7DEBB3
uid                 [ultimate] Carlos Alberto Dias da Silva Filho <email@email@gmail.com>
ssb   rsa3072/XXXXXXXXXX881A08 2024-02-18 [E] [expires: 2026-02-17]

```
Este comando gpg ```--list-secret-keys --keyid-format=long ``` é usado para listar as chaves secretas (privadas) disponíveis no sistema usando o utilitário GnuPG (GPG), que é uma implementação de código aberto do PGP (Pretty Good Privacy), um sistema de criptografia de chave pública.

### Aqui está uma explicação da saída:

- `sec:` Indica que a entrada é uma chave secreta (privada).
- `rsa3072/XXXXXXXXXX7DEBB3:` Identificador da chave, que consiste no algoritmo de criptografia (RSA com comprimento de chave de 3072 bits) seguido pelo identificador único da chave.
- `2024-02-18:` Data de criação da chave.
- `[SC]:` Indica que a chave é usada para assinar (S) e criptografar (C).
- `[expires: 2026-02-17]:` Indica que a chave expira em 17 de fevereiro de 2026.
- `XXXXXXXXXXC772F53F9901B28200FDD5DA7DEBB3:` O identificador único da chave, usado para referenciar a chave em operações GPG.
- `uid [ultimate] Carlos Alberto Dias da Silva Filho <email@email@gmail.com>:` A identificação do usuário associado à chave, que inclui o nível de confiança (ultimate), o nome do usuário e o endereço de e-mail.
- `ssb:` Indica que a entrada é uma subchave.
- `rsa3072/XXXXXXXXXX881A08:` Identificador da subchave.
- `[E]:` Indica que a subchave é usada apenas para criptografia de dados.
- `[expires: 2026-02-17]:` Indica que a subchave expira em 17 de fevereiro de 2026.

### Adicionando a chave à sua configuração Git no ficheiro .gitconfig

```
git config --global commit.gpgsign true

```
Esse comando configura o Git globalmente para assinar automaticamente seus commits com GPG (GNU Privacy Guard). Quando você faz um commit em um repositório Git após executar esse comando, o Git solicitará a assinatura usando a chave GPG configurada em sua máquina. Isso ajuda a garantir a autenticidade e integridade dos seus commits, fornecendo uma forma de verificar se os commits foram feitos por você e se não foram adulterados.

se você visualizar agora as configurações, terá uma saída equivalente a esta no arquivo de configurações.

```
$ cat .gitconfig

[user]
        name = Seu Nome
        email = seuemail@mail.com        
[commit]
        gpgsign = true
```

Definindo o programa padrão do GIT para GPG

```bash

git config --global gpg.program pgp

```

O comando ```git config --global gpg.program pgp``` configura o programa que o Git usará para operações GPG (GNU Privacy Guard) como "pgp".

Normalmente, o Git usa o programa GPG padrão instalado no seu sistema para lidar com operações de assinatura, criptografia, etc. No entanto, ao configurar gpg.program como "pgp", você está especificando um programa diferente para ser usado. Isso pode ser útil se você estiver usando um software de terceiros para lidar com operações GPG em vez do GPG padrão.

Por exemplo, se você estiver usando o PGP (Pretty Good Privacy) em vez do GPG, pode configurar o Git para usar o PGP com este comando.

A Saída agora deverá ser equivalente a essa.

```
 cat .gitconfig
[user]
        name = Seu Nome
        email = seuemail@mail.com
        fone = 9999999999
[commit]
        gpgsign = true
[gpg]
        program = pgp

```

### Gravando a KEY gerada no arquivo de configurações



  
#### Recursos Adicionais:
- Documentação oficial do GnuPG: [https://www.gnupg.org/documentation/](https://www.gnupg.org/documentation/)
- Tutoriais online e guias práticos sobre o uso do GnuPG.




