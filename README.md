# Mercado de Restaurantes em Los Angeles – Estudo Estratégico para Cafeteria com Garçons Robôs

Este projeto avalia o mercado de restaurantes em Los Angeles com o objetivo de validar a viabilidade de abrir uma cafeteria com garçons robôs e atrair investidores.

A pergunta central é:

> Existe espaço sustentável no mercado quando o fator novidade deixar de ser diferencial?

---

# 🎯 Objetivo

- Entender a estrutura do mercado de restaurantes em LA.
- Identificar padrões de rede vs estabelecimentos independentes.
- Avaliar tamanho médio dos restaurantes.
- Analisar concentração geográfica.
- Definir posicionamento ideal (tipo + tamanho + estratégia de expansão).

---

# 📂 Base de Dados

Arquivo:

`/datasets/rest_data_us_upd.csv`

Colunas:

- object_name — nome do estabelecimento  
- chain — pertence a rede (TRUE/FALSE)  
- object_type — tipo de restaurante  
- address — endereço  
- number — número de assentos  

---

# 1️⃣ Preparação dos Dados

### Etapas realizadas:

- Importação com Pandas
- Conversão correta de tipos:
  - `chain` → boolean
  - `number` → numérico
- Tratamento de valores ausentes
- Remoção de duplicatas
- Padronização de nomes de tipos
- Extração do nome da rua da coluna `address`

Criação de nova coluna:

- `street_name`

Essa etapa é crítica para evitar distorções nas análises geográficas.

---

# 2️⃣ Análise de Mercado

---

## 📊 1. Proporção por tipo de estabelecimento

Análise da distribuição de:

- Restaurant
- Cafe
- Fast Food
- Bar
- Bakery
- Outros

Gráfico: barra ou pizza.

Objetivo:
Entender saturação por categoria.

---

## 📊 2. Proporção de redes vs independentes

Gráfico comparando:

- Estabelecimentos de rede
- Estabelecimentos independentes

Pergunta estratégica:
O mercado é dominado por grandes marcas ou pequenos operadores?

---

## 📊 3. Tipo mais comum entre redes

Análise cruzada:

`object_type` × `chain`

Objetivo:
Identificar padrão típico de expansão.

Tendência esperada:
Fast food e cafés tendem a dominar redes.

---

## 📊 4. Estrutura das redes

Pergunta:

Redes possuem:
- Muitos estabelecimentos pequenos?
ou
- Poucos estabelecimentos grandes?

Análise:

- Média de assentos por tipo (rede vs não rede)
- Distribuição do número de assentos

---

## 📊 5. Número médio de assentos por tipo

Cálculo:

Média de `number` agrupada por `object_type`.

Gráfico comparativo.

Pergunta-chave:

Qual formato exige maior investimento estrutural?

---

## 📍 6. Análise Geográfica

### Extração de ruas

Separação do nome da rua da coluna `address`.

---

### 📊 7. Top 10 ruas com mais restaurantes

Gráfico de barras com:

- Rua
- Número de estabelecimentos

Objetivo:
Identificar zonas de alta competição.

---

### 📊 8. Ruas com apenas 1 restaurante

Contagem de ruas únicas.

Pergunta estratégica:
Existe espaço para diferenciação fora dos polos saturados?

---

### 📊 9. Distribuição de assentos nas ruas mais concorridas

Análise da dispersão:

- Restaurantes são majoritariamente pequenos?
- Grandes players dominam?

---

# 📈 Insights Estratégicos

Análise combinada para responder:

1. Qual tipo de restaurante é mais comum?
2. Redes dominam quais categorias?
3. Restaurantes maiores estão concentrados onde?
4. Existe espaço para modelo boutique?
5. Mercado favorece escala ou diferenciação?

---

# 🧠 Conclusão Estratégica para Investidores

A conclusão aborda:

- Tipo recomendado (ex: cafeteria vs restaurante completo)
- Tamanho ideal (ex: 30–50 assentos vs 100+)
- Localização estratégica (zona saturada vs emergente)
- Potencial de expansão em rede
- Risco de comoditização após perda do fator novidade

A recomendação final considera:

- Estrutura competitiva
- Intensidade de capital
- Padrão de expansão do mercado
- Sustentabilidade operacional

---

## 📦 Como Executar

1. Clone o repositório:

```bash
git clone https://github.com/rodriguesbrian/tt10_restaurants_project
cd tt10_restaurants_project