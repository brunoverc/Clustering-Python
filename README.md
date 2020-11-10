# brunovercosa.github
# brunovercosa.github

# Clustering

- Clustering

    - Algoritmo KMeans

 ```bash
pip install -U scikit-learn
```

## Desenvolvido por

Bruno Nascimento Verçosa

bruno.nv@hotmail.com | bruno@teckavan.com

## Descrição

Agrupamento de mineradoras de acordo com os dados de Exploração Mineral disponíveis no portal de dados do Governo Federal.

#### Agrupar Mineradoras de acordo com os dados de Exploração Mineral


## Bibliotecas

```python
import foobar

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from matplotlib import pylab
from sklearn.cluster import KMeans
from sklearn.decomposition import PCA
from sklearn.model_selection import train_test_split
from scipy.spatial.distance import cdist, pdist
from sklearn.metrics import silhouette_score
import warnings

```

## Passos:

- Carregando os dados
- Retirando espaços em branco do início e fim das variáveis
- Limpeza de linhas com valores faltantes e necessários para a análise
- Alteração das colunas categóricas para um valor numério (índice) e transformação em uma coluna categórica
- Inserindo os valores faltantes na coluna Quantidade Comercializada com a média de valores pela Substância (Minério)
- Aplicação de redução da dimensionalidade
- Criação de 12 modelos K-means para comparação do melhor valor de K
- Para comparação do melhor valor de K é calculado:
	- Centroids
	- Distância Euclidiana
	- Soma dos quadrados das distâncias
	- Soma total dos quadrados (Essa etapa pode demorar um pouco de acordo com a quantidade de informações e modelos)
	
	```python
		soma_total = sum(pdist(pca)**2)/pca.shape[0]
		
	```

	- Soma dos quadrados entre Clusters
- Os dados são exibidos em um gráfico de Curva de Elbow e o valor de 3 K's é o escolhido por comparação com outros modelos.
- Criação do modelo com K = 3
- Calculo da Silhouette Score
- Criação do Cluster Map


## Fonte de Dados

Dataset: Compensação Financeira pela Exploração de Recursos Minerais (CFEM)
Disponível em: https://dados.gov.br/dataset/sistema-arrecadacao
