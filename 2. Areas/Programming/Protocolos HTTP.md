---
tags:
  - http
  - protocols
links: "[[Full HTTP Networking Course]]"
---
---
# O que é um protocolo

Existem diversos protocolos cada um com seu objetivo.

Quando dois computadores estão tentando se comunicar entre si, eles precisam **usar a mesma língua**. Um falante de Inglês não consegue se comunicar verbalmente com um falante de Japonês, logo, é a mesma coisa quando dois computadores precisam se comunicar.

Um protocolo é simplesmente um acordo, um *combinado e conjunto de regras* conhecidas entre as duas partes que estão tentando se comunicar e, portanto, define por exemplo como uma conversa deve se iniciar, em que lugar eu quero que seja preenchida determinado tipo de informação; e, quando a informação volta, como exatamente ela vai voltar, como começa, como termina etc.

Os protocolos podem ser sobrepostos como:
> O HTTP, que define como informações Web vão ser trocadas entre cliente e servidor, que podem ser transmitida pelo protocolo TCP, este garante que as informações vão chegar do outro lado e que para transitar, de fato, é usado o protocolo IP.
> Em cima do IP não preciso necessariamente usar o TCP pois a garantia de que as informações cheguem completamente em ambos os lados tem o [custo] de deixar a transmissão mais devagar. Existem casos onde é necessário pagar por esse custo e casos que não.
> Para casos onde custo de ser mais lento não vale a pena existe o UDP.

# HTTP Headers

Os Headers de HTTP permitem que clientes e servidores passem informações adicionais entre cada request ou cada response. 

> Headers são apenas pares de chave-valor case-insensitive que passam metadados adicionais sobre o request ou response. 

Requests feitos por um browser web automaticamente possuem vários headers, mas não se limitando a:
	O tipo de cliente, o sistema operacional e a linguagem do sistema.

Os desenvolvedores podem definir headers customizados em cada request.

# HTTP Methods

O HTTP estabelece diversos métodos que são usados sempre que é feito um request. 
 - **GET**: Esse método é considerado seguro pois ele 'solicita' uma representação de algum recurso requisitado. Usando-o eu não estou pegando os dados do servidor mas sim solicitando a representação ou uma cópia dos recursos no seu estado atual.
 
```js
await fetch(url, {
	method: "GET",
	mode: "cors",
	headers: {
		'sec-ch-ua-platform': "macOS"
	}
})
```
Em um request usando GET não incluo o body nesse objeto da fetch porque estou solicitando os dados e não vou alterar nada.

- **POST**: esse método manda dados para o servidor, normalmente criando um novo recurso. O *body* do request é o payload que está sendo mandado para o servidor através do request, normalmente indicado pelo header =="Content-Type"==. Nem todo servidor vai requisitar mas é uma boa prática indicar o tipo de dado que está sendo mandado para o servidor. #flashcard
<!--SR:!2025-06-25,11,270-->

- **PUT:** é bem parecido com os métodos POST e o PATCH. O POST é usado exclusivamente para criar algo enquanto o PUT é *usado para atualizar ou criar ou apenas atualizar* 

---
# Protocolos
## HTTP

**Hypertext Transfer Protocol** - O Hypertext é um documento que possui referências para outros documentos. É um protocolo que define regras para a transferência desses documentos.
O protocolo HTTP é o mais famoso para comunicação online pela internet, apesar de existirem outros.

## TCP

**Transfer Control Protocol** - 
Esse protocolo possui um sistema chamado de [Error Recovery] para caso um pacote de informação não chegar na outra ponta, ele requisitar novamente até que ambos os lados tenham a certeza que a informação foi transmitida com integridade.

## IP 
**Internet Protocol**

## UDP
**User Datagram Protocol** - 
Em caso de uma transmissão / videochamada usando esse protocolo caso um pedaço da transmissão seja perdido, os próprios envolvidos basicamente [servem como se fosse o TCP], ou seja, um lado fala "Não entendi, repete." e o outro lado vai repetir a informação até que ambos estejam na mesma página.

(Datagram é como se fosse um pedaço de informação autocontido - Cada pacote é autossuficiente e não depende de uma negociação ou conferência dos dados)

## FTP

**File Transfer Protocol** - Protocolo mais dedicado à transferência de arquivos.

## SMTP
**Simple Mail Transfer Protocol** - Um dos padrões usados para a transferência de email.




---
### Links
* 
