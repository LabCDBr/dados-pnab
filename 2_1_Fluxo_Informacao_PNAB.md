# 2.1 - Fluxo da Informação relacionada à PNAB baseado em uma abordagem Top-Down
<div>
<p>
A <b>PNAB</b> é uma política federalizada que repassa recursos do Governo Federal para estados e municípios, promovendo o fomento à cultura em todo o Brasil. A execução da política envolve a transferência de recursos para agentes culturais, como artistas, músicos e pesquisadores. No entanto, a diversidade de soluções digitais utilizadas por diferentes estados e municípios (variando de sistemas robustos a processos manuais em papel) dificulta a análise unificada e a avaliação dos impactos da política.
</p>
</div>
<div>
<p>
Este repositório faz parte de uma iniciativa inserida no <b>Termo de Execução Descentralizada (TED)</b>  do  <b>Ministério da Cultura (MinC)</b>  com a  <b>Fundação da Universidade Federal do Paraná (FUNPAR)</b>. A iniciativa visa criar padrões de dados e soluções para a  <b>interoperabilidade entre sistemas</b>, facilitando a comunicação de dados entre diferentes plataformas e promovendo uma gestão cultural mais eficiente, desenvolvendo uma arquitetura de dados.
</p>
</div>
<div>
<p>
A proposta de <b>Arquitetura de Dados da PNAB</b> é o núcleo da padronização proposta para viabilizar a interoperabilidade entre diferentes sistemas. O objetivo é garantir que todas as plataformas de gestão cultural compartilhem um modelo de dados comum, possibilitando o cruzamento e a análise centralizada. 
</p>
<p>
Esta arquitetura considera a integração entre sistemas, bem como os fluxos de dados associados, como o <b>TransfereGov, o Plano Anual de Aplicação de Recursos (PAAR) e a ferramenta Mapas Culturais (Mapas). </b> Atualmente não existe integração entre os sistemas em questão, mas se faz neessária o entendimento dos fluxos, haja vista a forte relação entre os gestão dos recursos orçamentários e o monitoramento da execução da política cultural.
</p>
<p>
Esta arquitetura é uma perspectiva do <b> Sistema Nacional de Informações da Cultura (SNIIC)</b>, possuindo uma implementação no Mapas. Para viabilizar a extração de informações relacionados aos dados na PNAB no Mapas, se faz necessária a utilização de consultas baseada em <i>Structured Query Language </i> (SQL).
O processo de criação de uma arquitetura de dados depende de um conjunto de etapas.
</p>
<p>
Inicialmente se faz necessário o entendimento da tecnologia disponível no contexto do SNIIC. Como já citado, a aplicação Mapas desempenha
papel fundamental na agregação, sistematização e disponibilização de uma mídia digital de publicação de ações culturais no cenário
nacional e internacional.
</p>
<p>
Com enfoque na representação da informação, é realizada uma análise do banco de dados existente a afim de definir quais e
como estão definidas tais Entidades.
</p>
<p>
Após o entendimento, é possível realizar a agregação, remoção ou modificação das estruturas existentes (Entidades) com o intuito de adicionar
novas funcionalidades e/ou representações desejadas, tal qual da <b>PNAB</b>. Com a representação da informação realizada,
é possível criar Visões (<B>Views</B>), possibilitando apresentar/representar um conjunto de entidades de maneira consolidada.
</p>
<p>
De forma a documentar as Visões, a aplicação de representações gráficas demonstram uma grande efetividade, sendo a utilização da técnica de Modelagem Entidade Relacionamento (<b>MER</b>) uma destas.
O MER permite a definição das Entidades e os relacionamentos entre estas na forma de elementos gráficos, facilitando a modelagem lógica. Tal modelagem da Arquitetura pode ser visualizada na Seção ZZ.
</p>
<p>
Definidas as Entidades e os relacionamentos, se faz necessário a definição das características (Atributos) que compõe tais elementos.
Um instrumento de grande valia é a utilização de Dicionários de Dados.
</p>
<p>
Este enfoque de visualização permite a criação de interfaces com atores internos e/ou externos, sejam por requisições diretas (ODBC)
ou representações utilizando <i>Javascript Object Notation</i> (<b>JSON</b>), desenvolvendo assim o conceito de <b>Interoperabilidade</b> que é apresentado na Seção XX.
</p>
<p>
Na Figura 1 é apresentanda uma visão geral do processo de criação de uma proposta de arquitetura e uma visualização de dados. Para tanto, é necessário realizar a análise de requisitos, modelagem e implementação e a criação de painéis gráficos para apresentação dos indicadores. Essas etapas estão diretamente relacionados as entregas realizadas pela Equipe de Dados.
</p>
</div>
<br>
<center> <b>Figura 1: Etapas de análise de requisitos, modelagem e visualização de dados</b></center>

![**Figura 1: Etapas de análise de requisititos, modelagem e visualização de dados**](https://lh3.googleusercontent.com/pw/AP1GczNNmAcA4L8nC8bJ0z8cjO1BMhjp82_5b7XweEidL2qWxw3dbG_5RdS8EuK-DomR0F-IJOH7sLNMoaONS4t6MJYpis2qDRDRhl4D9hNu_JkFs0Q7awNvdOVhwTKVbvJnOEmcZ1Dwiji1PdYWJJCOvFSk=w2560-h940-s-no-gm?authuser=0)

<div>
<p>
A arquitetura proposta viabilizará a <b>interoperabilidade</b> entre os diversos sistemas de gestão cultural, possbilitando uma padronização da representação e transferência de informações entre os diversos <b>Agentes </b> do sistema.
</p>
</div>

## Fluxo da informação orientado à execução da PNAB

<div><p>A partir do levantamento de requisitos e da inter-relação com o fluxo do plano de trabalho é possível 
definir estruturas adicionais para a execução do fluxo de dados e informações relacionadas à PNAB, mapeadas baseadas no ciclo do recurso orçamentário destinado às ações culturais, sua execução e consequente prestação de informações.</p></div>

Com o intuito de realizar uma extensão da representação da informação da PNAB na ferramenta de referência Mapas, a [Seção 2.1.1](2_1_1_Analise_Ecossistema.md)
realiza a análise da situação das normativas vigentes que norteiam e definem os mecanismos da execução da política pública e as informações
ensejadas pelo Ministério da Cultura (MinC). Ainda no aspecto normativo, realiza a definição dos termos de Ação Cultural e 
Agente Cultural, por exemplo, e os Instrumentos de Fomento indispensáveis para a modelagem destes a partir do Marco Reculatório da Cultura. 
No caráter técnico da análise de sistemas, descreve e relaciona as Entidades existentes no Mapas, tais como Agente, Oportunidade, Espaços e Eventos.

A [Seção 2.1.2](2_1_2_TransfereGov_PAAR.md) apresenta uma análise do fluxo orçamentário a partir do Governo Federal 
[(I)](2_1_2_TransfereGov_PAAR.md#i-do-repasse-do-recurso-orçamentário-da-união), [(II)](2_1_2_TransfereGov_PAAR.md#ii-da-granularização-da-aplicação-dos-recursos-com-o-paar) 
o refinamento e granularização de sua aplicação utilizando o Plano Anual de Aplicação de Recursos (PAAR) pelo ente federado e 
a [Seção 2.1.3](2_1_3_Proposta_PNAB_Mapas.md) o acoplamento ao mecanismo de acompanhamento e execução da política pública 
e sua consequente prestação de informações por intermédio do Mapas Culturais.

