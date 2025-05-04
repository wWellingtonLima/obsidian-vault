---
tags:
  - git
  - github
links: "[[My Area]]"
---
---
# O básico de Git

O Git é um sistema de versionamento de código criado por Linus Torvalds em 2005.

## Funcionamento

O Git **Não armazena** apenas o diff entre cada commit como sistemas mais antigos como o CVS que armazena apenas o diff (Delta) entre os commits, apesar de isso ocupar menos espaço, para ter uma [versão atual do arquivo] é preciso reprocessar todo o histórico dele.


![[Pasted image 20250503201856.png]]
Cada foto que eu tiro do meu repositório é um commit do repositório inteiro mesmo.
O git vai pegar cada arquivo do meu projeto e pegar cada coisa de como ele foi deixado, colocar um identificador e salvar isso na pasta oculta do .git. O Nome desse pacotinho com identificador e o conteúdo do arquivo é chamado de [[_Glossário Programação#Blob - Binary Large Object|Blob - Binary Large Object]] 

![[Pasted image 20250503202045.png]]

Quanto eu altero um arquivo e tiro mais uma foto desse repositório o git não descarta nem modifica o Blob anterior que representava o conteúdo desse arquivo. Ele mantém esse blob de forma imutável e o mantém para histórico. 
Ele então cria um novo blob contendo o conteúdo inteiro da nova versão desse arquivo e a foto mais atual aponta para esse novo blob. Caso outro arquivo não tenha sido modificado, o git não cria novamente o arquivo, mas sim aponta para o blob anterior. 

![[Pasted image 20250503202635.png]]
> Cada commit é apenas uma série de apontamentos para Blobs existentes.


# Mais avançado sobre Git


---
# Comandos Git
* 

---
### Links
* 
