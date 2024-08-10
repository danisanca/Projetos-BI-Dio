1°:Criada uma instancia na Azure.
2°: Banco de dados alimentado com informações a serem trabalhadas.
3°:Conexão Power Bi com instancia na Azure.
4°:Extração dos dados da Azure.
5°:Transformação dos dados.
 - Cabeçalhos OK
 - Ajustado os tipo de dados das colunas para os padroes corretos.
 - Foi atribuido um gerente para Lname "Wallace" que era um null via alteração no Banco de Dados..
 - E o outro null Lname "Smith" foi atribuido como "CEO" via alteração no Banco de Dados.
 - Coluna de enredeço reorganizada e a informação do estado foi criada uma coluna unica.
 - Nome do departamento adicionado a tabela employee via "Mesclar consultas"
 - Deptartamento Location mesclado com departmento para atribuir localização ao departamento.
 - P Location mesclado com departmento. Diferenciar as localizações por departamento.
 - Colunas desnecessarias removidas.
 - Mesclado a coluna do numero do projeto do works_on com o nome do projeto da tabale Project

 
->  Analisar o numero de horas por projeto.
 
## - Perguntas

### 1° Pergunta: O que é mesclar consulta:
		Trazer a tabela como um todo em uma nova coluna ja parametrizada a partir de um "id" especifico entre as duas. 
		 Quando marcamos para trazer via mescla ja associamos as informações de acordo com o valor especifico da coluna da tabela principal.	-
### 2° Perguntas: Combinar consulta:
		Realiza uma mesca entre as tabelas onde a tabela que sera mesclada a principal é incluida como um todo e os valores ficam totalmente separado,
		mesmo dentro da tabela principal haver correlação.
 	-
### 3° Perguntas: Por que Mesclar e nao combinar?:
	- Por que quando é feita a mescla é possivel trazer um dado especifico a partir de um id de uma coluna. Assim quando combinamos os id entre as tabelas,
	é possivel pegar apenas a informação desejada para atribuir a tabela principal.