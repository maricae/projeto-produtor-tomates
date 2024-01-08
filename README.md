# Remoção de Outliers (Produtor de Tomate)
## Detecção e Remoção de Outliers Univariados: Um Exemplo Prático
#### Contexto da Análise:
Um produtor de tomates estipulou sua meta de faturamento no valor de R$ 3 Milhões para o segundo trimestre de 2023. Com isso, sua estratégia é aumentar o número de clientes e ele precisa saber qual o aumento necessário para alcançar sua meta.

Para encontrar esse percentual precisamos saber qual seria o número médio de tomates que seus clientes compram diariamente. Além disso, existem clientes que compram para consumo próprio, clientes que compram para revenda (Supermercados) e restaurantes.

Porém, o produtor acredita que a maioria dos seus clientes são restaurantes (não existe uma classificação no banco de dados), mas mesmo assim sabe-se que existem grandes mercados parceiros que apresentam uma disparidade muito grande em relação aos outros clientes. Essas grandes redes classificaremos como Outliers e que podem atrapalhar nossa análise causando viés na média.

Para isso, tendo disponível a base de vendas do primeiro trimestre de 2023, precisaremos entender o cenário atual das vendas do produtor de tomate: quantas vendas realizou, quantos clientes, análise diária, etc.

#### O que são outliers?
Outliers são valores muito distantes da média, podendo ser muito superior ou muito inferior. Com a presença de outliers o cálculo da média pode resultar em um valor viesado, pois valores muito discrepantes em relação às outras observações podem puxar o resultado tanto pra mais quanto pra menos. Para isso, precisamos detectar a presença dessas observações e removê-las para que a média tenha um resultado mais robusto.

Infelizmente, não existe uma regra para detectar definitivamente outliers. A detecção depende do contexto e do processo de coleta de dados. Embora não haja uma definição matemática única, existem procedimentos e testes estatísticos que podem ser utilizados para detectar esses pontos. Se os seus dados apresentam ou não distribuição normal, se são outliers univariados ou multivariados definirá qual método é mais adequado para sua análise.

Neste caso, nossos dados não apresentam distribuição normal e são outliers univariados (estamos lidando com apenas uma variável), então usaremos o método do Intervalo Interquartil (Boxplot).

O que causa a presença de outliers: Erros de medida, na extração dos dados, no processamento de dados, na amostragem e os naturais. Neste caso são outliers naturais, pois são apenas os clientes que apresentam um padrão diferente do restante da amostra.

#### Sobre os Dados:
A base possui 44.236 linhas com o número de unidades compradas diariamente por cada cliente, ou seja, está agrupada por data e por cliente_id. Além disso, possui o valor diário referente ao primeiro trimestre de 2023. Disponível em: https://www.kaggle.com/datasets/marianacaetano/compras-diarias-de-clientes
