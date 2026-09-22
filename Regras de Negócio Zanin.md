* Regras de Negócio : Um **CLIENTE** pode estar registrado sem fazer um **PEDIDO** , e um **CLIENTE** pode fazer vários pedidos . Um **PEDIDO** tem que possuir obrigatoriamente um **CLIENTE.**


RN01 (Relacionamento Cliente-Pedido): Um CLIENTE pode estar cadastrado no sistema sem realizar nenhum pedido, mas um pedido deve pertencer obrigatoriamente a um único CLIENTE registrado.


RN02 (Cardinalidade): Um cliente pode realizar zero ou vários pedidos ($0, N$), enquanto cada pedido está associado obrigatoriamente a um (e apenas um) cliente (1, 1). 


RN03 (Composição do Endereço): O endereço do cliente é composto obrigatoriamente por logradouro, cep, número e pode conter um complemento opcional.



RN04 (Identificação Única): Cada CLIENTE deve ser identificado de forma única por seu id\_cliente, e cada PEDIDO por seu numero\_pedido.



* Requisitos Funcionais: 



RF01 - Cadastro de Clientes: O sistema deve permitir o cadastro de novos clientes, armazenando id\_cliente, nome, telefone e os dados detalhados de endereco (logradouro, cep, número e complemento).



RF02 - Consulta e Atualização de Clientes: O sistema deve permitir consultar, alterar e excluir os dados cadastrais dos clientes. 



RF03 - Registro de Pedidos: O sistema deve permitir registrar novos pedidos vinculados a um cliente existente, informando o numero\_pedido e a quantidade\_itens.



RF04 - Associação de Pedido a Cliente: O sistema deve garantir que todo pedido criado esteja obrigatoriamente associado a um cliente válido.



RF05 - Listagem de Pedidos por Cliente: O sistema deve permitir visualizar todos os pedidos realizados por um determinado cliente.   



* Requisitos não Funcionais: 



RNF01 - Banco de Dados Relacional: O sistema deve utilizar um SGBD relacional (como MySQL, PostgreSQL, etc.) para persistir as entidades CLIENTE e PEDIDO com suas respectivas restrições de integridade referencial.



RNF02 - Integridade de Dados: O sistema deve garantir a atomicidade e consistência das transações, assegurando que nenhum pedido fique órfão (sem cliente associado).



RNF03 - Desempenho: As consultas de busca por id\_cliente e numero\_pedido devem retornar resultados em tempo inferior a 2 segundos.



RNF04 - Segurança e Acesso: O acesso ao cadastro de clientes e ao registro de pedidos deve ser restrito a usuários autenticados no sistema.

