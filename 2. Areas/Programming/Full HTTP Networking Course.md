---
tags:
  - freecodecamp
  - http
links: "[[Protocolos HTTP]]"
---
---
# Why HTTP

## Básico
### Resumo 
- URLs não são específicas para o protocolo HTTP
- "http://" no começo de uma URL é usado para indicar para o servidor que o protocolo usado será o HTTP
- O nome de Domínio é apenas uma parte da URL. É a parte responsável por ser mapeada em um endereço IP.
- Existem 8 partes principais em uma URL, não necessitando que todas estejam presentes ao mesmo tempo. Cada pedaço tem um papel responsável em ajudar os clientes a *encontrar os recursos que eles estão procurando*.


---

O core do HTTP é simplesmente um *sistema de Request/Response*. 

O computador que faz o "Request" é chamado de **cliente** e pede determinada informação para outro computador, este agindo como **servidor**. Esse computador devolve uma "Response" com a informação que foi solicitada.

![[Pasted image 20250504185814.png]]

Ex: 
**Request**: Quais são os itens de um jogo de fantasia?
**Response**: Devolve a lista de itens pedidos do jogo.

*Existem outros protocolos para se comunicar pela internet* mas o HTTP é particularmente ótimo para sites e aplicações web. Portanto, quando eu acesso qualquer site, meu browser está fazendo um request HTTP para o servidor daquele site, que responde com todo o texto, imagens, e informações de estilo que o meu browser precisa para renderizar.

![[Pasted image 20250504190356.png]]

Por exemplo, o "http://" no começo de uma URL de algum website especifica que o protocolo HTTP vai ser usado para a comunicação pois outros protocolos também usam URLs.

Cliente e Servidor são apenas palavras usadas para descrever o que determinado computador está realizando em determinada comunicação. Um computador pode ser um cliente, servidor, os dois ou nenhum.
## [[_Glossário Programação#URL - Uniform Resource Locator|URL - Uniform Resource Locator]] 

# CRUD
É um acrônimo que representa Create, Read, Update e Delete.
Sempre que interajo com o servidor, basicamente, uma dessas ações provavelmente vai estar sendo utilizada, uma vez que o propósito primário dos métodos HTTP são o de ==indicar para o servidor o que queremos fazer com o recurso que estou tentando interagir==. #flashcard
<!--SR:!2025-06-16,2,232-->

Dessa forma, é possível mapear essas ações para [[Protocolos HTTP#HTTP Methods|HTTP Methods]] equivalentes como:

![[Pasted image 20250608075613.png]]
> No entanto, isso é uma *convenção*.

Portanto, o CRUD é ==uma convenção== usada para estabelecer normas em relação às ações que representam o acrônimo CRUD.  #flashcard
<!--SR:!2025-06-16,2,250-->


---
# Web Addresses
## IP

> Como o meu computador sabe onde encontrar outro computador conectado a vasta imensidão de dispositivos conectados?

Para isso existe o *IP - Internet Protocol* e sua anatomia é feita de 4 seções de números separados por um ponto.

Por exemplo: 8. 67. 210. 7 sendo que cada par é um número que vai de 0 a 255

Cada dispositivo conectado à internet possui um Endereço de IP único e é dessa forma que é possível encontrar e ser encontrado.

Esse formato é o mais comum e antigo chamado de IPv4.
Existe uma nova versão chamada de IPv6 com a diferença dele possibilitar uma combinação maior e portanto armazenar mais IP's do que o IPv4. 

Sua anatomia é feita substituindo o ponto pelos dois pontos, tendo 8 seções, ficando assim:
![[Pasted image 20250518190439.png]]

## DNS - Domain Name System

O nome de Domínio é apenas uma parte da URL. É a parte responsável por ser convertida em um IP para contactar um determinado serviço Web.

O DNS funciona como um tradutor que converte o resultado da pesquisa feita por um usuário, por exemplo, em um IP relacionado ao nome digitado. 

Se eu quiser acessar algum serviço da Amazon eu digito Amazon.com e não o endereço IP relacionado a isso. 

Quando eu faço uma pesquisa a primeira parte que os computadores fazem por baixo dos panos é primeiramente *resolver o nome de domínio* buscado em um endereço de IP. Isso também vem com outra vantagem: se a Amazon por algum motivo *trocar o IP*, o nome de domínio não vai ser alterado mas precisa apenas mudar o apontamento para o endereço de IP novo.

> *Resumindo*: a primeira etapa de uma busca é Resolver o nome de Domínio e obter um IP, a segunda é de fato usar esse IP como endereço para fazer esse request para o servidor.

### O "Sistema" de Domain Name System

O DNS é o sistema e age como o dicionário. As pessoas digitam "nomes de domínio fáceis de ler" igual amazon.com e *o DNS "resolve" esses nomes de domínios em seus respectivos endereços de IP* para que os clientes web possam encontrar os servidores que buscam.
Nomes de Domínio são para humanos; IP para os computadores.

![[lvjZb5u.png]]

### Subdomínios

Subdomínios são basicamente meios de repartir um domínio em recursos sem que necessariamente seja preciso comprar outro nome de domínio.

Por exemplo, um *blog*.boot.dev é o domínio associado ao blog dessa página, enquanto o *api*.boot.dev é o serviço backend e o boot.dev é o website.

---

# [[_Glossário Programação#URI - Uniform Resource Identifier|URI - Uniform Resource Identifier]]
> Ver link acima

## [[_Glossário Programação#URL - Uniform Resource Locator|URL - Uniform Resource Locator]]
> Ver link acima sobre URL


---
# Status Code vs Errors
De um lado tenho uma **requisição HTTP sendo mandada pelo cliente**, se algo acontecer nesse momento, é produzido um *erro*. Exemplos disso são: um nome de domínio inválido para a fetch API ou se a internet cair e não for possível continuar o request. No entanto, se algo acontecer de errado no servidor, logo, se o request chegar com sucesso ao servidor e agora é o servidor que está processando o request, **se algo acontecer durante o processamento do request** isso resultará em um *Status Code* e mesmo assim um HTTP response vai ser enviado novamente e o status code vai ser dentro da response. Exemplos disso são: ==sem permissão para acessar o conteúdo== ou ==se algum dos serviços de backend estiver desligado== #flashcard #Relembrar
<!--SR:!2025-06-16,2,162!2025-06-16,2,162-->

 ## Status Codes
 Se tratando de requests é possível olhar os seus Status Code para saber se ele foi bem sucedido ou não.
 Os tipos de erro são:
 - 100-199: **Informational responses**. São um pouco raros.
 - 200-299: Response bem sucedido.
 - 300-399: **Redirection messages**. Normalmente esses são invisíveis porque o browser ou o cliente HTTP vai automaticamente fazer o redirecionamento.
 - 400-499: **Client errors**. Acontece normalmente quando tentando debugar alguma client application.
 - 500-599: **Erros do servidor**.
 ==.== #flashcard
<!--SR:!2025-06-16,2,182-->
### Mais comuns Status Code
- 200 - OK
- 201 - *Created*. Significa que o conteúdo foi criado com sucesso. Esse Code normalmente vem numa resposta de um request POST.
- 301 - *Movido permanentemente*. Significa que o recurso foi movido para um novo local e que a resposta inclui qual é esse novo local. Os websites normalmente usam o redirecionamento do código 301 quando o seu nome de domínio é alterado, por exemplo.
- 400 - *Bad request*. Um erro geral indicando que existe algum erro do lado do request do cliente.
- 403 - *Unauthorized*. Significa que o cliente não possui as permissões adequadas para acessar o recurso requisitado.
- 404 - *Not found*. Significa que o recurso não existe.
- 500 - *Internal Server Error*. Algo deu errado do lado do servidor.


---
# Links
* [[Protocolos HTTP]]
* [[_Glossário Programação]]



