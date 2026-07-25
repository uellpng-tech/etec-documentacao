# As Doze Regras de Edgar F. Codd

## Edgar F. Codd

Edgar Frank Codd nasceu em Fortuneswell, na Ilha de Portland, Dorset Inglaterra. Matemático, cientista da computação, pesquisador, professor e piloto militar, Edgar Codd foi um cientista da computação muito importante para o progresso da área de TI como um todo, mais específicamente um grande avanço em banco de dados, Codd foi o criador do modelo relacional de banco de dados, esse modelo aborda a separação entre a estrutura lógica dos dados e o armazenamento físico, organizando as informações em tabelas de linhas e colunas. Essa criação possibilitou a mudança no modo de sistema de dados da epoca assim facilitando o uso dessa ferramenta.

## As Doze Regras de Codd

Com a criação do sistema relacional, Edgar também trouxe as regras de Codd. As regras de Codd definem os critérios necessários para que um sistema gerenciador de banco de dados (SGBD) seja considerado verdadeiramente relacional (Um gerenciador de banco de dados SGBD é um software destinado a conectar usuário, aplicações e banco de dados, controlando o armazenando, a organização e o acesso a todas as informaçẽs.), o conceito é bem simples, Edgar aborda 13 regras de 0 a 12 que definem um SGBD como verdadeiramente relacional.

- Regra 0 (Regra fundamental): O SGBD deve gerenciar o banco de dados usando exclusivamente suas capacidades relacionais. Resumindo o sistema não pode bordar atalhos ou métodos dos sistemas antigos como por exemplo ponteiros de baixo nível ou navegação física.

- Regra 1 (Regra da Informação): Todos os dados devem ser representados explicitamente em tabelas. Os dados devem ser representados através de linhas e colunas.

- Regra 2 (Acesso Garantido): Cada dado é acessível logicamente usando o nome da tabela, a linha e o nome da coluna. Os dados devem ser acessíveis sendo navegados ou refêrenciados através da sinalização simples de sua tabela, linha (Chave primária)e nome da coluna.

- Regra 3 (Tratamento de Nulos): Valores Nulos devem ser suportados para representar dados ausentes ou desconhecidos de forma uniforme. Os valores NULL devem ser reconhecidos para representar dados ausentes ou desconhecidos.

- Regra 4 (Catálogo Dinâmico Online): A estrutura do banco de dados deve ser armazenada em um catálogo online acessível aos usuários autorizados.Ela determina que um SGBD verdadeiramente relacional não diferencia a estrutura do sistema dos dados que ele carrega.

- Regra 5 (Sublinhagem Abrangente): O sistema deve ter ao menos uma linguagem que suporte definição, manipulação, segurança e transação de dados. A regra diz que o sistema tem que possuir uma única linguaem unificada capaz de resolver as necessidades do banco de dados.

- Regra 6 (Atualizações de Visões): Todas as visões que podem ser atualizadas teoricamente também devem ser atualizáveis pelo sistema. Todas as visões devem ser capazes de serem atualizadas pelo sistema.

- Regra 7 (Inserção, Atualização e Exclusão): O SGBD deve permitir operações em conjuntos de linhas, e não apenas em uma linha por vez. As operações que abordam mais de uma linha devem ser permitidas pelo sistema.

- Regra 8 (Independência Física): Mudanças no armazenamento físico ou estruturas de acesso não devem afetar os programas aplicativos. As mudanças de estrutura de acesso ou armazenamento não podem afetar o funcionamento dos programas aplicativos.

- Regra 9 (Independência Lógica): Mudanças na estrutura lógica das tabelas não devem afetar o funcionamento das aplicações. As mudanças de estrutura lógica não podem afetar aplicações.

- Regra 10 (Independência de Integridade): As regras de integridade devem ser definidas na linguagem do banco, e não nos programas externos. As travas de segurança e consistencia devem morar dentro do banco de dados, nenhuma linguagem externa deve se vincular a isso, evitando assim a vulnerabilidade do banco de dados.

- Regra 11 (Independência de Distribuição): O banco distribuído deve funcionar como se fosse centralizado para o usuário final. O produto final deve ser simples para o usuário.

- Regra 12 (Não Subversão): Se o sistema possui uma linguagem de registro único, ela não pode burlar as regras de integridade ou segurança da linguagem relacional principal. A linguagem externa não pode burlar as regras de seguraça para não comprometer o banco de dados.