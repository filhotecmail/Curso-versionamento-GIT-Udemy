# Aula 3: Realizando o Primeiro Commit

Nesta aula, vamos aprender sobre um dos conceitos fundamentais do versionamento de código: o commit. Entender o que é um commit, para que serve, como fazer e quais são os padrões e propriedades de um commit é essencial para qualquer desenvolvedor de software.

## O que é um Commit?

Um commit, em termos simples, é uma operação que registra as alterações feitas nos arquivos de um repositório Git. Ele captura um instantâneo do estado atual dos arquivos e os armazena no histórico do repositório, permitindo que você acompanhe as mudanças ao longo do tempo.

## Para que Serve um Commit?

Os commits desempenham um papel crucial no versionamento de código. Eles fornecem um registro detalhado de todas as alterações feitas no código ao longo do tempo, facilitando a colaboração entre membros da equipe, a reversão de alterações indesejadas e a rastreabilidade das mudanças.

Além disso, os commits ajudam a organizar o desenvolvimento do projeto em unidades lógicas de trabalho, tornando mais fácil entender e revisar as alterações feitas ao longo do tempo.

## Como Fazer um Commit?

Fazer um commit no Git é um processo simples e direto. Aqui está uma visão geral dos passos envolvidos:

1. **Adicionar as Alterações ao Índice**: Antes de fazer um commit, você precisa adicionar as alterações que deseja incluir ao índice do Git usando o comando `git add`.
   
2. **Criar o Commit**: Depois de adicionar as alterações ao índice, você pode criar o commit usando o comando `git commit`. Certifique-se de fornecer uma mensagem descritiva que explique as alterações feitas no commit.

3. **Assinar o Commit (Opcional)**: Se você estiver usando assinaturas GPG para garantir a integridade e autenticidade dos commits, o Git solicitará que você assine o commit usando sua chave GPG.

4. **Confirmar o Commit**: Após revisar a mensagem de commit e garantir que todas as alterações estejam incluídas conforme desejado, confirme o commit para torná-lo oficial.

## Padrões e Propriedades de um Commit

Alguns padrões e propriedades comuns de um commit incluem:

- **Mensagem Descritiva**: Uma mensagem de commit deve ser clara e descritiva, explicando as alterações feitas de forma sucinta e compreensível.
  
- **Unidade Lógica de Trabalho**: Um commit deve representar uma única unidade lógica de trabalho. Evite fazer commits que abranjam múltiplas alterações não relacionadas.

- **Convenção de Nomenclatura**: É comum seguir uma convenção de nomenclatura para as mensagens de commit, como usar um prefixo indicando o tipo de alteração (por exemplo, "feat" para novas funcionalidades, "fix" para correções de bugs).

- **Assinatura GPG (Opcional)**: Para garantir a integridade e autenticidade dos commits, você pode assiná-los usando sua chave GPG.

### Comando Commit com Assinatura GPG

Ao fazer um commit com assinatura GPG, você está adicionando uma camada extra de segurança aos seus commits, garantindo que eles sejam autenticados e não adulterados. Isso é especialmente útil em ambientes onde a integridade dos commits é crucial, como em projetos de código aberto ou em ambientes corporativos.

Para fazer um commit com assinatura GPG, você precisa configurar corretamente o Git com sua chave GPG e, em seguida, usar o parâmetro `-S` ou `--gpg-sign` ao fazer o commit. Isso instruirá o Git a assinar o commit usando sua chave GPG configurada.

### Exemplo de Comando Commit com Assinatura GPG em Markdown


```bash
 git commit -S -m "Mensagem do commit assinada com GPG"
 
 ```


**Neste exemplo:**

- `git commit:` Este é o comando principal para fazer um commit no Git.
- `-S ou --gpg-sign:` Este parâmetro instrui o Git a assinar o commit com GPG.
- `-m "Mensagem do commit assinada com GPG":` Este é o parâmetro que define a mensagem de commit. Certifique-se de substituir "Mensagem do commit assinada com GPG" pela sua mensagem de commit real.
Após executar este comando, o Git solicitará que você insira sua senha GPG (se necessário) e, em seguida, assinará o commit com sua chave GPG configurada.

Esse é o processo para fazer um commit com assinatura GPG no Git. Certifique-se de ter configurado sua chave GPG corretamente antes de usar este comando.