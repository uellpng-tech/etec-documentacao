## Modelagem de Dados: Lógica e Abstração

## Abstração

A abstração dentro da modelagem de dados, é o processo de filtrar a realidade. A abstração é o processo de adaptação de uma realidade priorizando necessidades do cliente e trazendo esses conceitos para a modelagem de dados, é basicamente pegar oque é importante para o cliente e montar uma base para construção da parte lógica. A abstração possui processos também, a importancia desses processos é a construção de uma base sólida na montagem de um banco de dados.

- Modelo conceitual (Alto nível da abstração): Nesse nível a prioridade é descrever oque o banco de dados conterá. É o modelo utilizado para validar os requisitos com o cliente, fugindo dos detalhes técnicos e focando na semântica, clareza e comunicação.

- Modelo Lógico (Nível médio de abstração): Nesse nível o foco é formalizar as estruturas de dados, traduzindo o modelo conceitual para as regras de      banco de dados. Nesse nível adequamos as regras de estrutura relacional, chaves, tipos de dados...

- Modelo Físico (Baixo nível de abstração): Nesse nível deixamos o formato simples de lado e focamos na performance, armazenamente, otimização... focando na parte técnica. Apartir desse ponto descrevemos como os dados serão armazenados fisicamente e escolhemos ou seguimos o tipo de sistema SGBD (Sistema Gerenciador de Banco de Dados).

## Lógica

A lógica é oque dita as regras para a simplificação da abstração. A lógica dita as regras da estrutura criada (ex: CPF deve ser único, Saldo não pode ser menor que zero), nessa etapa usamos a estrutura criada na abstração para dar inteligência a essa estrutura. Dentro da lógica a três pilares para a moldagem da estrutura abordada pela abstração anteriormente.

- Determinismo: A lógica deve garantir que o sistema seja previsível. Se a uma regra lógica o sistema precisa se comportar sempre da mesma forma sob as mesmas condições.

- Relação e Conexão: A lógica determina como os elementos que a abstração filtrou conversam entre si. Ela cria as conexões e dependências entre os dados.

- Restrição e Validação: A lógica impede o caos. Ela cria barreiras matemáticas para garantir que os dados façam sentido no mundo real, isso evita contradições entre od dados (evitar estado falso).

## Conclusão

A Abstração e a Lógica são as estruturas da modelagem de dados. A Modelagem de dados utiliza diversos termos e metodos tecnicos para estruturar uma estrutura de dados, a estrutura apresentada é o macro de tudo que representa a modelagem de dados, sendo a abstração a filtragem e o processo inicial, e a lógica a aplicação das leis e a conexão das estruturas obtidas com a abstração.

- Modelagem de dados
    - Abstração
        - Lógica