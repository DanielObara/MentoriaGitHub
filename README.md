# Mentoria sobre GitHub

## Resumidão (clone até atualizar remoto)
Se você já sabe executar todo o fluxo e só quer relembrar, deixo abaixo o fluxo (básico e sem criação de branch) resumido mas se voce quiser saber detalhadamente recomendo prosseguir a leitura.

```bash
# Clone o repositório
$ git clone https://github.com/DanielObara/MentoriaGitHub
# Modifique algo e adicione ao stage
$ git add .
# Commite com a mensagem do que fez, siga o commitlint!
$ git commit -m "feat(lang): add portuguese language"
# Suba suas alterações
$ git push
```

## Criando um novo repositório:
Crie uma nova pasta, abra-a e no terminal execute o comando

```bash
$ git init
```
## Clonando um repositório:
Crie uma cópia de trabalho em um repositório local executando o comando:

```bash
$ git clone /caminho/para/o/repositório
```
Quando usar um servidor remoto, por exemplo o GitHub, seu comando será:

```bash
$ git clone https://github.com/DanielObara/MentoriaGitHub
```
O endereço do servidor remoto (repositório) e o link que você pode pegar clicando no botão code.

Para acessar o projeto recém clonado, acesse a pasta do projeto e caso tenha acessado via terminal digite `code .`,
se não clique com o botão direito dentro da pasta e veja se tem a opção de abrir no VSCode.

## Atualizando o repositório remoto:

Seus repositórios locais consistem em três "árvores" mantidas pelo git. A primeira delas é sua Working Directory que contém os arquivos atuais, a segunda Index / Stage que funciona como uma área temporária e finalmente a HEAD que aponta para o último commit (confirmação) que você fez.

<p align="center">
  <img src="https://user-images.githubusercontent.com/42970570/133843768-083e637d-5004-4582-8d45-eb1cf7263a0e.png" alt="Imagem demonstrando as três arvores (uma pasta que é o diretório de trabalho seguida de uma estrutura que é a index / stage e depois a estrutura concretizada que se torna a head)" ></img>
</p>

## Adicionar & Confirmar

Você pode propor mudanças (adicioná-las ao Index) usando:
Para adicionar um arquivo em particular

```bash
$ git add caminho/até/o/arquivo
```
ou para adicionar todas as alterações:

```bash
$ git add .

# ou pode-se usar *

$ git add *
```
Este é o primeiro passo no fluxo de atualizar o repositorio de forma básica do git. 

Para realmente confirmar estas mudanças (isto é, fazer um commit), use:

```bash
$ git commit -m "Mensagem dizendo o que eu fiz nessas alterações"
```
**Obs: recomendo seguir a convenção de commit conhecida como conventional changelog ou [commitlint](https://github.com/conventional-changelog/commitlint)

Agora o arquivo é enviado para o HEAD, mas ainda não foi enviado para o repositório remoto (aquele lá nos servidores/nuvem do Github).

## Enviando as alterações:
Lembre-se que suas alterações agora estão no HEAD da sua cópia do repositório local. 
Para enviar estas alterações ao seu repositório remoto, execute

```bash
$ git push origin main
```

Altere main para qualquer ramo (branch) desejado, enviando suas alterações para branch específica. Caso não especifique qual branch, o git entenderá por padrão a branch atual que você estiver.

Se você não clonou de um repositório que já existe e quer conectar seu repositório a um no servidor remoto (GitHub por exemplo), você deve adicioná-lo com

```bash
$ git remote add origin <servidor>
```

Ficaria assim:
  
```bash
$ git remote add origin git@github.com:DanielObara/MentoriaGitHub.git
```

Agora você é capaz de enviar suas alterações para o servidor remoto selecionado.

## Qual a situação atual?
Para verificar o que foi feito e qual a situação (Se está atualizado ou se tem modificações)

```bash
git status

```
