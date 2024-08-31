## Detalhamento de criação do Star Schema para o desafio de projeto.

##Criação das Tabelas.
1 - A Partir da tabela Financial foram criadas outras 6 Tabelas para o modelo Star Schema,
	sendo 1 tabela Fato e 5 tabelas Dimencional.
	*D_Produto
		Na tabela D_Produtos, foi altera para expor 6 informações com base no nome do produto que são:
		- Congagem de unidade vendida.
		- Valor minimo do preço de vendas.
		- Valor maximo do preço de Vendas.
		- Valor médio do preço de vendas.
		- A mediana do preço de vendas.
		- Media do preço de manofatura.
	*D_Desconto
		Na tabela D_Desconto, foi criada uma coluna condicional a partir do nome do produto onde para
		gerar o id_do_produto com base no nome do produto. E após a criação a coluna "Product" foi excluida.
		- id 0:Produto("Carretera")
		- id 1:Produto("Montana")
		- id 2:Produto("Paseo")
		- id 3:Produto("Velo")
		- id 4:Produto("VTT")
		- id 5:Produto("Amarilla")
		Obs: caso contrario o valor da coluna ficara "null".
	*D_Detalhes_Produto
		Na tabela Detalhe_Produto, foi criado uma coluna indice a partir de 0, 
		e mantida apenas as informações abaixo:
		- Discont Band
		- Units Sold
		- Manufacturing Price
		- Sale Price
	*D_Detalhes
		Na Tabela Detalhes, foram removidas 3 colunas referentes a descontos
	*F_Venda
		Na tabela Vendas, Foram removidas as colunas("Manufacturing Price", "Gross Sales", "Discounts", "COGS", "Month Number"),
		criadas as colunas de ID_Produto(id_do_produto com base no nome do produto) e SK_ID(Coluna Indice).
		
		
	
2 - Ja a tabela D_Calendario, foi criada atraves da função DAX.
	* D_Calendario
	 A tabela Calendario foi criada uma nova tabela e as colunas criadas conforme as funçoes DAX abaixo.
	 - Date: criada com a função:"CALENDAR(DATE(2013, 9, 1), DATE(2014, 12, 1))"
	 - Month Name:FORMAT(Calendar[Date], "MMMM")
	 - Year:YEAR(Calendar[Date])
	 - Day of Week:FORMAT(Calendar[Date], "dddd")