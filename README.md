# 📊 Datasets — Análise de Dados e Big Data

Repositório de datasets para a disciplina **Análise de Dados e Big Data**.

**Professor:** Giovane Barcelos — giovane.barcelos@ulife.com.br

> 🟢 **Dados reais** de fontes públicas: Portal da Transparência, TSE, IBGE, INEP, DATASUS, consumidor.gov.br, Google Trends, DataReportal  
> 🟡 **Dados realísticos** (fictícios com estrutura real): audiência TV, pesquisa de mercado, e-commerce, campanhas marketing, consumo de mídia  
> 🔴 **Dados fictícios propositais**: exemplos LGPD (dados pessoais fictícios para discussão) e avaliação A1 (com erros propositais)  
>
> ⚠️ Nenhum dado pessoal real está presente neste repositório. Gerado com `seed=42` para reprodutibilidade.

---

## 📁 Estrutura do Repositório

```
datasets/
├── class01/   → Aula 01 — Introdução à Ciência de Dados
├── class02/   → Aula 02 — Ecossistema de Dados
├── class03/   → Aula 03 — Excel: Fundamentos
├── class04/   → Aula 04 — Tabelas Dinâmicas e PROCV
├── class05/   → Aula 05 — OpenRefine e ETL
├── class06/   → Aula 06 — Visualização e A1
├── class07/   → Aula 07 — Coleta Web e Google Trends
├── class08/   → Aula 08 — Orange Data Mining
├── class09/   → Aula 09 — Pesquisa de Mercado
├── class10/   → Aula 10 — Fundamentos de Visualização
├── class11/   → Aula 11 — Power BI: Introdução
├── class12/   → Aula 12 — Power BI Avançado + A2
├── class13/   → Aula 13 — Data Storytelling
└── class14/   → Aula 14 — Big Data na Comunicação
```

---

## 📋 Descrição dos Datasets

### `class01/` — Introdução à Ciência de Dados 🟢

> Fonte: Portal da Transparência (portaldatransparencia.gov.br)

| Arquivo | Registros | Formato | Descrição |
|---------|-----------|---------|-----------|
| `dataset_gastos_publicos.csv` | 600 | CSV (`;`) | Gastos públicos municipais por UF, categoria, órgão e tipo de despesa |

**Colunas:** `ID`, `Municipio`, `UF`, `Categoria`, `Orgao`, `Valor_R$`, `Data`, `Tipo_Despesa`, `Fonte_Recurso`

---

### `class02/` — Ecossistema de Dados 🟢

> Fontes: TSE Dados Abertos (eleições 2022) + IBGE (censo/indicadores) + Dados fictícios LGPD

| Arquivo | Registros | Formato | Descrição |
|---------|-----------|---------|-----------|
| `dataset_eleicoes_tse.csv` | 500 | CSV (`;`) | Dados eleitorais fictícios (candidatos, votos, partidos) |
| `dataset_censo_ibge.csv` | 38 | CSV (`;`) | Indicadores demográficos por município (população, PIB, IDHM) |
| `exemplos_lgpd/cadastro_clientes_FICTICIO.csv` | — | CSV (`;`) | Cadastro fictício para discussão de LGPD |
| `exemplos_lgpd/historico_navegacao_FICTICIO.csv` | — | CSV (`;`) | Histórico de navegação fictício para discussão de LGPD |
| `exemplos_lgpd/pesquisa_saude_FICTICIO.csv` | — | CSV (`;`) | Pesquisa de saúde fictícia para discussão de LGPD |

**Colunas (eleições):** `ID`, `Ano`, `UF`, `Municipio`, `Cargo`, `Candidato`, `Partido`, `Numero`, `Votos`, `Situacao`, `Genero`, `Cor_Raca`, `Escolaridade`  
**Colunas (censo):** `ID`, `Municipio`, `UF`, `Populacao`, `PIB_per_capita_R$`, `Taxa_Alfabetizacao_%`, `Renda_Media_R$`, `IDHM`, `Domicilios_com_Internet_%`, `Esperanca_Vida_Anos`, `Taxa_Desemprego_%`, `Area_km2`

---

### `class03/` — Excel: Fundamentos 🟢

> Fontes: INEP Censo Escolar + DATASUS/TabNet

| Arquivo | Registros | Formato | Descrição |
|---------|-----------|---------|-----------|
| `dataset_educacao_inep.csv` | 400 | CSV (`;`) | Indicadores educacionais por escola (matrículas, IDEB, aprovação) |
| `dataset_saude_datasus.csv` | 500 | CSV (`;`) | Indicadores de saúde por município e ano |

**Colunas (educação):** `ID`, `Municipio`, `UF`, `Nome_Escola`, `Rede`, `Nivel_Ensino`, `Matriculas_2023`, `Aprovacao_%`, `Reprovacao_%`, `Abandono_%`, `IDEB_2023`, `Docentes_Total`, `Infraestrutura_Score`  
**Colunas (saúde):** `ID`, `Municipio`, `UF`, `Ano`, `Indicador`, `Valor`, `Populacao_Base`, `Fonte`, `Periodo_Referencia`

---

### `class04/` — Tabelas Dinâmicas e PROCV 🟡

> Dados fictícios com estrutura real (audiência TV é proprietária — Kantar IBOPE)

| Arquivo | Registros | Formato | Descrição |
|---------|-----------|---------|-----------|
| `dataset_pesquisa_mercado.xlsx` | — | XLSX | Pesquisa de mercado com 2 abas (dados + referência para PROCV) |
| `dataset_audiencia_tv.csv` | 500 | CSV (`;`) | Audiência de TV por emissora, programa, faixa horária e praça |

**Colunas (audiência):** `ID`, `Data`, `Emissora`, `Programa`, `Faixa_Horaria`, `Share_%`, `Audiencia_Pontos`, `Faixa_Etaria_Predominante`, `Genero_Predominante`, `Praca`, `Dia_Semana`

---

### `class05/` — OpenRefine e ETL 🟢

> Fonte: Baseado na estrutura do consumidor.gov.br (com inconsistências propositais para ETL)

| Arquivo | Registros | Formato | Descrição |
|---------|-----------|---------|-----------|
| `dataset_sujo_procon.csv` | 630 | CSV (`;`) | Reclamações PROCON **com inconsistências propositais** (duplicatas, datas em formatos variados, erros de digitação) |

**Colunas:** `ID`, `Data_Reclamacao`, `Consumidor`, `CPF`, `Cidade`, `UF`, `Categoria`, `Empresa`, `Descricao_Problema`, `Status`, `Nota_Consumidor`, `Tempo_Resposta_Dias`

> 💡 Este dataset foi intencionalmente "sujado" para prática de limpeza com OpenRefine.

---

### `class06/` — Visualização e Avaliação A1 🟡

> Dados fictícios (mídia regional sem fonte aberta + A1 com erros propositais)

| Arquivo | Registros | Formato | Descrição |
|---------|-----------|---------|-----------|
| `dataset_midia_regional.csv` | 400 | CSV (`;`) | Veículos de comunicação regional (audiência, receita, engajamento) |
| `dataset_avaliacao_a1.csv` | 200 | CSV (`;`) | Dataset para avaliação A1 (com problemas propositais para ETL) |

**Colunas (mídia):** `ID`, `Regiao`, `UF`, `Municipio`, `Veiculo_Comunicacao`, `Tipo_Conteudo`, `Audiencia_Mensal`, `Engajamento_%`, `Receita_Publicitaria_R$`, `Funcionarios`, `Ano_Fundacao`, `Plataforma_Digital`, `Assinantes_Digital`

---

### `class07/` — Coleta Web e Google Trends 🟢

> Fonte: Baseado em tendências reais do Google Trends Brasil 2024

| Arquivo | Registros | Formato | Descrição |
|---------|-----------|---------|-----------|
| `dataset_exemplo_importdata.csv` | 300 | CSV (`;`) | Dados de tendência de buscas para demonstração de `IMPORTDATA` no Google Sheets |

**Colunas:** `Data`, `Termo_Pesquisa`, `Volume_Buscas`, `Regiao`, `Categoria`, `Tendencia`

---

### `class08/` — Orange Data Mining 🟡

> Dados fictícios (formato survey — dados de consumo de mídia são proprietários)

| Arquivo | Registros | Formato | Descrição |
|---------|-----------|---------|-----------|
| `dataset_consumo_midia.csv` | 1.200 | CSV (`;`) | Consumo de mídia com variáveis numéricas e categóricas para clustering e análise visual |

**Colunas:** `ID`, `Idade`, `Genero`, `Escolaridade`, `Renda_Faixa`, `Regiao`, `Plataforma_Principal`, `Horas_Dia_Media`, `Dispositivo_Principal`, `Freq_Uso_Noticias`, `Confianca_Midia_1a10`, `Compartilha_Noticias`, `Assina_Jornal_Digital`, `Gasto_Mensal_Midia_R$`, `Satisfacao_Conteudo_1a10`, `Cluster_Sugerido`

---

### `class09/` — Pesquisa de Mercado e Comportamento 🟡

> Dados fictícios (formato survey — dados proprietários)

| Arquivo | Registros | Formato | Descrição |
|---------|-----------|---------|-----------|
| `dataset_comportamento_consumo.csv` | 1.000 | CSV (`;`) | Comportamento de consumo com variável-alvo `Classe_Consumidor` para árvore de decisão |

**Colunas:** `ID`, `Idade`, `Genero`, `Renda_Mensal_R$`, `Escolaridade`, `Estado_Civil`, `Filhos`, `Cidade`, `UF`, `Canal_Compra_Preferido`, `Influencia_Decisao`, `Categoria_Produto_Frequente`, `Gasto_Medio_Mensal_R$`, `Freq_Compra_Online_Mes`, `Usa_Cupom_Desconto`, `Segue_Influenciadores`, `Compra_Por_Impulso`, `Classe_Consumidor`

---

### `class10/` — Fundamentos de Visualização 🟢

> Fontes: IBGE (população, PIB), PNAD Contínua (internet), DataReportal (mídia), IAB Brasil (publicidade)

| Arquivo | Registros | Formato | Descrição |
|---------|-----------|---------|-----------|
| `dataset_visualizacao_pratica.csv` | 162 | CSV (`;`) | Indicadores por UF (2019–2024): mídia, internet, streaming e publicidade digital — ideal para mapas coropléticos e bar chart race |

**Colunas:** `Ano`, `UF`, `Regiao`, `Populacao`, `PIB_Bilhoes_R$`, `Acesso_Internet_%`, `Uso_Redes_Sociais_h_dia`, `Confianca_Midia_Tradicional_%`, `Confianca_Midia_Digital_%`, `Assinantes_Streaming_mil`, `Ouvintes_Podcast_mil`, `Receita_Publicidade_Digital_Mi_R$`

---

### `class11/` — Power BI: Introdução 🟡

> Dados fictícios (e-commerce — dados proprietários)

| Arquivo | Registros | Formato | Descrição |
|---------|-----------|---------|-----------|
| `dataset_ecommerce_comunicacao.csv` | 1.000 | CSV (`;`) | Pedidos de e-commerce com dimensões geográficas, temporais e de marketing |

**Colunas:** `Pedido_ID`, `Data_Pedido`, `Cliente_ID`, `Cidade`, `UF`, `Regiao`, `Categoria_Produto`, `Produto`, `Quantidade`, `Valor_Unitario_R$`, `Valor_Total_R$`, `Canal_Marketing`, `Desconto_%`, `Frete_R$`, `Status_Pedido`, `Avaliacao_1a5`, `Tempo_Entrega_Dias`, `Reclamacao`

---

### `class12/` — Power BI Avançado + A2 🟡

> Dados fictícios (métricas de campanhas são dados internos/proprietários)

| Arquivo | Registros | Formato | Descrição |
|---------|-----------|---------|-----------|
| `dataset_campanhas_marketing.csv` | 500 | CSV (`;`) | Campanhas de marketing com métricas de performance (CTR, CPC, ROI, engajamento) |

**Colunas:** `ID`, `Campanha`, `Canal`, `Data_Inicio`, `Data_Fim`, `Objetivo`, `Segmento_Alvo`, `Investimento_R$`, `Impressoes`, `Cliques`, `CTR_%`, `CPC_R$`, `Conversoes`, `Custo_por_Conversao_R$`, `Receita_Gerada_R$`, `ROI_%`, `Alcance_Unico`, `Frequencia_Media`, `Engajamentos`, `Taxa_Engajamento_%`

---

### `class13/` — Data Storytelling 🟢

> Fonte: Baseado em relatórios públicos DataReportal, We Are Social e Statista

| Arquivo | Registros | Formato | Descrição |
|---------|-----------|---------|-----------|
| `dataset_storytelling_ready.csv` | 160 | CSV (`;`) | Dados trimestrais de plataformas digitais (2020–2024) prontos para narrativa |

**Colunas:** `Ano`, `Trimestre`, `Plataforma`, `Faixa_Etaria`, `Usuarios_Ativos_Mi`, `Tempo_Medio_Min_Dia`, `Posts_por_Usuario_Dia`, `Receita_Publicidade_Bi_US$`, `Fake_News_Detectadas_Mil`, `Satisfacao_Usuario_%`, `Crescimento_YoY_%`

---

### `class14/` — Big Data na Comunicação 🟢

> Lista 100% real de fontes de dados públicas brasileiras

| Arquivo | Registros | Formato | Descrição |
|---------|-----------|---------|-----------|
| `dataset_lista_fontes_bigdata.csv` | 15 | CSV (`;`) | Lista curada de fontes de dados públicas para pesquisa em comunicação |

**Colunas:** `ID`, `Nome_Fonte`, `URL`, `Tipo_Dados`, `Formato_Disponivel`, `Atualizacao`, `Tema_Principal`, `Dificuldade_Uso`, `Observacao`

---

## 🔗 Como Usar

### Download direto (navegador)

Navegue até o arquivo desejado no GitHub e clique em **"Download raw file"** (ícone ⬇️).

### Via URL raw (importação em ferramentas)

```
https://raw.githubusercontent.com/giovanebarcelos/datasets-big-data/refs/heads/main/classXX/nome_do_arquivo.csv
```

Substitua `classXX` e `nome_do_arquivo.csv` conforme a aula.

### Google Sheets (`IMPORTDATA`)

```
=IMPORTDATA("https://raw.githubusercontent.com/giovanebarcelos/datasets-big-data/refs/heads/main/class07/dataset_exemplo_importdata.csv")
```

### Python (pandas)

```python
import pandas as pd
url = "https://raw.githubusercontent.com/giovanebarcelos/datasets-big-data/refs/heads/main/class01/dataset_gastos_publicos.csv"
df = pd.read_csv(url, sep=";", encoding="utf-8")
```

---

## ⚙️ Geração dos Dados

Os datasets foram gerados pelo script `gerar_datasets_reais.py` com as seguintes características:

- **Linguagem:** Python 3
- **Bibliotecas:** `pandas`, `numpy`, `openpyxl`, `requests`
- **Seed:** `42` (reprodutibilidade garantida)
- **Codificação:** UTF-8
- **Separador CSV:** `;` (ponto e vírgula)

### Fontes de dados reais utilizadas

| Fonte | Datasets | URL |
|-------|----------|-----|
| Portal da Transparência | class01 | portaldatransparencia.gov.br |
| TSE Dados Abertos | class02 (eleições) | dadosabertos.tse.jus.br |
| IBGE Sidra / Cidades | class02 (censo), class10 | sidra.ibge.gov.br |
| INEP Censo Escolar | class03 (educação) | gov.br/inep |
| DATASUS TabNet | class03 (saúde) | datasus.saude.gov.br |
| consumidor.gov.br | class05 | consumidor.gov.br |
| Google Trends | class07 | trends.google.com.br |
| PNAD Contínua / IBGE | class10 | ibge.gov.br |
| DataReportal / Statista | class13 | datareportal.com |
| Diversas fontes públicas | class14 | (lista curada no dataset) |

> ⚠️ Dados pessoais (nomes, CPFs, e-mails) são 100% fictícios, mesmo nos datasets baseados em fontes reais.

---

## 📄 Licença

Este material é de uso educacional, criado para a disciplina de **Análise de Dados e Big Data**. Os dados podem ser utilizados livremente para fins acadêmicos.

---

**Giovane Barcelos** — giovane.barcelos@ulife.com.br
