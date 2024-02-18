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
        fone = 9999999999
```

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
