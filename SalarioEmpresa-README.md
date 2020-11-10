# igti_bootcamp
Meu código para solucionar Desafio 2 do Módulo 1 do Bootcamp de Programador de Software Iniciante do IGTI.

Enunciado do desafio:

O desafio consiste em desenvolver funções em JavaScript para realizar alguns processamentos em cima de uma lista de funcionários de uma empresa.
Cada funcionário é representado pelas seguintes informações:
- Nome: nome do funcionário.
- Salário: salário do funcionário.
- Setor: setor da empresa que o funcionário trabalha.
A lista de funcionários será fornecida em um arquivo chamado funcionarios.json, juntamente com o enunciado deste trabalho.
Segue abaixo um exemplo da estrutura deste arquivo:
    {
    "funcionarios": [
    {
    "nome": "João Silva",
    "salario": 1000,
    "setor": "Administrativo"
    },
    {
    "nome": "João Silva",
    "salario": 2000,
    "setor": "Produção"
    }
    ]
    }
O aluno poderá ler o arquivo pelo programa a ser desenvolvido, ou senão criar uma variável dentro do programa já com os dados fornecidos, não sendo então obrigatório o processo de leitura do arquivo.
Segue abaixo a descrição das funções a serem desenvolvidas:
  1) Função que retorna o nome do funcionário que tem o maior salário da empresa.
  2) Função que retorna o nome do funcionário que tem o menor salário da empresa.
  3) Função que retorna a média salarial da empresa.
  4) Função que recebe um setor como parâmetro e retorna o funcionário de maior salário do setor informado.
  5) Função que recebe um setor como parâmetro e retorna o funcionário de menor salário do setor informado.
  6) Função que recebe um setor como parâmetro e retorna a média salarial do setor informado.
Lembrando que a média é calculada a partir da soma dos valores e dividindo pela quantidade. Por exemplo, se em um setor temos três funcionários com salários de 1000, 2000 e 3000, a média seria calculada somando 1000 + 2000 + 3000, e dividindo o resultado por 3, obtendo assim 2000 de média.
O aluno pode, caso queira, agrupar vários destes itens em uma mesma função, utilizando parâmetros para diferenciar a ação a ser realizada. Fica a critério do aluno a quantidade de funções a serem criadas, desde que todos os processamentos solicitados sejam contemplados.
O resultado das funções pode ser impresso no próprio terminal, ou senão mostrados em uma página web; este quesito fica como opcional. O aluno deverá utilizar estas saídas para responder o questionário de validação.
