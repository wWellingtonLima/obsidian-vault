---
tags:
  - programming
  - glossary
links: "[[My Area]]"
---
---
## NVM - .nvmrc
## Arquivo de Manifesto - [[NodeJs]]
Dentre outras coisas, ele lista as dependências do projeto. O arquivo de manifesto usado em JS é o package.json e lista, por exemplo, as dependências que o projeto necessita para funcionar como o Next na versão X. 
Isso é útil para outra pessoa instalar as exatas mesmas versões das dependências ou **quando um servidor remoto fizer o build final das dependências** ele também usar as versões corretas.

## Versionamento de código centralizado
Num sistema centralizado existe uma cópia principal do repositório do código num servidor e as pessoas reservam os arquivos para dentro do seu computador, dessa forma, esses arquivos alugados ficam indisponíveis para as outras pessoas que estão trabalhando nesse projeto.
Todos os outros usuários ainda conseguem ver e ler os arquivos mas somente quem está usando-o consegue editar enquanto não for devolvido.
> É como se o repositório central fosse um Hotel e antes de os arquivos saírem dele é preciso que façam um **checkout**, 
> Isso era feito dessa forma para evitar a mescla, o **merge** de um arquivo alterado por duas pessoas diferentes sobre um mesmo arquivo.

## Blob - Binary Large Object


## URL - Uniform Resource Locator
É o endereço de outro computador ou "servidor" na internet. Parte da URL especifica onde encontrar o servidor e a outra parte fala para o servidor que informação eu quero.

> Uma URL representa um pedaço de informação em algum computador em algum lugar. É possível acessar isso fazendo um request e lendo a resposta que o servidor retornar.

Existem 8 partes principais em uma URL, não necessitando que todas estejam presentes ao mesmo tempo. Cada pedaço tem um papel responsável em ajudar os clientes a *encontrar os recursos que eles estão procurando*.
Um objeto de URL feito usando o construtor nativo do Javascript *new URL* pode conter as seguintes propriedades: protocol, username, password, hostname, port, pathname, search e hash.

![[Pasted image 20250520175423.png]]

>OBS: 
>**Apenas o Domínio e o Protocol são obrigatórios**
>A porta usada pelo protocolo HTTP tem como padrão a 80; já HTTPS, a 443.
>O path não é obrigatório mas basicamente sempre está lá uma vez que o padrão é o "/"

### Sobre URLs
* *Protocolo* - é o primeiro componente da URL. Ele **define as regras** cujos dados sendo comunicados devem ser mostrados, encodados ou formatados.
	* Diferentes URL protocolos são o Http, ftp, mailto, https.
* *Portas URL* - Uma porta URL é um **ponto virtual onde conexões de rede são feitas**. As portas são gerenciadas pelo sistema operacional do computador e podem existir simultaneamente até cerca de 65.535 portas. As portas servem para diferenciar os serviços que rodam num mesmo servidor tais como um serviço Web que está sendo oferecido por esse servidor ou, por exemplo, um banco de dados. Em produção normalmente são usadas as portas padrão, caso não seja, elas serão especificadas na URL. Uma porta pode ser usada unicamente por um program por vez, por isso existem tantas portas.
* *Query Parameters* - Com a URL de websites, os parâmetros de rota raramente mudam qual página estou vendo, mas sim alteram o conteúdo da página. Não é uma regra. Eles podem ser usados para qualquer coisa que o servidor decidir fazer com elas, assim como os caminhos de URL.

## URI - Uniform Resource Identifier
![[Pasted image 20250518194924.png]]

É uma sequência única de caracteres que identifica um recurso que é quase sempre acessado via internet. Assim como o Typescript tem suas regras de sintaxe,  URI também possui. Essas regras servem para garantir a regularidade para que qualquer programa possa interpretar o significado de uma URI da mesma forma.
A URI pode vir de dois principais jeitos:
Como URN ou URL.

---

# Arsenal de dicas / Usabilidade
## Como fazer Border Radius Invertido
[Vídeo YT](https://www.youtube.com/watch?v=2pZR-vfbcbo&list=WL&index=3&ab_channel=DevlyCode)