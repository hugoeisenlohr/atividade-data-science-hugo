# 📚 Guia de Referência Rápida

## 🔗 Cheat Sheet de Comandos Úteis

### Pandas - Carregamento e Exploração
```python
# Carregar dados
df = pd.read_csv('caminho/arquivo.csv')

# Informações básicas
df.shape                    # (linhas, colunas)
df.head(), df.tail()        # Primeiras/últimas linhas
df.info()                   # Tipos de dados
df.describe()               # Estatísticas

# Dados faltantes
df.isnull().sum()           # Contar NaNs
df.dropna()                 # Remover NaNs
df.fillna(valor)            # Preencher NaNs
```

### Pandas - Manipulação
```python
# Seleção
df['coluna']                # Uma coluna
df[['col1', 'col2']]        # Múltiplas colunas
df.loc[0]                   # Linha por índice
df[df['col'] > valor]       # Filtrar por condição

# Modificação
df.rename({'velho': 'novo'}, axis=1)  # Renomear colunas
df.drop('col', axis=1)      # Remover coluna
df['nova_col'] = df['col'] * 2  # Criar nova coluna

# Agrupamento
df.groupby('col').mean()    # Agrupar e agregar
df.sort_values('col')       # Ordenar
```

### Scikit-Learn - Pré-processamento
```python
from sklearn.preprocessing import StandardScaler, MinMaxScaler

# Normalizar
scaler = StandardScaler() # transforma os valores para a mesma escala
X_scaled = scaler.fit_transform(X)

# Dividir dados
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
```

### Scikit-Learn - Modelos
```python
from sklearn.linear_model import LogisticRegression
from sklearn.ensemble import RandomForestClassifier

# Treinar
model = RandomForestClassifier(random_state=42)
model.fit(X_train, y_train)

# Predizer
y_pred = model.predict(X_test)
y_proba = model.predict_proba(X_test)
```

### Scikit-Learn - Métricas
```python
from sklearn.metrics import *

accuracy_score(y_test, y_pred)      # Acurácia
precision_score(y_test, y_pred)     # Precisão
recall_score(y_test, y_pred)        # Recall
f1_score(y_test, y_pred)            # F1-Score
confusion_matrix(y_test, y_pred)    # Matriz de confusão
classification_report(y_test, y_pred)  # Relatório
roc_auc_score(y_test, y_proba[:, 1])  # ROC-AUC
```

### Matplotlib & Seaborn - Visualização
```python
import matplotlib.pyplot as plt
import seaborn as sns

# Histograma
plt.hist(df['coluna'], bins=30)

# Boxplot
sns.boxplot(y=df['coluna'])

# Heatmap de correlação
sns.heatmap(df.corr(), annot=True)

# Scatter
plt.scatter(df['x'], df['y'])

# Configurações
plt.figure(figsize=(10, 6))
plt.title('Título')
plt.xlabel('X')
plt.ylabel('Y')
plt.show()
```

## 📊 Interpretação de Métricas

| Métrica | Significado | Range | Bom Valor |
|---------|------------|-------|-----------|
| **Acurácia** | % de predições corretas | 0-1 | > 0.80 |
| **Precisão** | % verdadeiros positivos entre os preditos positivos | 0-1 | > 0.80 |
| **Recall** | % de positivos reais que foram detectados | 0-1 | > 0.80 |
| **F1-Score** | Média harmônica entre Precisão e Recall | 0-1 | > 0.80 |
| **ROC-AUC** | Área sob a curva ROC | 0-1 | > 0.70 |

## 🎯 Matriz de Confusão

```
                 Predito
             Positivo  Negativo
Real Positivo  TP        FN
     Negativo  FP        TN

TP = Verdadeiro Positivo (correto!)
FP = Falso Positivo (alerta falso)
FN = Falso Negativo (perdeu um caso)
TN = Verdadeiro Negativo (correto!)

Acurácia = (TP + TN) / Total
Precisão = TP / (TP + FP)
Recall = TP / (TP + FN)
F1 = 2 * (Precisão * Recall) / (Precisão + Recall)
```

## 🐛 Dicas de Debugging

### Problema: Modelo com baixa acurácia
- Verificar se há dados faltantes
- Aumentar número de features
- Usar diferentes modelos
- Fazer feature engineering
- Balancear classes se desbalanceadas

### Problema: Valores muito diferentes em escala
- Usar StandardScaler ou MinMaxScaler
- Normalizar antes do treinamento

### Problema: Overfitting (ótimo em treino, ruim em teste)
- Aumentar regularização
- Diminuir complexidade do modelo
- Coletar mais dados
- Usar cross-validation

### Problema: Muitos falsos negativos/positivos
- Ajustar threshold de decisão
- Verificar matriz de confusão
- Balancear as classes

## 🚀 Workflow Recomendado

1. **Exploração**
   - Carregar dados
   - Verificar shape, tipos, descrição
   - Visualizar distribuições

2. **Limpeza**
   - Tratar dados faltantes
   - Remover/detectar outliers
   - Encodeamento de categorias

3. **Análise**
   - Correlação
   - Estatísticas
   - Gráficos exploratórios

4. **Pré-processamento**
   - Normalização/Padronização
   - Feature selection
   - Train-test split

5. **Modelagem**
   - Treinar múltiplos modelos
   - Validação cruzada
   - Comparar modelos

6. **Avaliação**
   - Calcular métricas
   - Matriz de confusão
   - Curva ROC
   - Feature importance

7. **Interpretação**
   - Documentar resultados
   - Explicar decisões
   - Sugerir melhorias

## 📖 Documentação Importante

- [Pandas Docs](https://pandas.pydata.org/docs/)
- [Scikit-learn Docs](https://scikit-learn.org/stable/)
- [Matplotlib Gallery](https://matplotlib.org/stable/gallery/index.html)
- [Seaborn Examples](https://seaborn.pydata.org)

---

**Boa sorte na atividade! 🚀**
