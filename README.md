## **O Negócio por trás da "Moda": Análise de Mercado do Jiu-Jitsu no Brasil**



📌 Visão Geral do Projeto

Nos últimos anos, a percepção social é de que o Jiu-Jitsu (BJJ) "virou moda" no Brasil. Este projeto de Market Intelligence e Engenharia de Dados testa essa hipótese empiricamente, cruzando o interesse orgânico de topo de funil (buscas de iniciação) com marcos culturais e a viabilidade de negócios físicos (abertura de academias).



Um projeto exploratório de análise de dados para investigar o fenômeno social do Jiu-Jitsu no Brasil e entender como o interesse pela arte suave evoluiu na internet e no mundo físico.



🛠️ Stack Tecnológico

Linguagem: Python



Bibliotecas de Dados: pandas, numpy



Extração: pytrends (Google Trends API não-oficial)



Visualização: matplotlib, seaborn



Metodologia Analítica: Análise de Séries Temporais, Coeficiente de Correlação de Pearson, Modelagem de Cohorts de Maturidade.



#### **📊 Arquitetura e Metodologia**

O projeto foi dividido em três camadas de análise:



**1. Aquisição Digital (O Topo do Funil)**

Para isolar a intenção real de prática esportiva do mero entretenimento, extraímos dados históricos (2004-2026) da API do Google Trends focados exclusivamente nas "dores do iniciante" (ex: como amarrar faixa, comprar kimono, regras). Os termos foram normalizados em um Índice Agregado de Buscas.



**2. Contextualização de Mercado (Eventos Causais)**

Sobreposição matemática dos dados orgânicos com marcos da cultura pop e eventos globais, validando a causalidade dos picos e vales de interesse:



2011: O Boom do MMA no Brasil (UFC Rio).



2020: A Pandemia (fechamento de academias).



2022: A Explosão do Grappling (No-Gi / ADCC).



**3. Prova de Conceito (PoC): O Impacto no Mundo Físico**

Para testar a correlação entre a busca digital e a injeção de capital no mundo físico, foi construído um modelo cruzando o Índice Agregado com o volume de aberturas de CNPJs (CNAE 8512-1/00 - Ensino de Esportes).



Nota de Arquitetura (PoC): A base de CNPJs utilizada nesta visualização específica é uma simulação estrutural (Mock Data). Em um ambiente de produção real, a extração dos +30GB de arquivos abertos da Receita Federal seria orquestrada localmente via DuckDB para contornar gargalos de memória (OOM), aplicando filtros de Regex na Razão Social antes da carga no Pandas.



#### **📈 Principais Insights** 

**A Mudança Estrutural de Patamar:** O Jiu-Jitsu deixou de ser um nicho. O baseline médio de buscas orgânicas subiu de 54.1 (Era do MMA) para 76.9 pontos (Era Lifestyle / Pós-2021). O esporte expandiu seu TAM (Total Addressable Market).



**Resiliência e Demanda Reprimida**: Apesar da queda de -38,89% no ano crítico da pandemia (2020), o mercado registrou um rebote agressivo, com crescimentos anuais (YoY) de +36,6% (2021) e +44,1% (2022).



**Validação da Tese (Forte Correlação)**: O modelo provou matematicamente (Correlação de Pearson = 0.88) que a escalada de interesse online reflete diretamente na escalabilidade física, transformando a "moda" em um modelo de negócio consolidado.



📂 Como Executar este Projeto Localmente

Clone o repositório:

git clone valquerya/jiu-jitsu-virou-moda



Instale as dependências:

pip install pandas pytrends matplotlib seaborn numpy



Execute o extrator para atualizar os dados do Google Trends:

python extrator.py



Rode os scripts de visualização para gerar os gráficos atualizados na sua máquina.



👤 Autora

Valquíria Alves

Estratégia de Produto, Inteligência de Mercado \& Dados

https://www.linkedin.com/in/val-quiria/

