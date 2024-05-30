# Modelo Econométrico para Previsão de Gastos com Benefícios do INSS
![Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![INSS](https://admin-blog.grupogen.com.br/app/uploads/sites/2/2021/04/segurados-da-previdencia-social.jpg)

 **Autor:** Victor Flávio P. Dornelos\
**E-mail:** victor.dornelos@hotmail.com

## Sumário
1. [Descrição](https://www.mercadolivre.com.br/ar-condicionado-inverter-samsung-windfree-connect-9000-btus-frio-220v/p/MLB27658591?item_id=MLB4436518970&from=gshop&matt_tool=12284505&matt_word=&matt_source=google&matt_campaign_id=14303413664&matt_ad_group_id=136581273569&matt_match_type=&matt_network=g&matt_device=c&matt_creative=584243205817&matt_keyword=&matt_ad_position=&matt_ad_type=pla&matt_merchant_id=735098639&matt_product_id=MLB27658591-product&matt_product_partition_id=2267835084921&matt_target_id=pla-2267835084921&cq_src=google_ads&cq_cmp=14303413664&cq_net=g&cq_plt=gp&cq_med=pla&gad_source=1&gclid=CjwKCAjwx-CyBhAqEiwAeOcTdUZXxD8hnM2zu6_Lny9juF3eNX0NDXZpaQH-7yT3nn-g_KV8Ix7zrxoCCG0QAvD_BwE)
2. [Objetivo](https://www.mercadolivre.com.br/ar-condicionado-inverter-samsung-windfree-connect-9000-btus-frio-220v/p/MLB27658591?item_id=MLB4436518970&from=gshop&matt_tool=12284505&matt_word=&matt_source=google&matt_campaign_id=14303413664&matt_ad_group_id=136581273569&matt_match_type=&matt_network=g&matt_device=c&matt_creative=584243205817&matt_keyword=&matt_ad_position=&matt_ad_type=pla&matt_merchant_id=735098639&matt_product_id=MLB27658591-product&matt_product_partition_id=2267835084921&matt_target_id=pla-2267835084921&cq_src=google_ads&cq_cmp=14303413664&cq_net=g&cq_plt=gp&cq_med=pla&gad_source=1&gclid=CjwKCAjwx-CyBhAqEiwAeOcTdUZXxD8hnM2zu6_Lny9juF3eNX0NDXZpaQH-7yT3nn-g_KV8Ix7zrxoCCG0QAvD_BwE)
3. [Metodologia](https://www.mercadolivre.com.br/ar-condicionado-inverter-samsung-windfree-connect-9000-btus-frio-220v/p/MLB27658591?item_id=MLB4436518970&from=gshop&matt_tool=12284505&matt_word=&matt_source=google&matt_campaign_id=14303413664&matt_ad_group_id=136581273569&matt_match_type=&matt_network=g&matt_device=c&matt_creative=584243205817&matt_keyword=&matt_ad_position=&matt_ad_type=pla&matt_merchant_id=735098639&matt_product_id=MLB27658591-product&matt_product_partition_id=2267835084921&matt_target_id=pla-2267835084921&cq_src=google_ads&cq_cmp=14303413664&cq_net=g&cq_plt=gp&cq_med=pla&gad_source=1&gclid=CjwKCAjwx-CyBhAqEiwAeOcTdUZXxD8hnM2zu6_Lny9juF3eNX0NDXZpaQH-7yT3nn-g_KV8Ix7zrxoCCG0QAvD_BwE)
4. [Resultados](https://www.mercadolivre.com.br/ar-condicionado-inverter-samsung-windfree-connect-9000-btus-frio-220v/p/MLB27658591?item_id=MLB4436518970&from=gshop&matt_tool=12284505&matt_word=&matt_source=google&matt_campaign_id=14303413664&matt_ad_group_id=136581273569&matt_match_type=&matt_network=g&matt_device=c&matt_creative=584243205817&matt_keyword=&matt_ad_position=&matt_ad_type=pla&matt_merchant_id=735098639&matt_product_id=MLB27658591-product&matt_product_partition_id=2267835084921&matt_target_id=pla-2267835084921&cq_src=google_ads&cq_cmp=14303413664&cq_net=g&cq_plt=gp&cq_med=pla&gad_source=1&gclid=CjwKCAjwx-CyBhAqEiwAeOcTdUZXxD8hnM2zu6_Lny9juF3eNX0NDXZpaQH-7yT3nn-g_KV8Ix7zrxoCCG0QAvD_BwE)
5. [Referências](https://www.mercadolivre.com.br/ar-condicionado-inverter-samsung-windfree-connect-9000-btus-frio-220v/p/MLB27658591?item_id=MLB4436518970&from=gshop&matt_tool=12284505&matt_word=&matt_source=google&matt_campaign_id=14303413664&matt_ad_group_id=136581273569&matt_match_type=&matt_network=g&matt_device=c&matt_creative=584243205817&matt_keyword=&matt_ad_position=&matt_ad_type=pla&matt_merchant_id=735098639&matt_product_id=MLB27658591-product&matt_product_partition_id=2267835084921&matt_target_id=pla-2267835084921&cq_src=google_ads&cq_cmp=14303413664&cq_net=g&cq_plt=gp&cq_med=pla&gad_source=1&gclid=CjwKCAjwx-CyBhAqEiwAeOcTdUZXxD8hnM2zu6_Lny9juF3eNX0NDXZpaQH-7yT3nn-g_KV8Ix7zrxoCCG0QAvD_BwE)

## 1. Descrição

O Sistema de Previdência Social brasileiro, responsável por realizar pagamentos de benefícios como aposentadorias, auxílios-doença e acidente, pensões por morte e salário-família, tem um papel socioeconômico crucial ao garantir recursos para os cidadãos mais vulneráveis da sociedade. O sistema funciona pelo regime de repartição, onde os trabalhadores ativos contribuem para o INSS para financiar os pagamentos aos beneficiários.\
Devido a fatores demográficos e econômicos, a tendência de aumento de gastos com benefícios impacta diretamente o orçamento público, tornando este um tema de grande relevância socioeconômica.

## 2. Objetivo

O objetivo deste projeto é criar um modelo econométrico de série temporal para prever de forma eficiente os gastos com benefícios do INSS, auxiliando na análise de políticas públicas.

## 3. Metodologia
A metodologia adotada começou com a obtenção de dados do site do Ministério da Previdência Social, através do Anuário Estatístico da Previdência Social (AEPS), onde foram disponibilizadas diversas tabelas contendo informações sobre o fluxo de caixa e o balanço financeiro do sistema. A partir desses dados, foi possível construir uma base de dados utilizando Excel e Pandas.\
Em seguida, utilizando a linguagem de programação Python, versão 3.12, em ambiente Jupyter Notebooks, realizei uma análise exploratória dos dados. Durante essa etapa, observa-se que se tratava de uma série temporal com tendência sazonal, que precisa levar em consideração para realização do modelo.\
Para escolher os modelos de previsão mais adequados, nos baseamos no Trabalho de Conclusão de Curso (TCC) intitulado "Análise da Série Histórica dos Benefícios Concedidos da Previdência Social do Brasil", de Poliana Lemos da Silva, realizado na UFMG em 2017. Os modelos selecionados para aplicação foram o SARIMA e a Suavização Exponencial com Holt-Winters.\
Para encontrar o melhor modelo SARIMA, utilizamos a biblioteca Pmdarima e realizamos diversos testes com o AutoARIMA para encontrar o modelo com menor AIC (Critério de Informação de Akaike). Em seguida, com a biblioteca Statsmodels, implementamos o modelo SARIMA aditivo. Posteriormente, utilizando novamente o Statsmodels, aplicamos a Suavização Exponencial aditiva para realizar a previsão da série temporal.\
Além disso, para avaliar a performance dos modelos, utilizamos métricas como Erro Médio Absoluto (MAD), Erro Médio Quadrático (MSD) e Erro Percentual Absoluto Médio (MAPE), utilizando a biblioteca Scikit-learn. Também calculamos o Erro Percentual Médio (MPE). Para visualização dos resultados, usei as bibliotecas Matplotlib e Seaborn. Essa abordagem nos permitiu entender a dinâmica dos dados e desenvolver modelos de previsão robustos para os gastos com benefícios do INSS.

## 4. Resultados

O modelo de Suavização Exponencial com Holt-Winters apresentou a melhor performance na previsão da série de dados reais. No entanto, houve dificuldade em estimar o período da Pandemia da Covid-19, devido ao cenário atípico. A conclusão é que o regime de repartição adotado pelo governo brasileiro enfrentará desafios com o constante crescimento dos gastos com os benefícios da Previdência Social.\

![grafico](/Users/victor/Desktop/curso python/Serietemporalprev/Serie_temporal_previdencia_social/foto.png)

## 5. Referências
Lemos da Silva, Poliana. Análise da Série Histórica dos Benefícios Concedidos da Previdência Social do Brasil. Trabalho de Conclusão de Curso (TCC) - Universidade Federal de Minas Gerais, 2017. Disponível em: <https://repositorio.ufmg.br/bitstream/1843/BUOS-B4GJ44/1/tcc_ufmg_poliana_lemos_da_silva.pdf\>. Acesso em: 30 de maio de 2024.\
Previdência Social do Brasil. Dados Estatísticos da Previdência Social e INSS. Disponível em: <https://www.gov.br/previdencia/pt-br/assuntos/previdencia-social/dados-estatisticos-previdencia-social-e-inss\>. Acesso em: 30 de maio de 2024.
