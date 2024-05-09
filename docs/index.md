<h2><a href= "https://www.mackenzie.br">Universidade Presbiteriana Mackenzie</a></h2>
<h3><a href= "https://www.mackenzie.br/graduacao/sao-paulo-higienopolis/sistemas-de-informacao">Sistemas de Informação</a></h3>


<font size="+12"><center>
Sistema de Presença escola INFINITO
</center></font>

>*Observação 1: A estrutura inicial deste documento é só um exemplo. O seu grupo deverá alterar esta estrutura de acordo com o que está sendo solicitado na disciplina.*

>*Observação 2: O índice abaixo não precisa ser editado se você utilizar o Visual Studio Code com a extensão **Markdown All in One**. Essa extensão atualiza o índice automaticamente quando o arquivo é salvo.*

**Conteúdo**

- [Autores](#nome-alunos)
- [Descrição do Projeto](#introdução-do-projeto)
- [Análise de Requisitos Funcionais e Não-Fucionais](#descrição-dos-requisitos)
- [Diagrama de Atividades](#diagrama-de-atividades) 
- [Diagrama de Casos de Uso](#diagrama-de-comportamento-atores)
- [Descrição dos Casos de Uso](#descrição-das-funcões)
- [Diagrama de Senquencia](#diagrama-de-ordem-interações)
- [Diagrama de Classes](#diagrama-orientado-objetos)
- [Diagrama de Estados](#diagrama-estrutura-componente)
- [Diagrama de Implantação](#diagrama-de-hardware-software)
- [Referências](#referências)


# Autores

* Gabriel Shihao Chen Yin
* Pedro Pessuto Ferreira
* Andrea Tessler


# Descrição do Projeto

  O projeto consiste no desenvolvimento de um sistema de controle de presença para a Escola Infinito, que atualmente faz esse controle de forma manual. O sistema permitirá que os professores registrem faltas de forma intuitiva em dois momentos do dia, gere relatórios das faltas e envie notificações por e-mail aos responsáveis quando a porcentagem de comparecimento às aulas estiver abaixo de 80%.
  Para atender as necessidades da escola é preciso criar um sistema que inclua as turmas do 1º ao 5º ano do Ensino Fundamental, cada uma com vários alunos (geralmente entre 20 e 30). Cada turma possui um professor principal que ministra a maior parte das aulas e outros professores para matérias específicas. A chamada é realizada todos os dias pelos professores em dois momentos: no início das aulas do dia e logo após o retorno do intervalo. Um estudante precisa ter comparecido a pelo menos 75% do total de aulas do ano para não ser reprovado por faltas.

# Análise de Requisitos Funcionais e Não-Funcionais
**Requisitos Funcionais**
  - Plataforma: permita que a mesma plataforma comporte diferentes tipos de cargos
  - Registro de faltas: permitir que professores registrem faltas de forma fácil e intuitiva.
  - Relatórios de faltas: gerar relatórios de faltas agrupados por data, ano do ensino, turma, professor disciplina ou aluno, para facilitar a análise e o acompanhamento do número de faltas.
  - Notificações: enviar notificações por e-mail aos pais ou responsáveis quando a porcentagem de comparecimento às aulas estiver abaixo de 80%.

**Requisitos Não-Funcionais**
  - Acessibilidade: garantir que o sistema seja acessível a todos os usuários, incluindo pessoas com deficiências, com recursos de acessibilidade como tamanho de fonte ajustável.
  - Acesso a partir de qualquer navegador web, inclusive em dispositivos móveis.Acessibilidade

# Diagrama de Atividades

![MACK Eng  de Softw  - Diagrama de Atividades (Copy)](https://github.com/gabrielyin/UML-Classroom-FCI/assets/116746646/ed4527fe-7324-4be8-a972-55983cc8a85b)

# Diagrama de Casos de Uso

![Diagrama de Casos de Uso - Diagrama de caso de uso](https://github.com/gabrielyin/UML-Classroom-FCI/assets/116746646/b1d5f9d7-4388-41a8-be75-b154ceaa600e)


# Descrição dos Casos de Uso

### Caso de Uso: Lançar faltas

| Nome do Caso de Uso | Lançar faltas |
|---------------------|---------------|
| Ator Principal      | Professor     |
| Atores Secundários  | Sistema       |
| Resumo              | Este caso de uso descreve as etapas percorridas por um professor para lançar as faltas dos alunos. |
| Pré-condições       | O professor precisa ter uma conta criada |
| Pós-condições       | Atualizar faltas no sistema |
| Fluxo Principal     | |
| Ações do Ator       | Ações do Sistema |
| 1. Professor acessa a área de lançar faltas no sistema | |
| | 2. Sistema apresenta as matérias das escolas |
| 3. Professor escolhe a sua matéria | |
| | 4. Sistema pergunta o horário e dia da aula |
| 5. Professor insere a data e o horário da aula | |
| | 6. Sistema mostra uma tabela com todas os alunos para o professor marcar as faltas |
| 7. Professor faz a chamada e marca os alunos que faltaram | |
| | 8. Sistema recebe todas as faltas dos alunos e salva esses dados no banco de dados |
| | 9. Sistema verifica quais alunos estão com a taxa de faltas maior que o permitido |
| | 10. Sistema envia as notificações por e-mail dos pais |
| 11. Pais recebem a notificação (ator: Pais) | |
| Restrições e Validações | |
| | 1. Somente professores podem lançar as faltas |
| | 2. A chamada deve ser feita no início e no final da aula |

### Caso de Uso: Efetuar Login

| Nome do Caso de Uso | Efetuar Login |
|---------------------|---------------|
| Ator Principal      | Professor     |
| Atores Secundários  | Sistema       |
| Resumo              | Este caso de uso vai descrever as etapas percorridas por um professor para efetuar o login na plataforma. |
| Pré-condições       | O professor precisa ter uma conta criada |
| Pós-condições       | Verificar usuário |
| Fluxo Principal     | |
| Ações do Ator       | Ações do Sistema |
| 1. Professor acessa a página do login | |
| | 2. Sistema pede a senha e o email do professor |
| 3. Professor insere o seu email e a sua senha | |
| | 4. O sistema verifica se esses dados do professor são válidos e retorna uma resposta adequada |
| 5. Depois do sistema validar e confirmar os dados do professor ele é liberado na plataforma | |
| Fluxo Alternativo   | |
| Ações do Ator       | Ações do Sistema |
| 1. Professor esqueceu ou quer alterar a senha | |
| | 2. Sistema confirma o email do professor enviando o código |
| 3. Professor digita o código enviado no email para poder alterar a senha | |
| | 4. O sistema pede para o professor digitar uma nova senha |
| 5. Professor digita a nova senha | |
| | 6. Sistema atualiza a nova senha no banco de dados e libera o acesso para o professor |
| Restrições e Validações | |
| | 1. Professor deve possuir uma conta no sistema |

### Caso de Uso: Gerar Relatório

| Nome do Caso de Uso |  Gerar Relatório |
|---------------------|---------------|
| Ator Principal      | Professor     |
| Atores Secundários  | Sistema       |
| Resumo              | Este caso de uso vai gerar as métricas de acordo com os parâmetros selecionados. |
| Pré-condições       | O professor precisa ter uma conta criada |
| Pós-condições       | Mostrar relatório com gráficos e estatísiticas dos dados |
| Fluxo Principal     | |
| Ações do Ator       | Ações do Sistema |
| 1. Professor acessa a área de gerar relatórios | |
| | 2. Sistema apresenta se quer ver o relatório de forma individual ou coletiva |
| 3. Professor escolhe a forma que prefere dentro das opções: Individual —> Selecionar aluno ou Coletivo —> Selecionar anos (todos ou específicos)  —> Selecionar turmas (todas ou específicas)  —> Selecionar matérias (todas ou específicas) | |
| | 4. O sistema mostrar os dados a paritr das opções selecionadas  |
| Restrições e Validações | |
| | 1. Professor deve possuir uma conta no sistema |

# Diagrama de Sequência

Professor
Sistema 
Pais


Loop	

Fazer login
Validar usuario e senha 
Registrar faltas
Verificar taxa de faltas

Enviar email aos pais


Pedir relatorio


Gerar Relatorio

# Diagrama de Classes

*&lt;Diagrama de relacionamento entre classes para os seus atributos e operações&gt;*

# Diagrama de Estados

*&lt;Diagrama para permite modelar o comportamento interno de um determinado objeto, subsistema ou sistema global&gt;*

# Diagrama de Implantação

*&lt;Diagrama para exibir o relacionamento de hardware e software no projeto&gt;*

# Referências

*&lt;Lista de referências&gt;*
