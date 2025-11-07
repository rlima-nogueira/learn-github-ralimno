# Módulo 2: Working with GitHub Repositories

Finalizamos as aulas do Módulo 2 e agora é hora de colocar em prática!

A atividade a seguir visa consolidar o conhecimento apresentado na aula, abordando os seguintes tópicos:

- Criação de repositório
- Adição de arquivos
- Adição de branch
- Clone de repositório

Vale ressaltar que o aspecto mais importante da atividade é a fixação dos conceitos envolvidos, portanto, busque tomar notas durante a prática e conectar os pontos dessa aula com as aulas anteriores e as seguintes.

Parabéns pela dedicação e bons estudos!

## 1. Criando Repositório

### Requisitos:
- Conta GitHub

### Procedimento:

1. Acesse [github.com](https://github.com/) no seu navegador e faça login em sua conta (clique no botão "Sign In" localizado no canto superior direito)
2. Clique no botão sinalizado com "+", posicionado na parte superior da tela e selecione "New Repository"

![Figura 1 - Captura de tela da página inicial do GitHub.](https://files.cdn.thinkific.com/file_uploads/401289/images/386/f3a/fdb/1744662312699.png)

3. Na página recém aberta, configure as seguintes informações:
   - Repository Owner
   - Repository Name (sugestão: learn-github-SeuNome)
   - Description
   - Defina a visibilidade do repositório: público ou privado

![Figura 2 - Captura de tela indicando os campos a serem configurados nesse passo.](https://files.cdn.thinkific.com/file_uploads/401289/images/e63/8c0/20b/1744657161735.png)

> **Observação:** Repare que na Figura 2 não existe a opção "Internal", isso ocorre pois tal opção está disponível apenas nas contas Enterprise. No exemplo usado, o GitHub não era Enterprise.

4. Avançando na página temos a seção "Initialize this repository with", nela, trabalhamos itens como os arquivos README e .gitignore e o licenciamento. Nessa etapa:
   1. Marque a caixa de seleção "Add a README file"
   2. Selecione a opção "None" na lista suspensa de GitIgnore
   3. Selecione a opção MIT License na lista suspensa de licenças

![Figura 3 - Captura de tela com as informações do passo 4](https://files.cdn.thinkific.com/file_uploads/401289/images/bd7/b13/7c4/1744657161838.png)

5. Clique em "Create Repository"

Pronto, o novo repositório foi criado!

Perceba que até essa etapa temos 2 arquivos no nosso repositório, são eles LICENSE e README.md, ambos localizados no ramo (branch) "main".

## 2. Adicionando arquivos

Nesta etapa, adicionaremos novos arquivos, para isso abordaremos de duas maneiras distintas: através da interface e via linha de comando.

### 2.1 Adicionando arquivos através da interface

1. Ainda no seu navegador (tela do repositório criado), clique no botão sinalizado com "+" ou "Add file", posicionado na parte central da tela e selecione "Upload Files"

> **Informação:** Caso você não esteja na página do seu repositório, você poderá acessá-la através da url no seguinte padrão:
> 
> `github.com/<proprietario>/<nomeRepositorio>`
> 
> Ou acesse github.com, e busque pelo nome do seu repositório no campo de buscas denominado "Find a repository"

![Figura 4 - Captura de tela sinalizando os cliques necessários](https://files.cdn.thinkific.com/file_uploads/401289/images/df4/bb8/cf6/1744657161920.png)

2. Na tela que for apresentada, arraste arquivos para a região mostrada ou clique no botão "Choose your files" para buscar arquivos através do explorador de arquivos do Windows. Adicione um arquivo.

![Figura 5 - Captura da tela para upload de arquivos](https://files.cdn.thinkific.com/file_uploads/401289/images/6f5/f75/d9d/1744657162010.png)

3. Na sequência, adicione informações pertinentes na seção "Commit Changes", nos campos abaixo:
   1. Resumo de commit
   2. Descrição extendida de commit

![Figura 6 - Captura de tela de upload](https://files.cdn.thinkific.com/file_uploads/401289/images/c72/3f2/c02/1744657162140.png)

4. Abaixo dos campos, devemos escolher se o commit será direto na branch "main" ou se haverá a criação de uma nova branch para esse commit. Escolha pela criação de uma nova branch e dê um nome adequado (informações sobre o passo 4 na Figura 6)

> **Observação:** Essa ação, além de criar uma nova branch com o arquivo selecionado, criará também um pull request, não abordaremos em detalhes qual o impacto da criação de um pull request. Por ora, vamos focar apenas que estamos adicionando um arquivo e criando uma nova branch ao mesmo tempo no nosso repositório

5. A tela que temos agora é de abertura de um pull request. Adicione um título e uma descrição

![Figura 7 - Captura de tela mostrando os campos para criação do pull request](https://files.cdn.thinkific.com/file_uploads/401289/images/864/d51/3e1/1744657162240.png)

6. Clique no botão "Create pull request", localizado logo abaixo da descrição e a direita

Pronto, ao término desses passos temos:

- 1 novo arquivo adicionado
- 1 nova branch
- 1 pull request

Alternativamente, é possível criar uma nova branch separadamente e inserir arquivos diretamente nela, sem gerar um pull request.

Explore essa possibilidade, acesse a página inicial, clique no link de branches, crie uma nova branch e adicione arquivos diretamente na branch (o procedimento é similar ao que já vimos nos passos acima).

### 2.2 Adicionando arquivos através de linhas de comando

#### Requisitos:
- Um repositório criado no github.com
- Software Git Bash já está instalado

> **Observação:** Substitua os termos entre "<>" que estarão presentes nas instruções abaixo pelas informações do seu repositório.

> Diversas vezes vamos nos referir a `<proprietario>` e `<nomeRepositorio>`, essas informações podem ser obtidas na url do seu repositório, conforme imagem abaixo:

![Figura 8 - Captura da tela mostrando a url da página do repositório](https://files.cdn.thinkific.com/file_uploads/401289/images/2f6/4c9/fc3/1744657162358.png)

> Exemplo:
> - Proprietário: jovisisa
> - Nome do repositório remoto (GitHub): gh4w

#### 2.2.1 Clone de repositório

Nesta etapa, clonaremos um repositório. A essência da clonagem de repositório é capturar um repositório remoto (criado no GitHub.com) e replicá-lo localmente. Ou seja, teremos um repositório git local igual ao existente remotamente, sendo esse repositório sua propriedade ou de outra pessoa.

**Procedimento:**

1. Crie uma nova pasta em "Documentos", essa será nossa pasta do repositório local git.
   a. Abra o explorador de arquivos do Windows
   b. Clique em "Documentos"

![Figura 9 - Explorador de arquivos com a pasta Documentos selecionada](https://files.cdn.thinkific.com/file_uploads/401289/images/3ec/520/9d9/1744657162478.png)

2. Crie uma nova pasta com o nome gh4w (botão direito do mouse, selecione new e depois Folder)

![Figura 10 - Tela do Explorador de arquivo windows com setas apontando para New e depois Folder para criação de uma pasta](https://files.cdn.thinkific.com/file_uploads/401289/images/4d4/285/1bb/1744657162588.png)

3. Acesse a pasta e copie seu endereço

![Figura 11 - Passos para captura do endereço da pasta](https://files.cdn.thinkific.com/file_uploads/401289/images/248/f5d/b2f/1744657162675.png)

4. Abra o Git Bash.
   a. Depois da instalação, vá até o menu iniciar e busque por Git Bash
   b. Selecione Git Bash na lista de resultados, conforme figura abaixo:

![Figura 12- Captura de tela mostrando os passos para abrir o Git Bash](https://files.cdn.thinkific.com/file_uploads/401289/images/0b3/152/74e/1744657162799.png)

A tela que abrirá será semelhante a Figura 13, a seguir, mas o conteúdo em verde serão as informações relativas à sua própria maquina:

![Figura 13 - Tela inicial do Git Bash](https://files.cdn.thinkific.com/file_uploads/401289/images/22e/ef2/d76/1744657162899.png)

5. Com o terminal aberto, execute o comando a seguir para acessar a pasta criada anteriormente. Vide Figura 14

```bash
cd "<enderecoPasta>"
```

> **Dica:** O endereço da pasta estará na área de transferência, pois foi copiado no passo 2. Então basta digitar cd e abrir aspas duplas, control+v e fechar aspas duplas

![Figura 14 - Captura de tela do terminal](https://files.cdn.thinkific.com/file_uploads/401289/images/0da/856/f64/1744657163009.png)

6. Acesse github.com no seu navegador e vá até a página do seu repositório

7. Localize o botão "Code" e copie o link HTTPS

![Figura 15 - Captura de tela do repositório demonstrando onde está localizado o link a ser copiado](https://files.cdn.thinkific.com/file_uploads/401289/images/842/b9b/85e/1744657163109.png)

8. Execute o comando:

```bash
git clone <linkCopiado>
```

> **Dica:** O link copiado já está na área de transferência, digite o comando git clone, depois control + v e depois enter

![Figura 16- Comando git clone executado](https://files.cdn.thinkific.com/file_uploads/401289/images/cea/94b/d29/1744657163194.png)

Pronto, temos o clone do nosso repositório do GitHub em um repositório local.

A pasta que criamos no passo 1 agora deve conter uma pasta, que é o nosso repositório clonado, contendo todos os arquivos do nosso repositório remoto.

![Figura 17 - Pasta local com o clone feito](https://files.cdn.thinkific.com/file_uploads/401289/images/10f/8d3/f9e/1744657163284.png)

#### 2.2.2 Adicionando arquivo através de linha de comando

**Procedimento:**

1. Voltando ao terminal, execute o comando: `cd <nomeRepositorio>`

> **Informação:** O comando acima nos levará até nosso repositório git local, que é o nosso repositório clonado. Perceba que o terminal indicará que agora estamos no nosso repositório e na branch "main"

2. Como boa prática, não devemos fazer alterações direto na "main", execute o comando a seguir para criar uma nova branch: `git checkout -b <nomeBranchNova>`

> **Informação:** O comando acima realiza a criação da nova branch e já nos coloca nessa nova branch, ou seja, as alterações feitas nos passos seguintes estarão nesse escopo.

![Figura 18 - Print do git bash com a execução do comando git checkout -b BranchExemplo](https://files.cdn.thinkific.com/file_uploads/401289/images/6a5/610/14b/1744657163380.png)

3. Agora execute o comando: `touch <nomeDoArquivo>`

> **Informação:** Como exemplo, o nome do arquivo será "meu_novo_arquivo.txt". Esse comando adicionará esse arquivo (que é um .txt vazio) ao meu repositório na branch "BranchExemplo"

4. Agora execute o comando: `git add .`

> **Informação:** Utilizando o "." aplicaremos o comando add a todos os arquivos da pasta, para selecionar arquivos específicos basta substituir o "." pelo nome dos arquivos com suas extensões, exemplo: git add arquivo1.txt arquivo2.js

![Figura 19 - Comando git add](https://files.cdn.thinkific.com/file_uploads/401289/images/d21/ea5/436/1744657163465.png)

5. Em seguida, execute o comando: `git commit -m "<Descrição>"`

> **Informação:** Esse comando "comita" a alteração feita no repositório local, no nosso caso, a adição de 1 arquivo através do comando do passo 4 com o git add.

> Perceba que o Git Bash detectará as alterações feitas e apontará que houve um arquivo alterado, ou seja, o arquivo que criamos na pasta no passo 3

![Figura 20 - Comando git commit](https://files.cdn.thinkific.com/file_uploads/401289/images/430/09d/660/1744657163596.png)

6. Na sequência, execute o comando: `git push --set-upstream origin <nomeBranchNova>`

> **Informação:** O comando acima enviará nossa branch criada localmente para o repositório remoto (GitHub). Ou seja, nossa branch estará disponível no GitHub.

> **Dica:** Utilizando o git push --set-upstream origin, seguido do nome da branch, configuramos a upstream da nossa branch, ou seja, ela será rastreada remotamente. Isso nos permitirá fazer envios posteriores com apenas git push (sem argumentos adicionais), pois o git já saberá para onde mandar essas alterações

Pronto! Temos um novo arquivo adicionado ao nosso repositório através da linha de comando, assim como uma nova branch para organizarmos nossas alterações.