# Estrutura e Integridade dos Dados

## Sistema de chaves 

O sistema de chaves é um conjunto de regras aplicado a uma coluna para garantir a integridade dos dados. O sistema de chaves tem o objetivo de identificar registros de forma única, impedir duplicações e conectar tabelas, enquanto a cardinalidade define as regras as chaves são as ferramentas que aplicam essas regras no modelo lógico e físico, a aplicação do sistemas de chaves na modelagem de dados é o padrão que cada coluna deve seguir. Para definir a função e o relacionamento de dados nas colunas o sistema de chaves usa nomenclaturas específicas para cada função:

- Chave Primária (PK): É a coluna principal da tabela que identifica cada registro de forma única, ela funciona como um CPF do registro, não pode existir duas linhas com o mesmo valor e ela nunca pode ficar vazia/nula (ex: ID_Cliente)

- Chave Estrangeira (FK): É a coluna que faz ponte entre duas tabelas, Ela recebe esse nome porque é uma "visita" na tabela atual, mais aponta para uma chave primária em outra tabela, materializando o relacionamento no banco de dados (ex: a tabela Pedidos recebe o ID_Cliente como FK para saber quem comprou).

- Chave Composta: É a junçao de duas ou mais colunas formando uma identificação única, ela é usada quando uma coluna não é o suficiente para garantir que o registro seja único (ex: em uma tabela de itens do pedido, a combinação de ID_pedido + ID_produto forma a chave).

- Chave Candidata: São colunas que possuem valores únicos e que tinham potencial para ser Chave Primária da tabela, porém perderam a disputa e viraram colunas comuns (ex: em uma tabela de usuário com a PK sendo o ID numérico, o CPF e o Email são chaves candidatas).

## Como as Chaves aplicam a Cardinalidade

As Chaves Estrangeiras(FK) são posicionadas nas tabelas de acordo com o tipo de relacionamento definido na etapa anterior da modelagem:

- No relacionamento Um para Muitos (1:N): A regra dita que a Chave Primária da tabela "Um" sempre vai dentro da tabela "Muitos" na forma de Chave Estrangeira (ex: O ID_Cliente da tabela Cliente vai para dentro da tabela Pedidos).

- No relacionamento de Muitos para Muitos (N:N): As chaves não podem se repetir diretamente, então é criada uma nova tabela intermediária para salvar o relacionamento, essa tabela téra uma Chave Composta formada pelas Chaves Estrangeiras das tabelas originais (ex: A tabela Matricula une o ID_Aluno e o ID_Diciplina).

- No relacionamento de Um para Um (1:1): A regra permite colocar a Chave Primária de uma tabela como Chave Estrangeira na outra tabela, Geralmente escolhe-se colocar FK na tabela que depende da existência da outra para fazer sentido (ex: O ID_prefeito vai para dentro da tabela cidade).

## Normalização de Dados

A normalização é o processo de organização do modelo lógico. A normalização de dados é o processo onde organizamos o modelo lógico para evitar a repetição desnecessária de dados e anomalias (erros ao inserir, atualizar ou deletar informações). Ela funciona através de regras chamadas de Formas Normais (FN). Para um banco estar seguro, ele precisa passar por três etapas:

- Primeira Forma Normal (1FN): Exige que todos os atributos sejam simples/atômicos (Não podem existir listas de dados ou textos separados por vírgula na mesma linha) e que a tabela possua uma Chave Primária definida.

- Segunda Forma Normal (2FN): Exige que a tabela já esteja na 1FN e garanta que todos os atributos comuns dependam da Chave Primária inteira (isso serve para impedir que tabelas com Chaves Compostas guardem dados que dependem de apenas uma das partes da chave).

- Terceira Forma Normal (3FN): Exige que a tabela já esteja na 2FN e elimina as dependências transitivas. Isso significa que um atributo comum não pode depender de outro atributo comum, ele deve depender única e exclusivamente da Chave Primária (ex: em uma tabela funcionários, a coluna "Nome do Departamento" não deve ficar lá se já existe o "ID_Departamento").