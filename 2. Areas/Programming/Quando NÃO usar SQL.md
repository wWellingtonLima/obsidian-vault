---
tags:
  - SQL
  - DB
links: "[[My Area]]"
---
---

## Existem alguns problemas ao usar SQL, alguns deles são:
### Impedance Mismatch

Isso acontece quando uma determinado conjunto de informações precisa de várias tabelas para ser armazenado, enquanto poderia ser facilmente armazenado em um objeto.

Ex: Informações de compra de um cliente, os dados são ID, o nome do cliente, os itens que ele comprou  e os detalhes do pagamento. Cada uma dessa informações precisaria de uma tabela específica para ser armazenado.

![[Pasted image 20250501073918.png]]

### ACID

Os princípios ACID são um conjunto de propriedades que garante que as transações em um bando de dados SQL (e outros bancos relacionais) sejam feitas de forma confiável.

* **Atomicity** - Significa que todas as transições são executadas ou nenhuma é executada. Uma transação deve ser executada completamente ou não ser executada. Se algo falhar no meio, o banco de dados reverte tudo que já foi feito na transação.
	* Transferência de dinheiro entre contas: se o débito da conta A acontecer, o crédito na conta B também tem que acontecer. Se uma dessas operações falhar, nenhuma delas deve ser aplicada.
* **Consistency** - O banco de dados deve sempre passar de um estado válido para outro estado válido. A transação deve manter as regras e restrições do banco (como chaves primárias, tipos de dados, restrições de integridade, etc) 
	* Se há uma regra dizendo que o saldo de uma conta não pode ser negativo, nenhuma transação pode deixar esse valor negativo, mesmo que algo quebre no meio.
* **Isolation** - As transações devem ser independentes entre si. Mesmo que várias transações ocorram ao mesmo tempo, elas não devem interferir umas nas outras. O resultado deve ser como se cada uma tivesse sido executada separadamente.
	* Duas pessoas tentando comprar o último ingresso ao mesmo tempo. O banco precisa isolar essas ações para que só uma consiga.
* **Durability** - Uma vez que uma transação é confirmada, seus dados não devem ser perdidos. Mesmo que haja falha de energia, pane no servidor ou queda do sistema, os dados continuam salvos lá.
	* Se eu fizer uma compra e o banco confirmou a transação, ela não vai sumir mesmo se o servidor cair logo depois.


---

### Notes / Links
* [[SQL]]
* 