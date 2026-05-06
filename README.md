# 🎓 Atividade: Projeto de Ciência de Dados com Boas Práticas

## 📋 Objetivo

Nesta atividade, você vai trabalhar em um **projeto real de Ciência de Dados** seguindo as melhores práticas da indústria. O projeto envolve análise, tratamento e modelagem de dados sobre doenças cardíacas.

## 📁 Estrutura do Projeto

```
atividade_data_science/
├── README.md                          # Este arquivo
├── data/
│   ├── raw/                          # Dados brutos (nunca alterar!)
│   │   └── heart_disease.csv
│   └── processed/                    # Dados tratados
│       └── heart_disease_processed.csv
├── notebooks/
│   ├── 01_EDA_e_Tratamento.ipynb    # Seu trabalho aqui!
│   └── 02_Treino_e_Avaliacao.ipynb   # E aqui!
└── requirements.txt                  # Dependências do projeto
```

## 🚀 Como Começar

### 1. Preparar o Ambiente
```bash
# Instalar as dependências
pip install -r requirements.txt
```

### 2. Explorar os Dados
Abra o notebook `notebooks/01_EDA_e_Tratamento.ipynb` e siga as instruções:
- Carregue os dados brutos de `data/raw/heart_disease.csv`
- Realize análise exploratória (EDA)
- Trate dados faltantes e outliers
- Normalize/Padronize as features
- **Salve os dados processados em `data/processed/heart_disease_processed.csv`**

### 3. Treinar e Avaliar
Abra o notebook `notebooks/02_Treino_e_Avaliacao.ipynb` e siga as instruções:
- Carregue os dados já tratados
- Divida em treino e teste
- Treine um modelo de classificação
- Avalie e interprete os resultados

## 📊 Dataset

**Heart Disease Dataset** (UCI Machine Learning Repository)

- **Features**: 13 atributos médicos (idade, pressão arterial, colesterol, etc.)
- **Target**: Presença de doença cardíaca (0 = não, 1 = sim)
- **Tamanho**: ~300 amostras

## 🎯 Boas Práticas Implementadas

✅ **Separação clara** entre dados brutos e processados  
✅ **Reutilização de código** - dados tratados em um notebook, utilizados em outro  
✅ **Reprodutibilidade** - notebooks bem documentados  
✅ **Versionamento** - estrutura pronta para Git  
✅ **Documentação** - markdown explicando cada passo  

## 📝 Entrega

Você deve completar:
1. ✓ EDA completa com gráficos e insights
2. ✓ Tratamento de dados bem documentado
3. ✓ Arquivo CSV processado salvo corretamente
4. ✓ Modelo treinado com boas métricas
5. ✓ Análise clara dos resultados
6. ✓ Anotações markdown em cada célula explicando o que fez

## 💡 Dicas

- **Sempre inspeccione seus dados primeiro**: `df.info()`, `df.describe()`, `df.head()`
- **Documente suas decisões**: Por que removeu aquela coluna? Por que usou aquele modelo?
- **Teste seus preprocessadores**: O que funciona em treino, funciona em teste?
- **Visualize sempre**: Um gráfico vale mil palavras!


---

