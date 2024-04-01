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

A escola Infinito necessita de um sistema de presença novo pois o atual é feito em papel.

# Análise de Requisitos Funcionais e Não-Funcionais
**Requisitos Funcionais**
  - Professores vão registrar a falta de forma intuitiva
  - A falta vai ser registrada em dois momentos: no início das aulas e após o retorno do intervalo
  - Gerar relatórios das faltas
  - Enviar notificações via email

**Requisitos Não-Funcionais**
  - Acessibilidade
  - Acesso a partir de qualquer dispositivo

# Diagrama de Atividades

![MACK Eng  de Softw  - Diagrama de Atividades](https://github.com/gabrielyin/UML-Classroom-FCI/assets/116746646/c0b5f5fe-5617-4410-acf1-099b27172a7c)


# Diagrama de Casos de Uso

![image](https://github.com/gabrielyin/UML-Classroom-FCI/assets/70323043/d0981966-f4bb-4ddb-b0e8-55fa3ea38fdb)

# Descrição dos Casos de Uso

### Caso de Uso: Lançar faltas

| Nome do Caso de Uso | Lançar faltas |
|---------------------|---------------|
| Ator Principal      | Professor     |
| Atores Secundários  | Sistema       |
| Resumo              | Este caso de uso descreve as etapas percorridas por um professor para lançar as faltas dos alunos. |
| Pré-condições       | O professor precisa ter uma conta criada |
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
| Restrições e Validações | |
| | 1. Somente professores podem lançar as faltas |
| | 2. A chamada deve ser feita no início e no final da aula |

### Caso de Uso: Efetuar Cadastro

| Nome do Caso de Uso | Efetuar Cadastro |
|---------------------|-----------------|
| Ator Principal      | Professor       |
| Atores Secundários  | Sistema         |
| Resumo              | Este caso de uso vai descrever as etapas percorridas por um professor para efetuar o cadastro. |
| Pós-condições       | Possuir uma conta criada |
| Fluxo Principal     | |
| Ações do Ator       | Ações do Sistema |
| 1. Entrar na página de cadastro dos professores | |
| | 2. Sistema vai pedir email e senha do professor |
| 3. Professor vai inserir seus dados | |
| | 4. Sistema vai verificar se o professor é um professor de uma instituição e criar a conta no banco de dados |
| 5. Professor recebe uma confirmação da criação da conta e entra na plataforma | |
| Restrições e Validações | |
| | 1. Somente professores da instituição podem criar uma conta |

### Caso de Uso: Efetuar Login

| Nome do Caso de Uso | Efetuar Login |
|---------------------|---------------|
| Ator Principal      | Professor     |
| Atores Secundários  | Sistema       |
| Resumo              | Este caso de uso vai descrever as etapas percorridas por um professor para efetuar o login na plataforma. |
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

| Nome do Caso de Uso | Efetuar Login |
|---------------------|---------------|
| Ator Principal      | Professor     |
| Atores Secundários  | Sistema       |
| Resumo              | Este caso de uso vai gerar as métricas de acordo com os parâmetros selecionados. |
| Pré-condições       | O professor precisa ter uma conta criada |
| Fluxo Principal     | |
| Ações do Ator       | Ações do Sistema |
| 1. Professor acessa a área de gerar relatórios | |
| | 2. Sistema apresenta se quer ver o relatório de forma individual ou coletiva |
| 3. Professor escolhe a forma que prefere | |
| | 4. O sistema mostrar os dados a paritr das opções selecionadas |
| Restrições e Validações | |
| | 1. Professor deve possuir uma conta no sistema |


### Caso de Uso: Enviar E-mail

| Nome do Caso de Uso | Efetuar Login |
|---------------------|---------------|
| Ator Principal      | Sistema     |
| Atores Secundários  | Professor       |
| Resumo              | Este caso de uso vai enviar uma notificação por e-mail para os responsáveis dos alunos que tenham a presença menor que 80% |
| Fluxo Principal     | |
| Ações do Ator       | Ações do Sistema |
| 1. Professor acessa a área de lançar faltas e faz a chamada | |
| | 2. Verifica ao final, quais alunos estão com presença menor do que 80% e envia os e-amils |
| Restrições e Validações | |
| | 1. Professor deve possuir uma conta no sistema |
| | 2. Deve ter tido aula até o momento |


# Diagrama de Sequência

*&lt;Diagrama de ordem e interação dos objetos&gt;*

# Diagrama de Classes

*&lt;Diagrama de relacionamento entre classes para os seus atributos e operações&gt;*

# Diagrama de Estados

*&lt;Diagrama para permite modelar o comportamento interno de um determinado objeto, subsistema ou sistema global&gt;*

# Diagrama de Implantação

*&lt;Diagrama para exibir o relacionamento de hardware e software no projeto&gt;*

# Referências

*&lt;Lista de referências&gt;*
