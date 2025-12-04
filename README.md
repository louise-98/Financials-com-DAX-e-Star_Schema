# Projeto Financials com DAX e-Star Schema no Power BI

Uso da tabela Financial Sample para criar as tabelas dimensão e fato, usar a DAX, além de um modelo baseado em Star Schema.

## ETAPAS DO PROJETO:

## POWER QUERY:

### 1)	Tabela Financials
a.	Renomear tabela financials para Financials_origem.

### 2)	Tabela D_Produtos
a.	Criar a tabela D_Produtos a partir da duplicação da tabela Financials_origem
b.	Criar coluna ID_Produto a partir da “Coluna Condicional”. Em seguida, movê-la para a extrema esquerda.
c.	Apagar colunas desnecessárias.
d.	Retirar linhas repetidas em “Remover Duplicadas”.
e.	Adicionar colunas calculadas através de “Agrupar por”.  

### 3)	Tabela D_Produtos_Detalhes
a.	Criar a tabela D_Produtos_Detalhes a partir da duplicação da tabela Financials_origem
b.	Criar coluna ID_Produtos a partir da “Coluna Condicional”. Em seguida, movê-la para a extrema esquerda.
c.	Apagar colunas desnecessárias.
d.	Retirar linhas repetidas em “Remover Duplicadas”.

### 4)	Tabela D_Descontos
a.	Criar a tabela D_Descontos a partir da duplicação da tabela Financials_origem
b.	Criar coluna ID_Produto a partir da “Coluna Condicional”. Em seguida, movê-la para a extrema esquerda.
c.	Apagar colunas desnecessárias.
d.	Retirar linhas repetidas em “Remover Duplicadas”.

### 5)	Tabela D_Detalhes
a.	Criar a tabela D_Detalhes a partir da duplicação da tabela D_Produtos_Detalhes
b.	Eliminar uma das “ETAPAS ELIMINADAS” (“Colunas Removidas”)
c.	Redefinir quais colunas são interessantes para tal tabela e apagar as outras colunas desnecessárias.

### 6)	Tabela F_Vendas
a.	Criar a tabela F_Vendas a partir da duplicação da tabela Financials_origem
b.	Criar coluna ID_Produto a partir da “Coluna Condicional”. Em seguida, movê-la para a extrema esquerda.
c.	Apagar colunas desnecessárias.
d.	Retirar linhas repetidas em “Remover Duplicadas”.
e.	Criar a Surrogate Key (SK) através da “Coluna de Índice”. Em seguida, renomeá-la de Índice para SK_ID e movê-la para a extrema esquerda.

---

## MODO DE EXIBIÇÃO DE TABELA:

1)	“Criar Tabela” denominada D_Calendario para inserir a DAX de data e hora (CALENDAR).
2)	Ocultar tabela Financials_origem.

---

## MODO DE EXIBIÇÃO DE MODELO:
Uma as tabelas dimensões a tabela fato por meio de relacionamentos, formando o Star Schema.

---

