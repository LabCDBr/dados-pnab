
# Repositório Público da Arquitetura de Dados da **Política Nacional Aldir Blanc de Fomento à Cultura (PNAB)**



## Apresentação


A **Política Nacional Aldir Blanc de Fomento à Cultura (PNAB)** é uma política federativa que repassa recursos do Governo Federal para estados e municípios, promovendo o fomento à cultura em todo o Brasil. O apoio financeiro é direcionado a agentes culturais, como artistas, músicos e pesquisadores, mas a diversidade de soluções digitais utilizadas pelos entes federados – desde sistemas robustos até processos manuais – torna desafiadora a avaliação unificada e transparente dos impactos da política.

Este repositório compreende a documentação de uma Arquitetura de Dados para a PNAB, incluindo uma Modelagem Entidade-Relacionamento (MER), padrões, dicionários e painéis de dados. Além disso, oferece orientações e propostas para interoperabilidade no ecossistema de soluções digitais que executam essa política pública. O objetivo é integrar os dados culturais gerados por estados e municípios, promovendo uma avaliação transparente e eficiente, tanto para gestores quanto para a sociedade civil.

Este repositório compreende alguns dos produtos do projeto **Qualificação do Ecossistema de Soluções Digitais para Mapeamento e Gestão Cultural**, no âmbito do Termo de Execução Descentralizada (TED) **00000**, firmado entre o Ministério da Cultura (MinC) e a Fundação da Universidade Federal do Paraná (FUNPAR). As pessoas diretamente envolvidas na consolidação deste repositório são:

- **Alexandre Cajazeira** e **Elliott Chaves** - Cientistas de Dados (UFPR) - Modelagem e Desenvolvimento dos produtos de dados do TED;
- **Uirá Porã** - Analista de Negócio (UFPR) - Supervisão Técnica;
- **Sofia Mettenheim** e **Juliana Almeida** (SGE/MinC) - Gestão e Acompanhamento.

A proposta de **Arquitetura de Dados** aqui apresentada é fundamental para a padronização e integração dos sistemas. Ela busca garantir que todas as plataformas de gestão cultural compartilhem um modelo de dados comum, permitindo análises mais precisas e centralizadas. O sistema Mapas Culturais foi utilizado como base para a arquitetura proposta, pois constitue uma plataforma consistente e robusta para a execução da política. Além disso, a interação entre sistemas e etapas de gestão orçamentária foi contemplada, envolvendo o **TransfereGov** e o **Plano Anual de Aplicação de Recursos (PAAR)**. 

A criação desta arquitetura segue etapas de análise de requisitos, modelagem e implementação de soluções digitais, além da elaboração de painéis para visualização de indicadores culturais, oferecendo uma base sólida para o monitoramento eficiente da política pública. A figura a seguir ilustra este processo.

<center> <b>Figura 1: Fluxo de atividades relacionadas aos produtos descritos neste repositório.</b></center>

![**Figura 1: Etapas de análise de requisititos, modelagem e visualização de dados**](https://lh3.googleusercontent.com/pw/AP1GczNNmAcA4L8nC8bJ0z8cjO1BMhjp82_5b7XweEidL2qWxw3dbG_5RdS8EuK-DomR0F-IJOH7sLNMoaONS4t6MJYpis2qDRDRhl4D9hNu_JkFs0Q7awNvdOVhwTKVbvJnOEmcZ1Dwiji1PdYWJJCOvFSk=w2560-h940-s-no-gm?authuser=0)


## Como este repositório está dividido? 

A **[seção 2.1](2_1_Fluxo_Informacao_PNAB.md)** explora o fluxo de informações da PNAB, adotando uma abordagem top-down. Foi realizada uma análise do conjunto normativo relacionado à política, uma análise do ecossistema de soluções digitais, com foco no sistema Mapas Culturais e, em seguida, uma análise do fluxo de execução orçamentária, mapeando possíveis integrações com o *TransfereGov* e o *Plano Anual de Aplicação de Recursos (PAAR)*. A **[seção 2.2](2_2_1_MER_Definicao.md)** explora o conceito de Modelagem Entidade Relacionamento (MER) e apresenta o MER PNAB, constituindo uma perspectiva simples e direta do fluxo de informações da política para que diferentes sistemas possam implementar o padrão de dados. A seguir, a **[seção 2.3](2_3_Entidades_Dicionarios.md)** compreende um dicionário de dados para cada entidade PNAB, destacando as características e atributos fundamentais ao padrão de dados e à interoperabilidade. Por fim, a **[seção 2.4](2_4_Analise_paineis_dados.md)** explora o tratamento e análise dos dados a partir do padrão proposto, documentando possíveis painéis de indicadores e orientações para visualização e disponibilização do conjunto de dados PNAB. O referencial normativo/legal utilizado na construção deste repositório está listado ao final deste documento, como também nos documentos e recursos disponíveis em cada seção.


Acesse e confira a documentação disponível para cada componente deste repositório: 

###  [2.1 Fluxo da Informação relacionada à PNAB baseado em uma abordagem Top-Down](2_1_Fluxo_Informacao_PNAB.md)
#### [2.1.1 Análise do ecossistema de soluções digitais, com foco no Mapas Culturais](2_1_1_Analise_Ecossistema.md)
#### [2.1.2 Análise do fluxo de execução orçamentária da PNAB, mapeando integrações com TranfereGov e com o Plano Anual de Aplicação de Recursos - PAAR](2_1_2_TransfereGov_PAAR.md)
#### [2.1.3 Proposta e formulação de uma atualização Mapas para a PNAB](2_1_3_Proposta_PNAB_Mapas.md)
###  [2.2 Modelagem Entidade Relacionamento - MER]()
#### [2.2.1 O que é um MER?](2_2_1_MER_Definicao.md)
#### [2.2.2 O MER PNAB](2_2_2_MER_Entidades.md)
###  [2.3 Relação das Entidades e Dicionários de dados PNAB](2_3_Entidades_Dicionarios.md)
###  [2.4 Painéis de Dados PNAB](2_4_Analise_paineis_dados.md)
### 3 Referencial normativo/legal utilizado

Durante a construção deste documento, foram consideradas as seguintes publicações:

- [**Lei nº 14.399 de 08 de julho de 2022**](https://www.planalto.gov.br/ccivil_03/_ato2019-2022/2022/lei/l14399.htm), que institui a Política Nacional Aldir Blanc de Fomento à Cultura (PNAB);
- [**Decreto nº 11.740 de 18 de outubro de 2023**](https://www.planalto.gov.br/ccivil_03/_ato2023-2026/2023/decreto/D11740.htm), que regulamenta a PNAB;
- [**Lei Paulo Gustavo (Lei Complementar nº 195/2022)**](https://www.gov.br/secom/pt-br/acesso-a-informacao/comunicabr/lista-dos-programas/lei-paulo-gustavo);
- [**Instrução Normativa Nº 6**](https://www.gov.br/cultura/pt-br/assuntos/noticias/entenda-quais-indicadores-vao-nortear-o-monitoramento-da-execucao-da-lpg), publicada pelo MinC em 23 de agosto de 2023;
- **Relatório TR nº 9452 - OEI/BRA/22/002 - MTUR**, [Padronização de Taxonomias do Fomento Direto à Cultura](https://github.com/LabCDBr/gestao/files/15473883/17MAIO2024_Relatorio.2_OEI.MinC_FINAL.ENVIADO.docx.pdf);
- [**Marco Regulatório do Fomento à Cultura**](https://www12.senado.leg.br/noticias/materias/2024/06/04/marco-regulatorio-para-financiamento-da-cultura-segue-para-sancao), aprovado no Senado Federal em 04 de junho de 2024;
- [**Publicações e documentações da plataforma Mapas Culturais**](https://mapas.tec.br/).

