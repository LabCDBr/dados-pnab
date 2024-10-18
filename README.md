# Proposta de arquitetura de dados da Política Nacional Aldir Blanc (PNAB)
<div align="justify">
<p>
Este repositório trata sobre uma proposta de arquitetura de dados para a representação da informação relacionada a implementação de mecanismos relacionados a <a href="https://www.gov.br/cultura/pt-br/acesso-a-informacao/perguntas-frequentes/politica-nacional-aldir-blanc">Política Nacional Aldir Blanc (PNAB)</a>. <i>Este repositório está em fase de desenvolvimento e compreende diferentes entregas do projeto. <b>Qualificação do Ecossistema de Soluções Digitais para Mapeamento e Gestão Cultural, objeto do Termo de Execução Descentralizada  XYZ</b>.</i>
</p>
</div align="justify">

### Equipe
-   **Modelagem e Desenvolvimento**: Alexandre Cajazeira e Elliott Chaves - Cientistas de Dados / UFPR;
-   **Supervisão Técnica**: Uirá Porã - Analista de Negócio / UFPR;
-   **Gestão**: Sofia Von Mettenheim, Alexandre Santos (SGE/MinC) e Juliana Almeida (SGE/MinC).

<div align="justify">
<p>
Para tanto, este documento é composto por uma Introdução, Fundamentação Legal e Teórica, Modelo Entidade Relacionamento e Dicionário de Dados. O documento possui relacões com elementos externos, para convalidação de uma proposta de arquitetura.</p></div>



# Introdução
<div align="justify">
<p>
A <b>PNAB</b> é uma política federalizada que repassa recursos do Governo Federal para estados e municípios, promovendo o fomento à cultura em todo o Brasil. A execução da política envolve a transferência de recursos para agentes culturais, como artistas, músicos e pesquisadores. No entanto, a diversidade de soluções digitais utilizadas por diferentes estados e municípios (variando de sistemas robustos a processos manuais em papel) dificulta a análise unificada e a avaliação dos impactos da política.
</p>
</div>
<div align="justify">
<p>
Este repositório faz parte de uma iniciativa inserida no <b>Termo de Execução Descentralizada (TED)</b>  do  <b>Ministério da Cultura (MinC)</b>  com a  <b>Fundação da Universidade Federal do Paraná (FUNPAR)</b>. A iniciativa visa criar padrões de dados e soluções para a  <b>interoperabilidade entre sistemas</b>, facilitando a comunicação de dados entre diferentes plataformas e promovendo uma gestão cultural mais eficiente, desenvolvendo uma arquitetura de dados.
</p>
</div>
<div align="justify">
<p>
A proposta de <b>Arquitetura de Dados da PNAB</b> é o núcleo da padronização proposta para viabilizar a interoperabilidade entre diferentes sistemas. O objetivo é garantir que todas as plataformas de gestão cultural compartilhem um modelo de dados comum, possibilitando o cruzamento e a análise centralizada. 
</p>
<p>
Esta arquitetura considera a integração entre sistemas, bem como os fluxos de dados associados, como o <b>TransfereGov, o Plano Anual de Aplicação de Recursos (PAAR) e a ferramenta Mapas Culturais (Mapas). </b> Atualmente não existe integração entre os sistemas em questão, mas se faz neessária o entendimento dos fluxos, haja vista a forte relação entre os gestão dos recursos orçamentários e o monitoramento da execução da política cultural.
</p>
<p>
Esta arquitetura é uma perspectiva do <b> Sistema Nacional de Informações da Cultura (SNIIC) </b>, possuindo uma implementação no Mapas. Para viabilizar a extração de informações relacionados aos dados na PNAB no Mapas, se faz necessária a utilização de consultas baseada em <i>Structured Query Language </i> (SQL).
</p>
O processo de criação de uma arquitetura de dados depende de um conjunto de etapas.  Na Figura 1 é apresentanda uma visão geral do processo de criação de uma proposta de arquitetura e uma visualização de dados. Para tanto, é necessário realizar a análise de requisitos, modelagem e implementação e a criação de painéis gráficos para apresentação dos indicadores. Essas etapas estão diretamente relacionados as entregas realizadas pela Equipe de Dados.
</p>
</div>
<br>
<center> <b>Figura 1: Etapas de análise de requisitos, modelagem e visualização de dados</b></center>

![**Figura 1: Etapas de análise de requisititos, modelagem e visualização de dados**](https://lh3.googleusercontent.com/pw/AP1GczNNmAcA4L8nC8bJ0z8cjO1BMhjp82_5b7XweEidL2qWxw3dbG_5RdS8EuK-DomR0F-IJOH7sLNMoaONS4t6MJYpis2qDRDRhl4D9hNu_JkFs0Q7awNvdOVhwTKVbvJnOEmcZ1Dwiji1PdYWJJCOvFSk=w2560-h940-s-no-gm?authuser=0)

<div align="justify">
<p>
A arquitetura proposta viabilizará a <b>interoperabilidade</b> entre os diversos sistemas de gestão cultural, possbilitando uma padronização da representação e transferência de informações entre os diversos <b>Agentes </b> do sistema.
</p>
</div>

# Fluxo da informação orientado à execução da PNAB

<div align="justify">A partir do levantamento de requisitos e da inter-relação com o fluxo do plano de trabalho é possível 
definir estruturas adicionais para a execução do fluxo de dados e informações relacionadas à PNAB, mapeadas baseadas no ciclo do recurso orçamentário destinado às ações culturais, sua execução e consequente prestação de informações.</p></div>
<div align="justify">
<p>
São definidos três blocos principais para a modelagem atual: (I) o repasse do recurso orçamentário, a partir do Governo Federal, (II) o refinamento e granularização de sua aplicação utilizando o Plano Anual de Aplicação de Recursos (PAAR) pelo ente federado e (III) o acoplamento ao mecanismo de acompanhamento e execução da política pública e sua consequente prestação de informações por intermédio do Mapas Culturais.
</p>
</div>

### I. Do repasse do recurso orçamentário da União
<div align="justify">
<p>
A partir das definições das frações do orçamento para cada ente beneficiário, disposto em norma legal, este deve criar um plano de ação definindo como o recurso será executado a priori. O plano de ação é composto por metas, que no escopo da PNAB são duas: Ações Gerais e Política Nacional Cultura Viva. O ente federado definirá quais os montantes serão aplicados para ações específicas, tais como fomento cultural, obras, reformas e aquisições de bens culturais, custo operacional e premiação de pontos de cultura, por exemplo. A definição dos montantes seguem os estipulados por leis específicas e suas devidas aplicações compulsórias. Na Figura 1 é apresentado um pseudo Modelo Entidade Relacionamento (MER) descrevendo o fluxo orçamentário relacionado ao TransfereGov.</p></div>

**<center>**Figura 1: Etapa de repasse do recurso da União**</center>**

![**Figura 1: Etapa de repasse do recurso da União**](https://lh3.googleusercontent.com/pw/AP1GczPNri-UDdOzKkFGI04nI2vTQgNkOU1qdcznsh0HnkUT_C-bw4O3ap7VmnbrjNDGZWopHMgQV0wx1wPad0Bxm-LwAqrEanHFTFDHXYyMP8zcJT3pPL9LdLDUe4e4E0Dy0LWzebbPGVK9SKctinypzj9U=w1516-h961-s-no-gm?authuser=0)

### II. Da granularização da aplicação dos recursos com o PAAR
<div align="justify">
<p> 
Durante a criação do plano de ação de execução dos recursos orçamentários da PNAB, é demandada a apresentação de um documento suplementar que é o PAAR.
</div></p>
<div align="justify">
<p> 
O PAAR refina a aplicação de recursos definidos nas ações do plano de trabalho. Neste caso, as ações gerais são subdivididas em fomento cultural, obras, reformas e aquisições de bens culturais, custo operacional e subsídio e manutenção de espaços e organizações culturais. Já para o Cultura Viva em fomento a projetos continuados de pontos de cultura, fomento a projetos continuados de pontões de cultura e premiação de pontos de cultura.
</div>
</p>
<div align="justify">
<p> 
As ações são subdivididas em atividades elencadas no Art. 5º da Lei 14.399/2022, podendo ser apoio a festivais, festas populares, feiras e produção de espetáculos, concessão de bolsas culturais, premiação, dentre outros (BRASIL, 2022). Também são definidos os valores associados, a forma do regime jurídico associado, a entrega, bem como suas quantidades. Tal representação/fluxo é apresentado na Figura 2.
</div>
</p>

**<center>**Figura 2: Fluxo e estruturação das informações no PAAR**</center>**
![**Figura 2: Fluxo e estruturação das informações no PAAR**](https://lh3.googleusercontent.com/pw/AP1GczMyJdfov59ltAal8WOWNkZnNZlH12Imk0OIHsWk84cMSrxe2-pd538yPUIMEPWx2KHplyNIS5RbrmH9e2MAQ2U849isC7kA8qy63cBGpDKTFTZXNNOAdc5rSLli3yP3NreOPPXI5mlvun_sTH3JmeNK=w1847-h961-s-no-gm?authuser=0)

### III. Mecanismo de acompanhamento e execução da política pública e sua consequente prestação de informações
 <div align="justify">
<p> 
A partir da definição das atividades descritas no PAAR, ouvida a sociedade civil, estes podem ser habilitados por intermédio dos instrumentos legais atinentes sejam estes chamamentos públicos, credenciamentos, licitações e contratos, por exemplo.
</p></div>

<div align="justify">
<p> 
Numa modelagem direcionada ao contexto atual, a entidade Oportunidade do Mapas Culturais acumula as funções de agregador de instrumentos de execução, na forma de Programas de Fomento, e a definição das próprias modalidades tais como fomento à execução de ações culturais, apoio a espaços culturais, concessão de bolsas culturais e concessão de premiação cultural. As Oportunidades permitem operacionalizar o fluxo do chamamento público, recebendo Inscrições, que podem ser avaliadas por uma Comissão de Avaliação. Caso a inscrição esteja conforme os critérios de elegibilidade e sendo aprovada pela comissão de avaliação, está apta a se tornar uma Iniciativa, a partir da celebração de um termo entre o ente propositor do instrumento e o agente cultural propositor da ação cultural. A modelagem preliminar associada a esta etapa intermediária é apresentada na Figura 3.
</p>
</div>

**<center>**Figura 3: Modelagem preliminar das atividades do PAAR em Iniciativas**</center>**
![**Figura 3: Modelagem preliminar das atividades do PAAR em Iniciativas**](https://lh3.googleusercontent.com/pw/AP1GczNOJveiiIARE3OV56qfQdZBXUPvhzOuP6Py7g4dF8l8pcc9tO9KL5PqLdsjvYhqcWgr0d1CIPPTrHyvaHMQgLREojpbawdU2-EYazQjZpBB4F25MvewgKhTvYm8Z64o8Xi68QySNxJgyhPiTZYAPytP=w1497-h961-s-no-gm?authuser=0)

<div align="justify">
<p> 
No caso da inscrição que seja convertida em uma Iniciativa, além dos campos gerais da proposta, também é necessária a definição de um plano de trabalho que contemple uma estrutura básica composta de uma Equipe, Orçamento, Metas e Entregas.
</p>
</div>

<div align="justify">
<p> 
As metas definem marcos físicos para a execução de uma determinada etapa, apresentando resultados tangíveis ou intangíveis como Entregas. A verificação da consecução das metas é realizada pelas Evidências. Um conjunto de recursos, sejam estes físicos (livros, CDs, DVDs, cartilhas), digitais (e-books, apresentações/gravações por intermédio de mídias digitais) ou a realização de Evento em um determinado Espaço podem ser consideradas com um dos tipos de Evidência.
</p>
</div>

<div align="justify">
<p> 
De forma a viabilizar a execução das Metas, é possível a participação de Agentes, formando assim uma Equipe. Os integrantes da Equipe têm papeis definidos no plano de trabalho, podendo sofrer alterações durante a execução dos trabalhos. A Equipe possui uma vinculação com o Orçamento, devido a necessidade de pagamentos para os integrantes.
</p>
</div>

<div align="justify">
<p> 
O Orçamento trata da discriminação dos itens que terão uma componente financeira no projeto, demonstrando a sua execução. Pode apresentar uma estrutura com o descritivo, quantidade e valores associados a cada elemento, sejam itens de custeio ou de capital, tais como a compra de bens ou prestação de serviço. Na Figura 4 é apresentada uma representação preliminar de uma proposta de plano de trabalho.
</p>
</div>

**<center>**Figura 4: Plano de trabalho e plano de trabalho associado**</center>**

![Projeto Fomentado e seu plano de trabalho](https://lh3.googleusercontent.com/pw/AP1GczOp-T0RivFOgoawTgCY7G3kF2YrcA4mhDMpl7CD1l3HlAfzytrz-LkBLN5ZGZxyTIUcenOsZ4Csyk9vTlov-Wbi0uL4qMrSDqDWk_FqmhOuJg4xKTbr8T3RrHafmNNrcP5bqpX6WlDXt8rdDPrnSDoR=w1744-h961-s-no-gm?authuser=0)

<div align="justify">
<p> 
Para que seja possível realizar o monitoramento da execução dos recursos públicos se faz necessária a prestação de informações.
</p>
</div>

<div align="justify">
<p> 
A interface de prestação de informações permite que o Agente recebedor do recurso público informe ao ente não só a utilização do recurso financeiro descrito no Orçamento mas da consecução das Metas contidas no Plano de Trabalho.
</p>
</div>

<div align="justify">
<p> 
A partir da verificação das entregas realizadas pelo Agente, por intermédio das Evidências e Indicadores extraídos do Plano de Trabalho, é possível acompanhar a execução da proposta, tanto de forma parcial como uma entrega total por parte do Agente. Independente do estágio da prestação, é facultado ao ente a solicitação de complementação de informações por parte do Agente, demandando a apresentação de explicação ou Recurso. Dependendo da análise do Ente, este pode avaliar o relatório como Aprovado ou Reprovado. Caso a execução seja realizada com êxito, o projeto tem associado um Termo de Encerramento, evidenciando a completa execução ou sua execução com ressalvas aprovadas, sem ônus para o Agente. Tal modelo preliminar pode ser verificado na Figura 5.
</p>
</div>

**<center>**Figura 5: Proposta de modelo preliminar para a prestação de informações relacionadas ao Plano de Trabalho.**</center>**
![**Figura 5: Proposta de modelo preliminar para a prestação de informações relacionadas ao Plano de Trabalho.**](https://lh3.googleusercontent.com/pw/AP1GczNVudkwHkzvfmfia2nw1d7HP74yusjVgMj21OkwC6FsgNqvOHztErhZqwUJkUt3oet4W4rTAsa7ffmhID9vZazuws06vXqhURpHpj3KspixWdbNOdAtpLELyZExCzQj7OEtGxFaAUAO5fB17KR_UXLf=w1351-h961-s-no-gm?authuser=0)


# Dicionário de Dados

<div align="justify">
<p>
O <b>Dicionário de Dados</b> descreve, de forma estruturada, as entidades da PNAB e seus respectivos atributos. Na Figura X é descrita a composição de um dicionário de dados.
</p>
</div>

![**Figura X: Composição do dicionário de dados.**](https://static.observableusercontent.com/files/a0edc0b7c5999c55542a387e65964c7cca08eb9ed4e56852bd47432facad70477578132ac7fb78e15130728c59250f0bd276d455eb10baea883393b794ff81fe)

Na Tabela 1 é apresentado o dicionário de dados relacionado a tabela Pessoa (Agente).

|          Campo         |                 Descrição                |                                                                              Valores possíveis                                                                              |         Tipo de variável        | Dado sensível |
|:----------------------:|:----------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:-------------------------------:|:-------------:|
| cpf                    | CPF da Pessoa                            |                                                                                                                                                                             | Texto (qualitativa nominal)     | Sim           |
| email                  | Email da Pessoa                          |                                                                                                                                                                             | Texto (qualitativa nominal)     | Não           |
| nome_completo          | Nome completo da pessoa                  |                                                                                                                                                                             | Texto (qualitativa nominal)     | Sim           |
| cod_mun                | Código do IBGE da cidade da Pessoa       |                                                                                                                                                                             | Inteiro (Quantitativa discreta) | Não           |
| cep                    | CEP vinculado ao endereço                |                                                                                                                                                                             | Texto (qualitativa nominal)     | Sim           |
| selo_pnab              | Selo de verificação de participação      | tipos_de_selos_pnab                                                                                                                                                         | Texto (qualitativa nominal)     | Não           |
| nome_social            |                                          |                                                                                                                                                                             | Texto (qualitativa nominal)     | Sim           |
| nome_perfil            | Como a pessoa quer ser chamada (Apelido) |                                                                                                                                                                             | Texto (qualitativa nominal)     | Sim           |
| data_nascimento        | Data de Nascimento da Pessoa             | formato: “dia/mes/ano” : “dd/mm/yyyy”                                                                                                                                       | Data                            | Sim           |
| escolaridade           | Escolaridade do Agente Cultural          | Níveis de instrução de acordo com o IBGE - Tabela 7128                                                                                                                      |                                 | Sim           |
| sexo                   | Sexo do Agente                           | Feminino;Masculino;Intersexo;Sem declaração.                                                                                                                                | Texto (qualitativa nominal)     | Sim           |
| genero                 | Gênero                                   | Cisgênero;Transgênero;Pessoa não-binária;Outro;Sem declaração.                                                                                                              | Texto (qualitativa nominal)     | Sim           |
| orientacao_sexual      |                                          | Grupo considerado pelo IBGE                                                                                                                                                 | Texto (qualitativa nominal)     | Sim           |
| quilombola             | Pessoa Quilombola?                       | Sim; Não; Não informado,                                                                                                                                                    | Texto (qualitativa nominal)     | Sim           |
| indigena               | Pessoa indígena                          | Sim; Não; Não informado,                                                                                                                                                    | Texto (qualitativa nominal)     | Sim           |
| comunidade_tradicional | Povos                                    |                                                                                                                                                                             | Texto (qualitativa nominal)     | Sim           |
| pessoa_com_deficiencia | Pessoa com Deficiência - PCD             | Não; Sim, Auditiva; Sim, Física-motora; Sim, Intelectual; Sim, Múltipla; Sim, Visual; Sim, Transtorno do Espectro Autista; Sim, Outra;                                      | Texto (qualitativa nominal)     | Sim           |
| faixa_renda            | Renda média individual                   | 1,00 a 500,00 501,00 a 1.000,00 1.001,00 a 2.000,00 2.001,00 a 3.000,00 3.001,00 a 5.000,00 5.001,00 a 10.000,00 10.001,00 a 20.000,00 20.001,00 a 100.000  100.001 ou mais | Texto (qualitativa nominal)     | Sim           |
| cor_raca               | Cor ou Raça da Pessoa                    | 5 grupos, segundo IBGE / Tabela 9605 - População residente, por cor ou raça, nos Censos Demográficos: 
Branca; Preta; Amarela; Parda; Indígena.                             | Texto (qualitativa nominal)     | Sim           |



# Painéis de Dados
Os **Painéis de Dados** são projetados para oferecer uma visão pública das entidades e dicionários da PNAB. Estes painéis fornecerão indicadores e visualizações agregadas, garantindo a proteção dos dados pessoais, conforme as diretrizes de privacidade.
