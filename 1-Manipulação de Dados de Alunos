# 🐼 Manipulação de Dados de Alunos

### Arquivo base: `alunos.csv`

Faça o download [deste arquivo](https://github.com/lukas-senai/pandas-tutorial/blob/main/assets/alunos.csv) e coloque na mesma pasta que seu arquivo python.

---

## 1️⃣ Importando Pandas e lendo o arquivo

```python
import pandas as pd

df = pd.read_csv("alunos.csv")
print(df)
```

Aqui estamos importando a biblioteca pandas (`pd` é o apelido comum) e lendo o arquivo CSV com `pd.read_csv`. O resultado é um **DataFrame**, que é como uma tabela do Excel, e `print(df)` mostra todos os dados.

---

## 2️⃣ Seleção de colunas

```python
print(df["Nome"])  # Mostra apenas a coluna Nome
print(df[["Nome", "Nota"]])  # Mostra Nome e Nota
```

Podemos selecionar uma coluna (retorna uma Series) ou várias colunas (retorna um DataFrame). Isso é útil quando queremos trabalhar apenas com informações específicas.

---

## 3️⃣ Filtrando informações

```python
aprovados = df[df["Nota"] >= 7]
print(aprovados)

idade_17 = df[df["Idade"] == 17]
print(idade_17)
```

Para filtrar dados usamos `df[condição]`. No primeiro caso, selecionamos alunos com nota maior ou igual a 7. No segundo, apenas alunos com idade 17. Isso retorna sempre um **novo DataFrame**.

---

## 4️⃣ Estatísticas básicas

```python
media = df["Nota"].mean()
print("Média das notas:", media)

print("Maior nota:", df["Nota"].max())
print("Menor nota:", df["Nota"].min())

qtd_maior_17 = df[df["Idade"] > 17].shape[0]
print("Alunos com idade > 17:", qtd_maior_17)
```

Pandas facilita cálculos estatísticos: `mean()` calcula média, `max()` e `min()` retornam valores extremos. Para contar linhas que atendem a uma condição, usamos `.shape[0]`.

---

## 5️⃣ Criando novas colunas

```python
df["Situação"] = df["Nota"].apply(lambda x: "Aprovado" if x >= 7 else "Reprovado")
print(df)
```

Aqui criamos a coluna `Situação`. A função `apply()` aplica uma função a cada valor da coluna `Nota`. Se a nota for >= 7, o aluno é "Aprovado", caso contrário "Reprovado".

---

## 6️⃣ Ordenando dados

```python
print(df.sort_values(by="Nota", ascending=False))  # Ordena por nota do maior para o menor
print(df.sort_values(by="Nome"))  # Ordena por nome em ordem alfabética
```

`sort_values` ordena o DataFrame por uma coluna. `ascending=False` faz ordem decrescente, padrão é crescente.

---

## 7️⃣ Exportando resultados

```python
df.to_csv("relatorio_final.csv", index=False)
```

`to_csv` salva o DataFrame em um arquivo CSV. Usar `index=False` evita salvar a coluna de índice, deixando o arquivo limpo.

---

✅ **Extra:** calcular média dos aprovados e reprovados:

```python
media_aprovados = df[df["Situação"]=="Aprovado"]["Nota"].mean()
media_reprovados = df[df["Situação"]=="Reprovado"]["Nota"].mean()
print("Média dos aprovados:", media_aprovados)
print("Média dos reprovados:", media_reprovados)
```

Filtramos pelo valor da coluna `Situação` e usamos `mean()` para calcular a média separadamente.
