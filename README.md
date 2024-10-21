
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

### 2.0 Como este repositório está organizado?
####  2.1 Fluxo da Informação relacionada à PNAB
##### 2.1.1 Análise do ecossistema de soluções digitais, com foco no Mapas Culturais (extensão daquele doc Análise da taxonomia)
##### 2.1.2 Análise do fluxo de execução orçamentária da PNAB, mapeando integrações com TranfereGov e com o Plano Anual de Aplicação de Recursos - PAAR
##### 2.1.3 Proposta e formulação de uma atualização Mapas para a PNAB
####  2.2 Modelagem Entidade Relacionamento - MER
##### 2.2.1 O que é um MER?
##### 2.2.2 O MER PNAB
####  2.3 Relação das Entidades e seus Dicionários de dados
####  2.4 Análise exploratória utilizando Painéis de Dados
### 3.0 Referencial normativo/legal utilizado