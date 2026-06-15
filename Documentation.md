# Modelagem Ontológica do Sistema Petrolífero

## 1. Domínio

Um sistema petrolíferoé um modelo conceitual fundamental para a exploração de hidrocarbonetos. Ele representa o conjunto de elementos geológicos e processos responsáveis pela geração, migração, aprisionamento e acumulação de petróleo e gás natural em bacias sedimentares. A modelagem conceitual utilizada para construir a representação desta pesquisa baseou-se nos conceitos abordados por Magoon e Dow (1994) .

Do ponto de vista geológico, o sistema petrolífero é composto por elementos essenciais, como rocha geradora, rocha reservatório, rocha selante e estruturas de armadilha, que interagem de forma interdependente ao longo do tempo geológico. A rocha geradora contém matéria orgânica que, submetida a condições específicas de temperatura e pressão decorrentes do soterramento sedimentar, passa pelo processo de geração de hidrocarbonetos. Os fluidos gerados são então expulsos e transportados por caminhos de migração, camadas permeáveis ou sistemas de falhas, em direção a zonas de menor pressão, caracterizando o processo de migração. Ao encontrar uma configuração geométrica favorável, os hidrocarbonetos se acumulam e formam depósitos, no processo denominado acumulação.

A diversidade terminológica entre disciplinas geocientíficas e formatos de dados da indústria, como RESQML e OSDU, criam desafios significativos de interoperabilidade semântica. A ontologia proposta, fundamentada na BFO e alinhada à GeoCore, fornece uma representação formal e processável por máquina dos conceitos do domínio, tornando explícito o significado das entidades, suas propriedades e relações. Isso viabiliza a integração de dados entre sistemas de modelagem de bacias e de reservatórios, a harmonização terminológica entre especialistas de diferentes disciplinas, e o suporte a inferências automáticas sobre o conhecimento do domínio.

## 2. Questões de Competência

As questões de competência abaixo orientaram o desenvolvimento da ontologia:

1. Quais entidades geológicas, substâncias, qualidades e processos constituem um sistema petrolífero?
2. Como as entidades e os processos geológicos interagem para possibilitar a geração, migração, aprisionamento e acumulação de hidrocarbonetos?
3. Quais propriedades e características geológicas influenciam a ocorrência e o comportamento dos hidrocarbonetos em um sistema petrolífero?
4. Como os componentes de um sistema petrolífero estão relacionados espacial e funcionalmente dentro de uma bacia sedimentar?
5. O que distingue as diferentes disposições relacionadas as corpos rochozos em um sistema petrolífero, como selo, geradoura e reservatório?
6. Como um sistema petrolífero pode ser formalmente representado em termos de entidades geológicas, qualidades, substâncias, processos e seus relacionamentos?

---

### 3.1 Continuantes Independentes

Entidades que existem de forma completa em qualquer instante de tempo e não dependem de outro portador para existir.

**Earth Fluid / Fluidos da Terra**

| Entidades   | Descrição                                                                                                                                                                              |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Petroleum   | Um fluido terrestre que é uma ocorrência natural de hidrocarbonetos, seja em estado gasoso, líquido ou sólido, originada por processos termogênicos ou biogênicos na crosta terrestre. |
| Oil         | Um petróleo que se encontra em estado líquido a condições de superfície e é gerado principalmente por processos de maturação termal de matéria orgânica dentro da janela do óleo.      |
| Natural Gas | Um petróleo que se encontra em estado gasoso a condições de superfície e é gerado por processos termogênicos ou biogênicos.                                                            |

**Materiais Terrestres / Earth Material**

| Entidade         | Definição                                                                                                                                                                                                   |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Organic Matter   | Um material terrestre que é composto por compostos de carbono de origem biológica, presente em rochas geradoras, e que sob condições específicas de temperatura e pressão se transforma em hidrocarbonetos. |
| Rock             | Um material terrestre que é um agregado natural de minerais e/ou matéria orgânica, cuja identidade é determinada por sua composição e origem.                                                               |
| Sedimentary Rock | Uma rocha que é formada pela deposição, compactação e cimentação de sedimentos ou precipitação química em ambientes superficiais ou subsuperficiais.                                                        |
| Igneous Rock     | Uma rocha que é formada pelo resfriamento e solidificação de magma, seja na superfície (extrusiva) ou em profundidade (intrusiva).                                                                          |
| Basalt           | Uma rocha ígnea que é de composição máfica e textura fina, originada pelo resfriamento rápido de lava vulcânica, comum em ambientes de rifte continental.                                                   |
| Limestone        | Uma rocha sedimentar que é composta predominantemente por carbonato de cálcio (calcita ou aragonita), de origem biogênica ou química, podendo atuar como reservatório ou selante.                           |
| Sandstone        | Uma rocha sedimentar que é composta por grãos de areia cimentados, caracterizada por porosidade e permeabilidade intergranulares que a tornam frequente candidata a reservatório.                           |
| Shale            | Uma rocha sedimentar que é de granulação fina, laminada, composta por partículas de argila e silte, frequentemente enriquecida em matéria orgânica, e associada às funções de rocha geradora e selante.     |

**Objetos Geológicos / GeologicalObject**

| Entidade           | Definição                                                                                                                                                     |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Body of Rock       | Um objeto geológico que é um volume contínuo de rocha com extensão espacial definida, podendo corresponder a uma unidade litoestratigráfica.                  |
| Basin              | Um corpo rochoso que é uma depressão da crosta terrestre propícia ao acúmulo de sedimentos e à formação de sistemas petrolíferos.                             |
| Layer              | Um corpo rochoso que é uma camada ou estrato com propriedades relativamente homogêneas, delimitado por superfícies estratigráficas.                           |
| Shale Layer        | Uma camada que é constituída por folhelho.                                                                                                                    |
| Sandstone Layer    | Uma camada que é constituída por arenito.                                                                                                                     |
| Limestone Layer    | Uma camada que é constituída por calcário.                                                                                                                    |
| Dikes              | Um corpo rochoso que é um corpo ígneo tabular intrusivo, capaz de fornecer calor adicional à matéria orgânica adjacente ou de atuar como barreira de selagem. |
| Aggregate of Rocks | Um agregado de objetos que é composto por múltiplos corpos rochosos e que delimita geometricamente uma armadilha geológica.                                   |

**Estruturas Geológicas / GeologicalStructure**

| Entidade | Definição                                                                                                                                                                                  |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Trap     | Uma estrutura geológica que configura uma geometria tectônica ou estratigráfica, materializada em um ou mais corpos rochosos, capaz de promover o acúmulo e a retenção de hidrocarbonetos. |

---

### 3.2 Continuantes Dependentes

Entidades que dependem de um portador (*bearer*) para existir, sem existência independente.

#### Qualidades

| Entidade     | Definição                                                                                                                                                                             | Portador     |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ |
| Porosity     | Uma qualidade que inere em um material rochoso e representa a proporção volumétrica de espaços vazios disponíveis para o armazenamento de fluidos.                                    | Rock, Layer  |
| Permeability | Uma qualidade que inere em um material rochoso e representa a capacidade de transmitir fluidos por meio de uma rede de poros interconectados.                                         | Rock         |
| Pressure     | Uma qualidade que inere em um corpo rochoso e representa a força exercida por unidade de área sobre seus constituintes, influenciando processos de geração e migração.                | Layer, Dikes |
| Temperature  | Uma qualidade que inere em um corpo rochoso e representa a medida da energia cinética média de suas partículas constituintes, determinando a janela de maturação da matéria orgânica. | Layer, Dikes |

#### Disposições

| Entidade  | Definição                                                                                                                                                                                                 | Portador                         |
| --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
| Source    | Uma disposição que inere em uma camada de rocha e, sob condições específicas de temperatura e pressão, confere a capacidade de gerar e expelir hidrocarbonetos a partir da matéria orgânica nela contida. | Shale Layer                      |
| Seal      | Uma disposição que inere em uma camada de rocha e confere a capacidade de impedir a migração de hidrocarbonetos por meio de baixa permeabilidade.                                                         | Shale Layer                      |
| Reservoir | Uma disposição que inere em uma camada de rocha e confere a capacidade de armazenar e transmitir fluidos por meio de sua porosidade e permeabilidade efetivas.                                            | Sandstone Layer, Limestone Layer |

---

### 3.3 Ocorrentes

Entidades que se desenvolvem no tempo e possuem partes temporais.

| Processo     | Descrição                                                                                                                                                               |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Generation   | Um processo que consiste na transformação da matéria orgânica em hidrocarbonetos sob a ação combinada de temperatura, pressão e tempo geológico em uma camada geradora. |
| Migration    | Um processo que consiste no transporte natural dos hidrocarbonetos desde a rocha geradora até uma armadilha geológica, por meio de caminhos permeáveis.                 |
| Accumulation | Um processo que consiste na concentração de hidrocarbonetos em uma armadilha geológica, resultando na formação de um depósito de petróleo e/ou gás.                     |

---

### 3.4 Relações (Object Properties)

| Relação               | Semântica                                                                                            |
| --------------------- | ---------------------------------------------------------------------------------------------------- |
| contained_in          | Indica que o fluido hidrocarboneto está fisicamente contido em uma camada rochosa.                   |
| bounds                | Indica que um agregado de corpos rochosos delimita geometricamente uma armadilha.                    |
| high_concentration_of | Indica a concentração de matéria orgânica suficiente para caracterizar uma rocha geradora potencial. |
| constituted_by        | Indica a relação de constituição material entre uma camada e o tipo rochoso que a compõe.            |
| bearer_of             | Indica que uma camada rochosa é o portador de uma disposição funcional.                              |
| inheres_in            | Indica que uma qualidade (pressão, temperatura, porosidade, permeabilidade) inere em seu portador.   |
| has_participant       | Indica quais entidades participam de um processo geológico.                                          |
| precedes              | Expressa a ordem temporal entre geração → migração → acumulação.                                     |
| has_part              | Indica que uma armadilha é composta por camadas rochosas e/ou diques.                                |

## 5. Ontologias Importadas

| Ontologia    | URL de Importação                                                                      |
| ------------ | -------------------------------------------------------------------------------------- |
| **BFO 2020** | `http://purl.obolibrary.org/obo/bfo/2020/bfo.owl`                                      |
| **DUL**      | `http://www.ontologydesignpatterns.org/ont/dul/DUL.owl`                                |
| **GeoCore**  | `https://www.inf.ufrgs.br/bdi/ontologies/geocore/releases/2024-04-06/geocore-full.owl` |
