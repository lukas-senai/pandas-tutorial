# Operações básicas com Pandas

## Seleção de colunas
```python
# Selecionar uma coluna
df["Nome"]

# Selecionar várias colunas
df[["Nome", "Idade"]]
```

## Filtragem de linhas
```python
# Apenas linhas com idade >= 18
df[df["Idade"] >= 18]

# Apenas linhas com nota >= 7
df[df["Nota"] >= 7]
```

## Estatísticas simples
```python
# Média de uma coluna
df["Nota"].mean()

# Maior e menor valor
df["Nota"].max()
df["Nota"].min()

# Contar linhas que atendem a uma condição
df[df["Idade"] > 17].shape[0]
```

## Criando novas colunas
```python
# Criando uma coluna Situação
df["Situacao"] = df["Nota"].apply(lambda x: "Aprovado" if x >= 7 else "Reprovado")
```

## Ordenando dados
```python
# Ordenar por coluna
df.sort_values(by="Nota", ascending=False)

# Ordenar por mais de uma coluna
df.sort_values(by=["Nota", "Idade"], ascending=[False, True])
```

## Exportando DataFrames
```python
df.to_csv("arquivo_final.csv", index=False)
```
- `index=False` evita salvar a coluna de índice no arquivo.
