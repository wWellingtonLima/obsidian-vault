---
tags:
  - responsive
  - css
  - tailwind
links: "[[My Area]]"
---
---
# 5 Medidas para tornar a estilização mais responsiva
## **Relative padding**
### Problema

Em grandes telas usar o padding normal como *5em* funciona bem mas em telas menores não funciona.
### Alternativa básica de resolução

Usar Media Queries e, ao chegar em determinada largura, diminuir o padding usado.
Isso pode ser usado, claro, mas existe uma forma melhor.
### Resolvendo usar unidade relativa e a função min() do CSS

Ela aceita dois argumentos e calcula qual deles é menor e aplica isso para a propriedade onde foi usada.

Por exemplo: Tenho uma classe container na tag 'main' e o pai desse elemento é o 'body', ao 
adicionar um padding de min(5em, 8%) ele vai **calcular qual desses valores é o menor** , quando a tela tiver em desktop os 5em vão ser menores do que os 8% do tamanho total da tela (comparando com o elemento pai), mas quando eu começar a diminuir, em algum momento os 8% do padding vão ser menores do que os 5em então esse valor vai ser aplicado e, **como o % é uma unidade relativa, ele vai continuar a diminuir enquanto a tela estiver sendo diminuída**. 

---
## **Responsive Font-sizes**
### Problema

Não usar px em fontes e sim o REM.
O REM é o tamanho de fonte relativo à raiz do meu elemento mas pode dar problema em grandes Headings

### Usando a unidade vw

Essa propriedade escala o tamanho de fonte relativo à view-port **mas deve ser usada com cuidado**. Em grandes telas o 10vw pode ser muito grande e em um celular 10vw fica pequeno.

### Resolvendo usar unidade relativa e a função min() do CSS




---

## **Responsive Font-sizes**
### Problema


### Alternativa básica de resolução


### Resolvendo usar unidade relativa e a função min() do CSS




---
### Links
* https://www.youtube.com/watch?v=2IV08sP9m3U&ab_channel=Coding2GO
* 