# Introdução ao Pandas

Pandas é uma biblioteca do Python para **manipulação e análise de dados**. É muito usada para trabalhar com tabelas, CSVs e bancos de dados simples.

## Instalação
Para instalar Pandas, execute:
```bash
pip install pandas
```

## Importando Pandas
No Python, usamos:
```python
import pandas as pd
```

`pd` é o apelido padrão para trabalhar com a biblioteca.

## Lendo arquivos CSV
```python
import pandas as pd

df = pd.read_csv("caminho/do/arquivo.csv")
print(df)
```
- `df` é um **DataFrame**, uma tabela com linhas e colunas.
- Você pode ver as primeiras linhas com:
```python
df.head()
```
- Ou as últimas linhas com:
```python
df.tail()
```

## Informações sobre o DataFrame
```python
df.info()       # mostra colunas, tipos de dados e valores nulos
df.describe()   # estatísticas básicas das colunas numéricas
df.shape        # retorna (n_linhas, n_colunas)
df.columns      # nomes das colunas
```
