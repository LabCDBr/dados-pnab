# Dicionários de dados das Entidades PNAB

Nesta seção, o repositório apresenta os dicionários de dados associados a cada entidade destacada no [MER PNAB](2_2_2_MER_Entidades.md). 

Em resumo, os dicionários definem quais são e o que significam cada característica (ou atributo) associado a uma entidade. Ou seja, **descreve como cada entidade deve ser representada** em um sistema que implemente o padrão de dados PNAB. 

A figura a seguir ilustra a estrutura proposta para cada dicionário PNAB, que possui:

- **Descrição breve da entidade**: Um resumo sobre o que a entidade representa no contexto da PNAB.
  
- **Lista de Atributos**: Cada entidade é descrita por uma tabela de atributos que inclui o **Nome**, **Descrição**, **Tipo** e **Valores possíveis**. Essa estrutura facilita a consulta e a compreensão dos dados.

- **Consulta SQL**: Para cada entidade, o dicionário fornece uma consulta SQL que pode ser utilizada no sistema **Mapas Culturais** para extrair os dados correspondentes.


![**Figura X: Composição do dicionário de dados.**](https://static.observableusercontent.com/files/a0edc0b7c5999c55542a387e65964c7cca08eb9ed4e56852bd47432facad70477578132ac7fb78e15130728c59250f0bd276d455eb10baea883393b794ff81fe)

*É importante destacar que pequenas variações de taxonomia podem ser administradas durante os fluxos de compartilhamento de informações entre o ministério e o conjunto de entes federados - e seus respectivos sistemas, com base neste padrão de dados.  

# Lista de Dicionários do padrão de dados PNAB

- [Pessoas]() e [Organizações]() - Agentes Culturais e entes federados estão contidos nesta definição;
- [Iniciativas]() - É importante destacar que existem subtipos desta entidade, como Programas PNAB, Programa de Fomento, Projeto Fomentado, dentre outros);
- [Oportunidades]()
- [Inscrição](), [Plano de Trabalho](), [Metas](), [Atividades]() e [Entregas]() - Entidades relacionadas às Ações Culturais submetidas via inscrição ou em execução;
- [Relatórios](), 
- [Eventos]() e [Espaços]().
