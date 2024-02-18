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
