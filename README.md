# Projeto-MC536
## Objetivo

O projeto tem como objetivo o cruzamento de dois datasets voltados a temas ambientais, que nos permitem analisar relações sobre a presença de unidades de conservação ambiental e a quantidade de resíduos coletados em mutirões de limpeza em corpos hídricos nas cidades brasileiras.

---

## Dados Utilizados

- **Unidades de Conservação Ambiental**
  - Usado o CNUC_2022_1ºSemestre.csv do link:
  https://dados.mma.gov.br/dataset/unidadesdeconservacao
- **Mutirões de Limpeza em Corpos Hídricos**
  - Usado o csv encontrado no link:
    https://dados.mma.gov.br/dataset/rios-mais-limpos

---

## Estrutura do Banco de Dados

O banco é composto pelas tabelas:

- unidade_de_conservacao
- mutirao_de_limpeza
- coleta_de_lixo
- bioma
- categoria_manejo
- esfera_administrativa
- instituicao_organizadora
- local_de_coleta
- municipio
- tipo_de_lixo

---

## Como Rodar

1. Clone este repositório.
2. Certifique-se de instalar o `pandas` e o `psycopg2` para o funcionamento do projeto, pois os seguintes imports são necessários:
```python
import pandas as pd
import psycopg2
from psycopg2 import sql
from io import StringIO
```
3. Abra o script codigo_completo (ele já conterá os imports acima).
4. Na parte de conectar com o banco, passe os parâmetros de connect conforme o seu banco.
```python
from psycopg2 import sql
conn = psycopg2.connect(dbname = "", user = "postgres", password = "", host = "localhost", port = "5432")
cursor = conn.cursor()
```
5. Execute o script.
6. Use as queries SQL disponíveis para análise ou fique a vontade para criar outras.

---

## Ferramentas Utilizadas

- Python (pandas, psycopg2)
- PgAdmin4
- Jupyter Notebook
- Draw.io
  
---

## Algumas Conclusões e Insights

- O estado do Amazonas foi um dos com mais lixo extraido, e é disparado o que possui mais unidades de conservação.
- De 2019 a 2022, 2021 foi disparadamente o ano com mais extração de lixo, com a duração total dos mutirões sendo muito superior a qualquer outro.
- Dos biomas brasileiros, a amazônia foi o que teve mais lixo coletado, com foco em plástico e garrafas pets.
- Os mutirões organizados por instituições públicas são os mais eficientes entre todos, já os voluntarios e privados foram muito pouco eficientes.

---

## Autores

Projeto desenvolvido por:  
- Gabriel dos Santos Souza - 269844  
- Pedro Gomes Ascef - 257086 
- Rafael Attilio Agricola - 249245 
