# Data Science Challenge Alura Store

Análise de Dados de Vendas de Lojas
Este projeto realiza uma análise detalhada de dados de vendas de várias lojas. A análise foi feita utilizando o Google Colab com a linguagem Python, onde utilizamos bibliotecas como Pandas, Matplotlib e SQLite para realizar a leitura, processamento e visualização dos dados.

Funcionalidades
Carregamento dos Dados:

O projeto carrega os dados de várias lojas de arquivos CSV (contendo informações sobre produtos vendidos, preços, avaliações, frete, etc.).

Através do pandas, as tabelas CSV foram carregadas em DataFrames para manipulação.

Análise de Faturamento por Loja:

Realizamos a análise do faturamento por loja, considerando o total de vendas de cada loja, utilizando a coluna Preço.

Foi possível agrupar e somar o faturamento por loja, proporcionando uma visão clara do desempenho financeiro de cada uma.

Análise de Categorias de Produtos:

Identificação das categorias de produtos mais vendidas.

Cálculo do faturamento total por categoria de produto.

Exibição dos cinco produtos mais e menos vendidos por categoria.

Avaliação de Produtos e Lojas:

Cálculo da média de avaliações de produtos vendidos em cada loja.

Exibição das lojas com as melhores e piores avaliações, ajudando a identificar quais lojas estão recebendo os melhores feedbacks dos clientes.

Gráficos Interativos:

Gráficos de barras para visualização do desempenho de faturamento por loja e por categoria de produto.

Gráficos de linha e pizza para visualização de tendências de vendas, avaliações e outros dados de interesse.

Análise de Frete Médio:

Cálculo do frete médio por loja para verificar o custo médio de envio dos produtos para os clientes.

Recomendação para Venda de Loja:

Com base em um conjunto de critérios como desempenho de vendas, avaliações e frete médio, o sistema sugere qual loja possui o pior desempenho e que pode ser considerada para venda.

Como Usar
Clone este repositório ou baixe os arquivos no Google Colab.

Carregue os dados das lojas nos arquivos CSV para realizar as análises.

Utilize as funções implementadas para:

Realizar as análises de faturamento, avaliação, e frete.

Gerar gráficos para visualização.

Obter recomendações de quais lojas devem ser vendidas com base nos dados.

Requisitos
Python 3.x

Pandas

Matplotlib

SQLite (para análise de banco de dados)

Google Colab

Exemplo de Código
Aqui está um exemplo simples de como carregar os dados de uma loja e analisar o faturamento:

python
Copiar
Editar
import pandas as pd

# Carregar o arquivo CSV
url = "https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science/refs/heads/main/base-de-dados-challenge-1/loja_1.csv"
loja_1 = pd.read_csv(url)

# Calcular o faturamento por loja
faturamento_por_loja = loja_1.groupby("Loja")["Preço"].sum().reset_index()

# Exibir resultados
print(faturamento_por_loja)
Resultados Esperados
Após rodar os códigos e gerar os gráficos e análises, você poderá identificar:

Loja com maior faturamento.

Categorias de produtos mais rentáveis.

Loja com melhor e pior avaliação.

Loja com o menor desempenho, recomendada para ser vendida.

Contribuições
Se você deseja contribuir para o projeto, basta seguir os seguintes passos:

Faça um fork deste repositório.

Crie uma branch para sua feature (ex: feature/nova-analise).

Faça suas alterações e commit.

Envie um pull request.

Licença
Este projeto é licenciado sob a MIT License.
