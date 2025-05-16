# InteliCompAV2_2025_1
Relatório de Análise de Dados e Modelagem Preditiva de Salários
Equipe: Daphne Soares, Fred Lopes, Marcelo Silveira
1. Introdução
Este relatório apresenta uma análise exploratória de dados (EDA) e a construção de modelos de machine learning para prever salários com base em características como idade, gênero, nível de educação, cargo e anos de experiência. O objetivo é identificar padrões nos dados e comparar o desempenho de diferentes algoritmos de regressão.
2. Pré-processamento dos Dados
2.1. Tratamento de Valores Ausentes
Colunas numéricas (Age, Years of Experience, Salary):
Valores ausentes foram preenchidos com a mediana para evitar influência de outliers.
Colunas categóricas (Gender, Education Level, Job Title):
Valores ausentes foram substituídos pela moda (valor mais frequente).
2.2. Padronização de Dados Categóricos
Nível de educação (Education Level):
Valores como "phD", "PhD", "Master's Degree" foram padronizados para garantir consistência (ex.: "PhD", "Master's").
3. Análise Exploratória de Dados (EDA)
3.1. Salário por Gênero
Mulheres têm um salário médio menor que homens, mas a análise não considera diferenças de cargo ou experiência, pessoas que não se identificaram aparecem com a maior média, porém, a quantidade de dados existente na database é muito inferior à de masculino e feminino.

3.2. Salário por Cargo
Top 10 cargos mais bem pagos:
Cargos como "Director", "CEO", e "Data Scientist" lideram a lista.


3.3. Salário por Nível de Educação
Quanto maior a escolaridade, maior o salário:
Visto que pessoas com PhD possuem salários maiores, e pessoal em High School menor.

3.4. Salário por Anos de Experiência
Relação linear positiva:
Salários aumentam conforme os anos de experiência crescem.

4. Modelagem Preditiva
4.1. Pré-processamento para Machine Learning
Variáveis categóricas (Gender, Education Level, Job Title):
Codificadas com One-Hot Encoding.
Divisão dos dados:
80% treino e 20% teste.
4.2. Modelos Testados
Foram avaliados quatro algoritmos de regressão:
Modelo
MAE
RMSE
R² (Ajuste)
Regressão Linear
15495.11
21467.9
0.8292
Random Forest
3335.33
8246.2
0.9748
Ridge Regression
15539.66
21480.45
0.829
Gradient Boosting
11723.00
15883.04
0.9065

4.3. Resultados
Melhor modelo: Random Forest com:
MAE = 2884.60 (erro médio absoluto)
RMSE = 6881.90 (erro médio absoluto)
R² = 0.97 (excelente ajuste aos dados).
Pior modelo: Regressão Linear e Ridge,ambos tiveram desempenho similar e ruim comparado aos outros.
XGBoost teve bom desempenho com relação ao R², mas ainda assim, inferior ao Random Forest.

5. Conclusões e Recomendações
5.1. Principais Achados
Experiência e Educação Impactam Salários:
Anos de experiência e nível de escolaridade têm forte correlação com salários.
Diferenças Salariais por Gênero:
Homens têm salários médios maiores, mas é necessário análise mais aprofundada (ex.: mesmo cargo e experiência).
Random Forest é o Melhor Modelo:
Teve o menor erro (MAE = 15k) e melhor explicação da variância (R² = 0.97).
