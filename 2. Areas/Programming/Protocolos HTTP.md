---
tags:
  - http
  - protocols
links: "[[My Area]]"
---
---
# O que é um protocolo

Existem diversos protocolos cada um com seu objetivo.
Um protocolo é simplesmente um acordo, um combinado e conjunto de regras conhecidas entre as duas partes que estão tentando se comunicar e, portanto, define por exemplo como uma conversa deve se iniciar, em que lugar eu quero que seja preenchida determinado tipo de informação; quando a informação volta, como exatamente ela vai voltar, como começa, como termina.

Os protocolos podem ser sobrepostos como:
> O HTTP, que define como informações Web vão ser trocadas entre cliente e servidor, que podem ser transmitida pelo protocolo TCP, este garante que as informações vão chegar do outro lado e que para transitar, de fato, é usado o protocolo IP.
> Em cima do IP não preciso necessariamente usar o TCP pois a garantia de que as informações cheguem completamente em ambos os lados tem o [custo] de deixar a transmissão mais devagar. Existem casos onde é necessário pagar por esse custo e casos que não.
> Para casos onde custo de ser mais lento não vale a pena existe o UDP.



---
# Protocolos
## HTTP

**Hypertext Transfer Protocol** - O Hypertext é um documento que possui referências para outros documentos. É um protocolo que define regras para a transferência desses documentos.

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
