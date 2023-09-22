
# 📊 Indicador de região de congestão de preços em ativos financeiros

Bem-vindo ao meu primeiro projeto em Python, este é um projeto autêntico e estou estudando para enriquecê-lo com novas funções e futuramente técnicas de machine learning. O objetivo é que ele seja migrado para as plataformas do Metatrader e TradingView.




## 🚀 Funcionamento
Este indicador busca no gráfico de preços a principal região de congestão ou "região de briga" que são aquelas onde há mais aberturas e fechamentos de candles.

O algoritmo começa comparando duas metades do range de preços e selecionando aquela que tem maior pontuação, depois armazena o novo range de preços da região com maior pontuação e analisa as duas metades dessa nova região. Usando o `while` a seleção se repete até que não haja distância entre as regiões.

Você pode selecionar o ativo que quiser a partir da biblioteca do Yahoo Finance, além do timeframe e o intervalo dos dados. Basta alterar os valores de `tickers`, `period` e `interval`.

```python
data = yf.download(tickers='EURJPY=x', period='1d', interval='5m')
```

