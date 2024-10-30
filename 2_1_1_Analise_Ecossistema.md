# Preâmbulo

O marco regulatório do fomento à cultura, aprovado no Senado Federal em 04 de junho de 2024, estabelece as diretrizes e mecanismos para fortalecer e organizar a política de fomento à cultura. Será, portanto, o arcabouço legal primordial a ser seguido na implementação de sistemas de informações e arquitetura de dados relacionados ao tema.
Em seu 3º Art., incisos I, II, III e IV, o marco regulatório estabelece os conceitos de ações culturais, agentes culturais e instrumentos de execução e de captação de recursos. Esses conceitos compreendem os principais elementos do fomento à cultura.
De modo geral, as ações culturais representam o conjunto das atividades financiadas; os agentes culturais são os beneficiários e executores dessas atividades; e os instrumentos de execução e captação de recursos são os meios pelos quais o financiamento é materializado.
É importante salientar que esta divisão não compreende, necessariamente, todas as especificidades e características do fazer cultural. Em outras normativas e sistemas, por exemplo, existem classificações contundentes e robustas, explorando conceitos como projetos, oportunidades, espaços, dentre outros que também serão considerados e analisados neste documento.
Ademais, o acompanhamento e avaliação da implementação da política de fomento deve explorar questões minuciosas que podem não ser contempladas nesta tríade ação-agente-instrumento.  
Todavia, uma arquitetura baseada nestes conceitos estará efetivamente alinhada ao marco regulatório. Além disso, a partir da tríade ação-agente-instrumento é possível padronizar a terminologia e a estrutura dos dados, o que facilita a interoperabilidade e comunicação entre sistemas.   
Portanto, estes são os principais conceitos norteadores para esta análise e, consequentemente, para uma proposta de arquitetura e dicionário de dados. A seguir, o documento está organizado em um resumo inicial das principais entidades e características da arquitetura da plataforma Mapas Culturais e em seguida a análise da taxonomia guiada pelos grupos destacados no marco regulatório.

# Modelagem e Arquitetura do projeto Mapas Culturais

O Mapas Culturais representa o estado da arte em termos de sistemas que implementam o fomento à cultura, servindo como uma ferramenta fundamental para a gestão e mapeamento de informações culturais. Utilizar o Mapas Culturais como uma das bases de análise para a construção da arquitetura de dados da PNAB é crucial devido à sua maturidade e experiência na gestão de dados culturais. A plataforma está estruturada em cinco entidades principais, descritas a seguir.

## Agentes

<p>Artistas, gestores e produtores culturais estão organizados na plataforma como Agentes. Ou seja, uma rede de atores envolvidos na cena cultural responsáveis por cadastrar e acompanhar oportunidades, espaços, eventos e projetos. São os “usuários básicos” da plataforma.</p> 
<p>A tabela agente possui, dentre outras características, um nome, localização, descrição, tipo e status. A tabela se relaciona com as principais tabelas do esquema de banco de dados (oportunidades, projetos, espaços, eventos, selo, dentre outras).  A lista de agentes e diferentes exemplos podem ser observados neste link.</p>
<p>Durante o desenvolvimento deste documento, algumas questões relacionadas à arquitetura da plataforma foram esclarecidas pelo Analista de negócios do projeto e estão detalhadas a seguir:</p>

+ Qual o conceito de subsite? Como o agente está relacionado?
    + SaaS Software as a Service (“submapas” um banco de dados/sistema que consiga conversar com o banco de dados geral e apresentar resultados específicos de um local/ente). Há, também, uma perspectiva de gestão descentralizada do sistema.   
+ Como se define o conceito de selo? Ele é atribuído a um agente ou projeto?

    + Um administrador do sistema atribui (instâncias com caráter oficial). Diferentes tipos, níveis e formas a depender do ente (na função de administrador do sistema);
+ Onde estão registradas as áreas de atuação, formas de atuação (individual, coletivo, etc), galeria de vídeos, etc.
  + Agent Meta

Para mais detalhes, um diagrama de atributos e relacionamentos dos agentes no banco de dados da plataforma (tabela agent) está disponível entre os anexos, ao final deste documento.

## Oportunidades
As oportunidades compreendem a inscrição ou acompanhamento de editais, oficinas, prêmios e concursos. Um ‘agente’ cadastra uma oportunidade, que também pode possuir oportunidades-filhas (quando uma oportunidade possui diferentes oportunidades relacionadas/subordinadas).
Cada oportunidade possui uma meta, método de avaliação, configurações e características das inscrições e o conjunto de inscrições propriamente dito (todas são tabelas interdependentes). Além disso, cada oportunidade possui nome, tipo e status), descrição (curta e detalhada), período de inscrição (início-fim), dentre outras. A lista de oportunidades e diferentes exemplos podem ser observados neste link.
Para mais detalhes, um diagrama de atributos e relacionamentos das oportunidades no banco de dados da plataforma (tabela opportunity) está disponível entre os anexos, ao final deste documento.

## Eventos

Os usuários da plataforma podem cadastrar e divulgar eventos culturais de diferentes tipos. Os eventos incluem relacionamentos com as tabelas ‘Projeto’ e ‘Agente’ (cada evento pode ou não ter relação com as tabelas) e são cadastrados com nome, descrição curta e detalhada, tipo e status, dentre outros.   
Cada evento possui ainda uma meta, uma “ocorrência” (relação entre evento e espaço) e um registro de comparecimento  (todas são tabelas interdependentes no Banco de Dados). Um exemplo de evento pode ser visualizado neste link.
Para mais detalhes, um diagrama de atributos e relacionamentos dos eventos no banco de dados da plataforma (tabela event) está disponível entre os anexos, ao final deste documento.

## Espaços
Os usuários da plataforma podem cadastrar e divulgar os espaços onde desenvolvem suas atividades artísticas e culturais. Os espaços incluem relacionamentos com as tabelas ‘Projeto’ e ‘Agente’ (cada evento pode ou não ter relação com as tabelas) e são cadastrados com nome, descrição curta e detalhada, tipo e status, dentre outros.   
Para mais detalhes, um diagrama de atributos e relacionamentos dos eventos no banco de dados da plataforma (tabela space) está disponível entre os anexos, ao final deste documento.

## Projetos
Os projetos compreendem, na plataforma, leis de fomento, mostras, convocatórias e editais criados, além de diversas iniciativas cadastradas pelos usuários da plataforma. No documento de termos de uso da plataforma está associado às oportunidades em um serviço único: “Projetos e Oportunidades - podem ser criados projetos e oportunidades para que os agentes possam se inscrever. Essas informações serão públicas para os outros Usuários da plataforma”.

# Análise da Taxonomia a partir das classes Ação Cultural, Agente Cultural e Instrumentos de Execução e Captação de Recursos do Marco Regulatório da Cultura

## Agente Cultural

Segundo o marco regulatório, um Agente cultural é todo “agente atuante na arte ou na cultura, na qualidade de pessoa física, microempresário individual, empresário individual, organização da sociedade civil, sociedade empresária, sociedade simples, sociedade unipessoal ou outro formato de constituição jurídica previsto na legislação”.

Desta maneira, uma das principais questões relacionadas à representação de agentes culturais na arquitetura para a PNAB envolve a gestão de múltiplos perfis dentro de uma entidade única, como grupos, pessoas e empresas, com características e dinâmicas distintas. 

Esta questão também é verificada na arquitetura implementada pela plataforma Mapas Culturais, conforme descrito anteriormente. Segundo documento de termos de uso da plataforma, dois serviços estão associados diretamente a esta entidade, destacados a seguir. Outros serviços, como “Espaços” e “Eventos” também se relacionam, indiretamente, à definição de um “Agente Cultural”.  
+ **“Agente individual"** - Ao criar um cadastro na Plataforma, cria-se automaticamente um agente individual, considerado o agente responsável pelo Usuário. Logo, todos os dados registrados nesse agente são os dados pessoais e de trabalho individual do usuário.”
+ **“Agente coletivo"** - o Usuário poderá criar um ou mais agentes coletivos, que podem ser pessoas jurídicas registradas em cartório, com CNPJ, ou podem ser grupos ou coletivos sem formalidade jurídica.”

Diante deste cenário, uma das soluções debatidas durante o desenvolvimento deste documento é a distinção na representação de pessoas físicas (PF) e agentes culturais (AC), associados diretamente ao cadastro e execução do fazer cultural contemplado por um instrumento de fomento.

A Pessoa Física (PF) seria a entidade básica da arquitetura, com um identificador (CPF) e dados individuais possivelmente extraídos de outras bases de dados. Já os agentes culturais (AC) são entidades responsáveis por ações culturais (objeto de fomento) e podem ser coletivos, empresas ou indivíduos. E a relação entre PF e AC acontece em diferentes papeis: Representantes (pessoas que cadastram, administram e se responsabilizam pelo perfil do AC) e demais participantes (demais atores envolvidos com o AC em questão, com diferentes papeis).  

Desta maneira, a caracterização detalhada dos agentes culturais, com distinção entre os papéis de representantes e participantes, melhora a precisão dos dados coletados. Isso facilita a resposta a perguntas importantes, como a diversidade e a inclusão dos agentes culturais, além de permitir um monitoramento mais preciso das ações culturais.

A política de selos pode ser mantida para identificar perfis, com cadastros simples e a possibilidade de agregar dados, facilitando o registro de membros de comunidades, como quilombos. Ou seja, um representante de um AC Quilombo poderia cadastrar uma série de pessoas integrantes de sua comunidade, que posteriormente seriam validadas em um cadastro individual (PF verificada).

Esta arquitetura permite responder mais efetivamente às perguntas do documento "O que queremos saber", abordando aspectos como a diversidade cultural, a inclusão de diferentes perfis de agentes culturais e a descentralização das ações. Através dessa estrutura, é possível realizar um acompanhamento mais detalhado e preciso das políticas de fomento, garantindo que os objetivos da PNAB sejam atingidos com maior transparência e eficácia.

Este documento apresenta apenas um indicativo para a estruturação desta arquitetura, de modo que a definição de atributos e relacionamentos deve ser aprofundada na definição da arquitetura de dados em si.

Outro ponto crucial a ser considerado é a descentralização resultante do caráter federativo da PNAB (diferentes entes deverão interagir com a arquitetura a partir de diferentes sistemas), que deve garantir a interoperabilidade entre sistemas e abordar problemas de inconsistências, como a possibilidade de um CPF ser cadastrado múltiplas vezes por sistemas diferentes, com diferentes informações relacionadas.

## Ação Cultural

O marco regulatório da cultura define uma ação cultural como  “qualquer atividade ou projeto apoiado por políticas públicas de fomento cultural”.  Na plataforma Mapas Culturais, uma ação cultural apresenta similaridade com as categorias:

**Eventos**: A seção de eventos cobre a realização de ações culturais, permitindo que os usuários pesquisem e incluam eventos na plataforma. Estes eventos representam as produções artísticas e culturais desenvolvidas pela comunidade.

**Espaços**: Embora mais relacionados ao local físico, os espaços culturais são fundamentais para a execução das ações culturais. O cadastro e a busca de espaços onde as atividades culturais ocorrem fazem parte do suporte necessário para a realização dessas ações.

**Projetos**: Aqui se encontram leis de fomento, mostras, convocatórias e editais, além de iniciativas cadastradas pelos usuários. Esta seção abrange tanto as ações culturais (como projetos e mostras) quanto os instrumentos de fomento associados a essas ações.

Uma das principais questões relacionadas à representação de ações culturais em uma arquitetura de dados é a diversidade de tipos, categorias, formatos e outras características que uma ação cultural pode assumir.

O documento "O que queremos saber da PNAB" apresenta três recortes específicos que podem auxiliar a representação desta entidade em uma arquitetura: O MinC pretende observar durante a avaliação da política a Caracterização, Capacidade de execução da ação cultural e Resultados. No documento, se destacam questões como: “Quais ações culturais foram contempladas e com quanto recurso ? (divididos por formato, linguagem / expressão , tema e momento da cadeia produtiva) Quais produtos foram gerados? Quantos empregos e postos de trabalho foram gerados?

Durante o desenvolvimento deste documento não foi possível finalizar os debates necessários para esclarecer quais os principais atributos que uma ação cultural deve possuir em cada etapa do fluxo da PNAB, de modo que uma nova rodada de conversas e a interlocução com outras equipes do projeto devem continuar neste sentido.

## Instrumento de execução e de captação de recursos

Os instrumentos de fomento, tanto de execução quanto de captação de recursos, são essenciais para a operacionalização das políticas culturais no âmbito da PNAB. Eles incluem mecanismos como editais, prêmios, convênios, parcerias, leis de incentivo fiscal e fundos culturais, cada um com suas características específicas e processos administrativos.

A capacidade de proporcionar uma arquitetura efetiva e transparente para a gestão de recursos e a execução de políticas culturais depende da representação consistente dos instrumemntos de execução e captação de rercursos. A aplicação desses mecanismos, conforme descrito no marco regulatório, assegura que o apoio à cultura seja eficaz, abrangente e alinhado com os objetivos dos planos de cultura nacionais e regionais. 

### Instrumentos de execução de recursos

Os instrumentos de execução do regime próprio de fomento à cultura são meios jurídicos que formalizam o apoio da administração pública a ações culturais. Eles são divididos em dois grupos: Com ou Sem repasse de recursos pela Administração Pública.

**Com repasse:**

+ Termo de Execução Cultural: Usado para formalizar a relação entre a administração pública e os agentes culturais, possibilitando o repasse de recursos para a realização de ações culturais.
+ Termo de Premiação Cultural: Destinado a premiar iniciativas culturais. Visa a reconhecer relevante contribuição de agentes culturais para a cultura. Neste caso o Agente não precisa se inscrever/cadastrar obrigatoriamente.
+ Termo de Bolsa Cultural: Visa a promover ações culturais de estudos e pesquisas por meio da concessão de bolsa, contemplando atividades como: intercâmbios e residências artísticas, participação em eventos estratégicos, projetos de pesquisa para a criação de obras e espetáculos artísticos, cursos de capacitação, dentre outros.

**Sem repasse:**

+ Termo de Ocupação Cultural: Permite que espaços públicos sejam utilizados para atividades culturais, sem repasses de recursos, com o estabelecimento de data e deveres do agente cultural responsável.
+ Termo de Cooperação Cultural: Contempla situações de interesse mútuo (Adm pública-agente cultural) cujo escopo não se enquadra na hipótese de ocupação cultural. Além disso, ocorre por decisão discricionária da administração pública, sem necessidade de chamamento público.

### Instrumentos de captação de recursos

Além dos instrumentos de execução, o marco regulatório define os mecanismos para a captação de recursos privados para o fomento à cultura, com ou sem incentivo fiscal.  Esses instrumentos abrangem uma variedade de mecanismos e ferramentas legais e administrativas que viabilizam a obtenção de fundos para o financiamento de ações culturais.

### Representações para a arquitetura

As principais questões relacionadas à representação dos instrumentos públicos em uma arquitetura de dados para a PNAB incluem a necessidade de uma estrutura flexível que acomode diferentes tipos de instrumentos, como editais, prêmios e convênios, garantindo a uniformidade na definição e aplicação desses instrumentos. Além disso, a representação dos instrumentos deve ser clara e consistente, facilitando o entendimento e a utilização por todos os atores envolvidos na política cultural.

Na plataforma Mapas, encontramos a tabela Oportunidades, que está diretamente relacionada aos instrumentos de fomento do marco regulatório. Nela, os usuários podem se inscrever em editais, oficinas, prêmios e concursos, que são formas de viabilização e financiamento de ações culturais.

Assim como nas ações culturais, durante o desenvolvimento deste documento não foi possível finalizar os debates necessários para esclarecer os principais atributos que um instrumento deve possuir em cada etapa do fluxo da PNAB, de modo que uma nova rodada de conversas e a interlocução com outras equipes do projeto devem continuar neste sentido.
