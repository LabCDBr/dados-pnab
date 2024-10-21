# 2.1 Fluxo da Informação relacionada à PNAB baseado em uma abordagem Top-Down
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
Esta arquitetura é uma perspectiva do <b> Sistema Nacional de Informações da Cultura (SNIIC) </b>, possuindo uma implementação no Mapas. Para viabilizar a extração de informações relacionados aos dados na PNAB no Mapas, se faz necessária a utilização de consultas baseada em <i>Structured Query Language </i> (SQL).
O processo de criação de uma arquitetura de dados depende de um conjunto de etapas.  Na Figura 1 é apresentanda uma visão geral do processo de criação de uma proposta de arquitetura e uma visualização de dados. Para tanto, é necessário realizar a análise de requisitos, modelagem e implementação e a criação de painéis gráficos para apresentação dos indicadores. Essas etapas estão diretamente relacionados as entregas realizadas pela Equipe de Dados.
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

# Fluxo da informação orientado à execução da PNAB

<div><p>A partir do levantamento de requisitos e da inter-relação com o fluxo do plano de trabalho é possível 
definir estruturas adicionais para a execução do fluxo de dados e informações relacionadas à PNAB, mapeadas baseadas no ciclo do recurso orçamentário destinado às ações culturais, sua execução e consequente prestação de informações.</p></div>

São definidos três blocos principais para a modelagem atual: [(I) o repasse do recurso orçamentário, a partir do Governo Federal, (II) o refinamento e granularização de sua aplicação utilizando o Plano Anual de Aplicação de Recursos (PAAR) pelo ente federado](2_1_2_TransfereGov_PAAR.md) e [(III) o acoplamento ao mecanismo de acompanhamento e execução da política pública e sua consequente prestação de informações por intermédio do Mapas Culturais](2_1_3_Proposta_PNAB_Mapas.md).

