# <center>Banco de Dados NoSQL</center>

### <center>Introdução ao MongoDB e Banco de Dados NoSQL</center>

---

![ranking](./img/ranking_BD.jpg)

#### 1- Introdução:

* ***O que são bancos de dados NoSQL?***

***NoSQL*** é um termo genérico que representa os ***bancos de dados não relacionais***.   
Uma classe definida de banco de dados que fornecem um mecanismo para armazenamento e recuperação de dados que são modelados de formas diferentes das relações tabulares usadas nos bancos de dados relacionais.

* ***Como funciona um banco de dados NoSQL (não relacional)?***

Os bancos de dados ***NoSQL*** usam uma variedade de modelos de dados para acessar e gerenciar os dados.

Esses tipos de banco de dados são otimizados especificamente para aplicativos que exigem modelos de grande volume de dados, baixa latência e flexibilidade.

Esses requisitos são atendidos mediante o relaxamento de algumas restrições de consistência de dados dos outros bancos.

Considere o exemplo de modelagem do esquema para um banco de dados simples de livros:

Em um banco de dados relacional, um registro de livro é normalmente disfarçado (ou “normalizado”) e armazenado em tabelas separadas, e os relacionamentos são definidos por restrições de chave primária e externa.

Neste exemplo, a tabela Livros têm colunas para ISBN, Título do livro e Número da edição, a tabela Autores têm colunas para AuthorID e Nome do autor e, finalmente, a tabela Author-ISBN tem colunas para AuthorID e ISBN.

O modelo relacional é projetado para permitir que o banco de dados imponha a integridade referencial entre as tabelas no banco de dados, normalizadas para reduzir a redundância e geralmente otimizadas para armazenamento.

Em um banco de dados NoSQL, um registro de livro é normalmente armazenado como um documento JSON.

Para cada livro, o item, o ISBN, o Título do livro, o Número de edição, o Nome do autor e o AuthorID são armazenados como atributos em um único documento.

Neste modelo, os dados são otimizados para desenvolvimento intuitivo e escalabilidade horizontal.

* ***Por que você deve usar um banco de dados NoSQL?***

Os bancos de dados NoSQL são ideais para muitos aplicativos modernos, como dispositivos móveis, Web e jogos, que exigem bancos de dados flexíveis, escaláveis, de alta performance e altamente funcionais para proporcionar ótimas experiências aos usuários.

***Flexibilidade***: os bancos de dados NoSQL geralmente fornecem esquemas flexíveis que permitem um desenvolvimento mais rápido e iterativo.  

O modelo de dados flexível torna os bancos de dados NoSQL ideais para dados semiestruturados e não estruturados.

***Escalabilidade***: os bancos de dados NoSQL geralmente são projetados para serem escalados horizontalmente usando clusters distribuídos de hardware, em vez de escalá-los verticalmente adicionando servidores caros e robustos.

Alguns provedores de nuvem lidam com essas operações nos bastidores como um serviço totalmente gerenciado.

***Alta performance***: o banco de dados NoSQL é otimizado para modelos de dados específicos e padrões de acesso que permitem maior performance do que quando se tenta realizar uma funcionalidade semelhante com bancos de dados relacionais.

***Altamente funcional***: os bancos de dados NoSQL fornecem APIs e tipos de dados altamente funcionais criados especificamente para cada um de seus respectivos modelos de dados.

![](./img/tipos_bd_nosql.png)

* ***Tipos de bancos de dados NoSQL***

    * ***Colunares***:  

        Banco de dados colunares possuem o armazenamento orientado a colunas, o que influencia significativamente na sua performance, já que diminuem a quantidade de dados que você precisará carregar no disco.

        Esses bancos de dados utilizam-se de tabelas para representar entidades e seus dados são gravados em discos e agrupados por colunas separadas. 

        Como vantagens podemos listar:

        Capacidade de compreensão dos dados;
        Indicados para sistemas que precisam ler e realizar operações de consultas em grandes volumes de dados (OLAP);

        Como exemplo de banco de dados colunares podemos citar o ***Cassandra***.

        Desenvolvido em Java, gratuito e multiplataforma, o Cassandra foi originalmente desenvolvido no Facebook, que em 2008 compartilhou seu código-fonte para a comunidade e agora é um projeto de sistema de banco de dados mantido pelos desenvolvedores da fundação Apache e por muitas outras empresas que se tornaram colaboradoras (Apache Cassandra).

        Dentre suas características, podemos destacar:

        Altamente escalável;
        Fornece acesso de baixa latência a clientes;
        Gratuito;
        Orientado por colunas (o que torna um banco de dados mais rápido);
        Possui um modelo distribuído otimizado e descentralizado, entre outros.

    * ***Documentos***:

        Também conhecido como armazenamento por documentos, os bancos de dados orientados a documentos são um modelo de banco de dados projetado para gerenciar, armazenar e recuperar informações orientadas a documentos, não carecendo de colunas pré-montadas, como vimos acima no Cassandra, e é um modelo eficiente para o trabalho com dados não estruturados (que não podem ser organizados em tabelas).

        Popularmente conhecido por ser um dos principais da categoria de banco de dados NoSQL, tem como principal característica o fato de conter todas as informações em um único documento.

        Como exemplo de banco de dados orientado a documentos podemos citar o ***MongoDB***.

        De código aberto, multiplataforma e lançado em 2009, o MongoDB é considerado um “líder” no quesito SGBD NoSQL. 

        Orientado a documentos e baseado no formato JSON (JavaScript Object Notation), possui uma curva de aprendizagem baixíssima.

        Dentre suas principais características, podemos citar:

        Totalmente gratuito;
        Possui uma baixa curva de aprendizagem, como dito acima;
        Fácil escalabilidade horizontal;
        Multiplataforma;
        Suporte para transações ACID multi-documento;
        Consultas suportam funções JavaScript personalizadas, entre outros.

    * ***Grafos***: 

        Com a armazenagem de documentos em forma de grafos, no banco de dados orientado a grafos os dados são predispostos no formato de arcos conectados por arestas. 

        Criados especificamente para possibilitar o armazenamento de relacionamentos e a navegação, utilizam nós para armazenar entidades de dados e bordas para armazenar os relacionamentos entre estas entidades. 

        Foi um tipo de Banco de dados criado especialmente para lidar com as limitações de banco de dados relacionais.

        Voltado para trabalho com dados altamente conectados e com relacionamentos dinâmicos em grandes volumes, são bastante utilizados para aplicações como redes sociais, sistema de recomendações e outros tipos de dados mais complexos. 

        Como exemplo de banco de dados orientado a grafos podemos citar o ***Neo4j***.

        Desenvolvido pela ***Neo4j***, é um banco de dados orientado a grafos lançado em 2007 escrito em Java, open source que possui disponível uma “edição da comunidade” de código aberto licenciada pela GPL3. 

        Utilizado por grandes empresas como Walmart e LinkedIn, por exemplo, possui uma linguagem de acesso simples e intuitiva para grafos.

        Dentre suas principais características, podemos citar:

        Linguagem de acesso simples e intuitiva para grafos;
        Possui uma linguagem de consulta própria chamada Cypher;
        Possui uma comunidade bem ativa no Github e Stackoverflow;
        Os dados podem ser acessados utilizando uma API em Java ou uma API RESTful, entre outras.

    * ***Chave-valor***:

        Bastante simples, o banco de dados do tipo chave-valor é formado apenas por pares de chaves com valores associados, permitindo obter os valores quando uma consulta é realizada a uma chave.

        Por conta de sua simplicidade, não são empregados em aplicações mais complexas.

        Uma de suas principais aplicações são os sistemas de armazenamento embarcados e dados em cache. 

        Como exemplo de banco de dados do tipo chave-valor podemos citar o ***Redis***.

        Redis é o banco de dados de chave-valor mais popular do mundo, ou seja, seus dados são armazenados em forma de chave valor, que armazenam objetos indexados por chaves e possibilitam a busca por estes objetos a parte das mesmas.

        Criado por Salvatore Sanfiippo, foi liberado de forma open-source em 2009.

        É escrito utilizando a linguagem de programação C, porém, compatível com várias outras linguagens de programação como: Java, Python, PHP, C++, entre outras.

        Extremamente rápido, tanto para escrita como para leitura de dados, pois seus dados são armazenados na memória, seus comandos são executados anatomicamente e possui modelcliente-servidor. 

        Dentre suas principais características, podemos citar:

        Desempenho muito rápido;
        Multiplataforma;
        Estruturas de dados na memória;
        Versatilidade e facilidade de uso;
        Replicação e persistência;
        Compatibilidade com a sua linguagem de desenvolvimento preferencial, entre outros.

Característica | Bancos de dados relacionais | Bancos de dados NoSQL
--------------------------|-----------------------------|----------------------------
Cargas de trabalho ideais | Bancos de dados relacionais são projetados para aplicativos transacionais e fortemente consistentes de processamento de transações online (OLTP) e são bons para processamento analítico online (OLAP). | 	Os bancos de dados do NoSQL são projetados para vários padrões de acesso aos dados que incluem aplicativos de baixa latência. Os bancos de dados de pesquisa NoSQL são projetados para análise de dados semiestruturados.
Modelo de dados	|O modelo relacional normaliza dados em tabelas, compostas por linhas e colunas. Um esquema define estritamente tabelas, colunas, índices, relações entre tabelas e outros elementos do banco de dados. O banco de dados impõe a integridade referencial nos relacionamentos entre as tabelas. | Os bancos de dados NoSQL fornecem uma variedade de modelos de dados, como chave-valor, documento e gráfico, que são otimizados para performance e escala.  
Propriedades ACID | Bancos de dados relacionais fornecem propriedades de atomicidade, consistência, isolamento e durabilidade (ACID): **Atomicidade** exige uma transação para executar completamente ou não é executada de forma alguma. **Consistência** exige que, quando uma transação é confirmada, os dados devem estar em conformidade com o esquema do banco de dados. **Isolamento** exige que as transações simultâneas sejam executadas separadamente umas das outras. **Durabilidade** exige a capacidade de se recuperar de uma falha do sistema ou falta de energia inesperada para o último estado conhecido. | Os bancos de dados NoSQL geralmente fazem compensações relaxando algumas das propriedades ACID dos bancos de dados relacionais para um modelo de dados mais flexível que pode ser escalado horizontalmente. Isso torna os bancos de dados NoSQL uma excelente opção para casos de uso de baixa latência e alta taxa de transferência que precisam ser escalados horizontalmente além das limitações de uma única instância.
Performance | A performance normalmente depende do subsistema do disco. A otimização de consultas, índices e estrutura de tabela é necessária para alcançar máxima performance. | A performance geralmente é uma função do tamanho do cluster do hardware subjacente, da latência de rede e do aplicativo que faz a chamada.
Escala | Os bancos de dados relacionais geralmente escalam verticalmente o tamanho ao aumentar os recursos de computação do hardware, ou escalam horizontalmente o tamanho ao adicionar réplicas para cargas de trabalho somente leitura. | Os bancos de dados NoSQL normalmente são particionáveis porque os padrões de acesso podem escalar horizontalmente o tamanho usando arquitetura distribuída para aumentar a taxa de transferência que fornece performance consistente em escala quase ilimitada.
APIs | As solicitações para armazenar e recuperar dados são comunicadas usando consultas compatíveis com uma Structured Query Language (SQL – Linguagem de consultas estruturadas). Essas consultas são analisadas e executadas pelo banco de dados relacional. | APIs baseadas em objetos permitem que desenvolvedores de aplicativos armazenem e restaurem facilmente estruturas de dados. As chaves de partição permitem que os aplicativos procurem pares de chave-valor, conjuntos de colunas ou documentos semiestruturados que contenham objetos e atributos de aplicativos serializados.

* ***Terminologias SQL x NoSQL***

A tabela a seguir compara alguns exemplos de terminologia usada pelos bancos de dados (SQL) selecionados com a terminologia usada pelos bancos de dados NoSQL.

(SQL)  | MongoDB | DynamoDB | Cassandra | Couchbase
-------|---------|----------|-----------|-----------
Tabela | Coleta  | Tabela   | Tabela    |Bucket de dados
Linha  | Documento | Item | Linha | Documento
Coluna | Campo | Atributo | Coluna | Campo
Chave primária | ObjectId | Chave primária |Chave primária | ID do documento
Índice | Índice | Índice secundário | Índice | Índice
Visualização | Visualização | Índice secundário global | Visualização materializada |Visualização
Tabela ou objeto aninhado | Documento incorporado | Mapa | Mapa | Mapa
Matriz | Matriz | Lista | Lista | Lista

---

#### 2- Introdução ao MongoDB:

***Banco de Dados Orientado a Documentos***

A definição geral apresentada é que os Bancos de Dados orientados a Documentos utilizam o conceito de dados e documentos autocontidos e auto descritivos, e isso implica que o documento em si já define como ele deve ser apresentado e qual é o significado dos dados armazenados na sua estrutura.

Banco de Dados Orientados a Documentos tem como característica conter todas as informações importantes em um único documento, ser livre de esquemas, possuir identificadores únicos universais (UUID), possibilitar a consulta de documentos através de métodos avançados de agrupamento e filtragem (MapReduce) e também permitir redundância e inconsistência.

Esses bancos de dados também são chamados de Bancos NoSQL (Not Only SQL).   
Esse termo NoSQL é devido à ausência do SQL, mas esse tipo de Banco de Dados não se resume apenas a isso, por isso o termo não é o mais correto para esse novo tipo de Banco de Dados.  

No entanto, ele é aceito porque o termo já se popularizou na comunidade.

Alguns chegaram a defender o termo NoREL (Not Relational), mas diferente do anterior este não foi muito aceito.   
De forma resumida esse tipo de Banco de Dados não traz consigo as ideias do modelo relacional e nem a linguagem SQL. 

Uma diferença fundamental entre os dois modelos surge quando precisamos criar relacionamentos nos bancos de dados relacionais, diferente dos bancos orientados a documentos que não fornecem relacionamentos entre documentos, o que mantém seu design sem esquemas. 

Dessa forma, ao invés de armazenar dados relacionados em uma área de armazenamento separado, os bancos de dados de documentos integram esses dados ao próprio documento. 

Contudo, ainda assim é possível armazenar dados relacionados de forma separada, isso pode ser feito usando uma coleção separada, porém, é preciso tomar cuidado com isso visto que os ganhos de desempenhos podem ser perdidos.

Existem diversos Banco de Dados NoSQL hoje, os mais conhecidos são:   
MongoDB, DynamoDB, Azure Table Storage, Berkeley DB, Hadoop, Cassandra, Hypertable, Amazon SimpleDB, CouchDB, RavenDB, Neo4J, Infinite Graph, InforGrid, etc.

***Características do MongoDB***

O MongoDB é um banco de dados orientado a documentos, diferente dos Bancos de dados tradicionais que seguem o modelo relacional.

Dessa forma, já temos uma primeira diferença entre os dois modelos, onde o Banco orientado a documentos lida com documentos e não com registros como no modelo relacional onde tudo é representado usando uma abordagem bidimensional (tabelas representadas através de duas dimensões: linhas e colunas).

Este Banco de Dados tem como característica ser código-fonte aberto licenciado pela GNU AGPL (Affero General Public License) versão 3.0, possuir alta performance, não possuir esquemas, ser escrito em C++, multiplataforma e ser formado por um conjunto de aplicativos JSON.   

Apesar do projeto MongoDB ter iniciado em 2007 o Banco de Dados somente foi concluído em 2009 lançando assim a primeira versão do MongoDB.   

Diversas linguagens e plataforma já possuem drivers para o MongoDB, entre elas destacam-se:   
C, C#, C++, Haskell, Java, JavaScript, Perl, PHP, Python, Ruby e Scala. Além disso, o MongoDB possui binários para diversas plataformas como Windows, Mac OS X, Linux e Solaris.

Entre as empresas que já utilizam o MongoDB destacam-se:   
Globo.com, SourceForge, FourSquare, MailBox (serviço de e-mail do Dropbox), LinkedIn, SAP, MTV, Pearson Education, e muitos outros.   

***Instalando o MongoDB***

Para instalar o MongoDB devemos primeiramente baixa-lo, escolhendo uma versão de sistema operacional.

Agora já podemos descompactar o zip para alguma pasta.

Após isso devemos ir até a pasta onde descompactamos o MongoDB e ir na pasta “bin”.

Por fim executamos o “mongod.exe”.

Agora já podemos executar o cliente de Shell do MongoDB.

O aplicativo de Shell do MongoDB está incluído junto com a distribuição sendo localizado na pasta “bin”.

No Windows, está na forma do aplicativo mongo.exe.

Através deste Shell podemos criar bancos de dados, documentos e coleções.

Se em qualquer momento for preciso obter ajuda, basta dar o comando "help" na linha de comando do Shell do Mongo.

Por padrão, o Shell do Mongo se conecta ao banco de dados "test".

Para mudar para outro banco de dados, usamos o comando "use nomeDoBanco".

Se o banco de dados não existir o MongoDB o criará assim que forem incluídos dados nele.

O Shell deve apresentar a mensagem: switched to db meuMongoDB.

---

#### 3- MongoDB - CRUD(Create,Read,Update,Delete) - Alguns exemplos:

***Create***:

>db.people.insert({name: 'Tom', age: 28});

Ou

>db.people.save({name: 'Tom', age: 28});

A diferença com **save(salvar)** é que se o documento passado contiver um campo _id, se já existir um documento com esse
_id será atualizado em vez de ser adicionado como novo.

Dois novos métodos para inserir documentos em uma coleção, no MongoDB 3.2.x:

- Use **insertOne** para inserir ***apenas um registro***:
>db.people.insertOne({nome: 'Tom', idade: 28});

Use **insertMany** para ***inserir vários registros***:
>db.people.insertMany([{nome: 'Tom', idade: 28},{nome: 'João', idade: 25}, {nome: 'Kathy', idade: 23}])

Observe que insert é destacado como obsoleto em todos os drivers de idioma oficial desde a versão 3.0.

A distinção completa sendo que os métodos do shell na verdade ficaram atrás dos outros drivers na implementação do método.

A mesma coisa aplica-se a todos os outros métodos CRUD

***Read***:

***Consulte todos os documentos na coleção de pessoas*** que tenham um campo de nome com um valor de 'Tom' :
>db.people.find({name: 'Tom'})

***Ou apenas o primeiro***:

>db.people.findOne({name: 'Tom'})

Você também pode especificar quais campos devem ser retornados passando um parâmetro de seleção de campo.

O seguinte excluirá o campo _id e incluir apenas o campo idade:
>db.people.find({nome: 'Tom'}, {_id: 0, idade: 1})

Nota: por padrão, o campo _id será retornado, mesmo que você não o solicite.

Se você não quiser recuperar o _id, você pode simplesmente seguir o exemplo anterior e pedir que o _id seja excluído especificando _id: 0 (ou _id: false ).

Se você deseja encontrar sub-registro como objeto de endereço contém país, cidade, etc.
>db.people.find({'endereço.país': 'EUA'})

e especifique o campo também se necessário

>db.people.find({'address.country': 'US'}, {'name': true, 'address.city': true})

Lembre-se de que o result tem um método `.pretty()` que imprime o JSON resultante:
>db.people.find().pretty()

***Update***:

Atualize o objeto inteiro:

>db.people.update({nome: 'Tom'}, {idade: 29, nome: 'Tom'})

Novo no MongoDB 3.2:

>db.people.updateOne({name: 'Tom'},{age: 29, name: 'Tom'})

Irá substituir apenas a primeira correspondência documento.

>db.people.updateMany({name: 'Tom'},{age: 29, name: 'Tom'})

Irá substituir todos os documentos correspondentes.

Ou apenas atualize um único campo de um documento.
Neste caso, idade:
>db.people.update({name: 'Tom'}, {$set: {age: 29}})

Você também pode atualizar vários documentos simultaneamente adicionando um terceiro parâmetro.
Esta consulta atualizará todos documentos onde o nome é igual a Tom :
>db.people.update({name: 'Tom'}, {$set: {age: 29}}, {multi: true})

Novo no MongoDB 3.2:
>db.people.updateOne({name: 'Tom'},{$set:{age: 30})

Irá atualizar apenas o primeiro documento correspondente.
>db.people.updateMany({name: 'Tom'},{$set:{age: 30}})

Irá atualizar todos os documentos correspondentes.

Se um novo campo estiver chegando para atualização, esse campo será adicionado ao documento.

>db.people.updateMany({nome: 'Tom'},{$set:{idade: 30, salário:50000}})

Documento terá `salário` campo também.

Se for necessário substituir um documento,
>db.collection.replaceOne({name:'Tom'}, {name:'Lakmal',age:25,address:'Sri Lanka'})

pode ser usado.

Observação: os campos usados ​​para identificar o objeto serão salvos no documento atualizado.
Campos que não estão definidos na seção de atualização será removida do documento.

***Delete:***

Exclui todos os documentos que correspondem ao parâmetro de consulta:

no MongoDB 3.2:
>db.people.deleteMany({name: 'Tom'})

Todas versões:
>db.people.remove({name: 'Tom'})

Ou apenas um

no MongoDB 3.2:
>db.people.deleteOne({name: 'Tom'})

Todas versões:
>db.people.remove({name: 'Tom'}, true)

O método remove() do MongoDB.

Se você executar este comando sem nenhum argumento ou sem argumento vazio, ele removerá todos os documentos da coleção.

>db.pessoas.remover();

ou

>db.pessoas.remove({});

---

***Vantagens***

Utilizando MongoDB temos uma melhor performance, visto que uma única consulta retorna tudo o que precisamos saber sobre o documento.

Os banco de dados NoSQL apresentam vantagens sobre os outros quando precisamos de escalabilidade, flexibilidade, manipulação de quantidade massiva de dados, bom desempenho e facilidade para consultas.

O MongoDB possui consultas bastantes simples de serem realizadas, visto que não existem transações e joins.

As consultas são mais fáceis de escrever e mais fáceis de ajustar.

O escalonamento horizontal com Sharding é muito bem implementado no MongoDB. Sharding é utilizado quando temos muitos dados e estamos no limite do disco, dessa forma dividimos esses dados entre várias máquinas, assim temos mais rendimento e maior capacidade de armazenamento em disco.

Portanto, quanto mais Shards maior será o armazenamento e o desempenho.

O MongoDB disponibiliza essa opção. Para mais detalhes sobre Sharding podemos consultar a documentação oficial na página oficial do MongoDB.

Banco de dados relacionais muito utilizados como o MySQL não suportam esse tipo de solução por padrão, para isso teríamos que manipular os dados em uma camada acima da base de dados, sendo muito mais trabalhoso.

Como a linguagem de consulta SQL é fácil de ser convertida para MongoDB temos uma maior facilidade para migração de organizações que atualmente usam bancos de dados relacionais.

Por fim, o MongoDB também possui a funcionalidade chamada GridFS que é responsável por armazenar arquivos de grandes dimensões.

Isso significa que vídeos, arquivos, etc, podem ser armazenados diretamente no banco de dados, diferente do modelo relacional que tinhamos que armazenar tudo no Filesystem e disponibilizar apenas uma referência para esses arquivos no banco de dados.

O tempo de resposta desses arquivos armazenados no MongoDB é comparado ao tempo de resposta dos arquivos em Filesystems.

***Desvantagens***

Uma desvantagem é quando queremos alterar todos os registros relacionados a uma unidade semântica, nesse caso é preciso tratar um a um.

Uma pergunta a ser respondida ainda é a dúvida que todos os usuários possuem em relação ao suporte do MongoDB que todas as grandes empresas e projetos de alto valor necessitam.

Até que ponto o MongoDB oferece esse suporte necessário?

 Outro ponto é em relação a disponibilidade do serviço.
 
 Essas e outras perguntas serão respondidas ao longo do tempo, o fato é que muitas empresas de grande porte tem utilizado em projetos de complexidade média, uma escolha natural devido ao pequeno tempo que essa nova tecnologia está no mercado e os resultados têm sido muito satisfatórios.

---
