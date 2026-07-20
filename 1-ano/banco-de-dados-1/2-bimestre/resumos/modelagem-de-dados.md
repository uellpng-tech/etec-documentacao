## Oque é Modelagem de Dados?

A modelagem de dados é o planejamento da organização do banco de dados. A modelagem de dados usa de artificios visuais para planejar a organização da estrutura do banco de dados, geralmente ela é usada para pré-definir um banco de dados com base na necessidade de uma empresa ou individuo, para o planejamento do banco de dados usamos nomenclaturas para definir cada tipo de dado. A modelagem de dados segue três etapas que seguem a abstração:

- Modelo Conceitual: É o rascunho do negócio, ele usa caixas e setas para mostrar oque o negócio precisa e suas necessidades, é feito para conversar com o cliente ou o dono da empresa de forma mais simplificada.

- Modelo Lógico: Aqui definimos o nome das tabelas, as colunas, os tipos de dados (texto, número, data) e quem se conecta com quem. É o modelo mais intermédiario.

- Modelo Físico: É a transformação do desenho para o código SQL puro (comando como CREATE TABLE). Ele é totalmente dependente do SGBD escolhido (MySQL, PostgreSQL, etc.) e dita como o computador vai salvar as informações.

## Diagrama de Entidade e Relacionamento (DER)

O DER mapeia as entidades, seus atributos e como se relacionam. O Diagrama de Entidade e Relacionamento é a representação visual do MER (Modelo de Entidade e Relacionamento), a função do DER é mapear as entidades (coisas e conceitos), seus atributos (características) e como se relacionam. O DER possui alguns componentes principais:

- Entidade: Representam objetos, pessoas ou conceitos do mundo real (ex: Cliente, Produto).

- Atributos: São as informações detalhadas de cada entidade (ex: CPF do cliente, Preço do produto).

- Relacionamentos: Mostram como as entidades interagem entre si podendo ser do tipo um-para-um, um-para-muitos ou muitos-para-muitos.

## Tipos de Atributos

No DER os atributos não são todos iguais. Os atributos possuem classificações específicas que ditam como a informação será dividida e armazenada:

- Aributo Simples (ou Atômico): É aquele que possui valor único e não precisa ser dividido (ex: Idade, Preço).

- Atributo Composto: É um atributo que pode ser dividido em partes menores (ex: Endereço, que se divide em Rua, Número, Bairro e CEP).

- Atributos Multivalorado: É um atributo que pode guardar mais de um valor para o mesmo registro (ex: Telefone, onde o cliente pode ter vários). No modelo Lógico, atributos multivalorados viram uma nova tabela.

- Atributo Derivado: É um atributo cujo valor depende de outro campo já existente (ex: a engrenagem de "Total do Pedido" que calcula a soma dos itens).

## Modelo de Entidade e Relacionamento (MER)

O MER é o modelo conceitual que descreve quais informações o banco de dados vai guardar. O MER é oque descreve quais informações o banco de dados vai guardar atráves dos três elementos citados anterioemente no DER, a difereça entre MER e DER é que o MER é a ideia teórica e o DER é o desenho visual da ideia o diagrama.

## Cardinalidade

A cardinalidade é oque define quantos elementos de uma coluna podem se conectar. A cardinelidade no MER serve para ditar as regras do negócio e impedir registros impossiveis. A cardinalidade possui três tipos de regras:

- Relacionamente um para um (1:1): No relacionamento de um para um o registro só pode se conectar a um único registro de outra tabela (ex: Prefeito e cidade) só pode existir um prefeito para uma cidade.

- Relacionamento de um para muitos (1:N): No relacionamento de um para muitos um registro da tabela A pode se conectar em vários registros da tabela B, porém o da tabela B só pode se conectar a um da tabela A (ex: Cliente e pedidos), um cliente pode fazer vários pedidos, porém o pedido pertence apenas ao cliente.

- Relacionamento de muitos para muitos (N:N): No relacionaemnto de muito para muitos um registro da tabela A pode se conectar em vários da tabela B, e um registro da tabela B pode se conectar a vários da tabela A (ex: Aluno e disciplina), um aluno se conecta a várias disciplinas e várias disciplinas se conectam a um aluno.