# Dashboard de Clientes

Dashboard em um único arquivo HTML, com gráficos, estatísticas de preços e datas, importação de planilhas e exportação de relatórios.

## Como usar

1. Abra `dashboard-clientes.html` no navegador (Chrome, Edge, Firefox ou Safari). É preciso estar online, pois as bibliotecas são carregadas por CDN.
2. O dashboard abre com 15 clientes de exemplo.
3. Clique em **Importar Excel / CSV** para carregar a sua própria planilha.
4. Clique em **Dados de exemplo** para voltar aos dados originais.

## Formato da planilha

A primeira linha deve conter os cabeçalhos. A coluna **Valor** é obrigatória; as demais são recomendadas.

| Coluna  | Exemplo                | Observação                                      |
|---------|------------------------|-------------------------------------------------|
| ID      | 1                      | Se não existir, é numerado automaticamente      |
| Nome    | Ana Beatriz Souza      | Também aceita o cabeçalho "Cliente"             |
| Produto | Notebook Dell          | Também aceita o cabeçalho "Item"                |
| Valor   | 3899,90 ou R$ 3.899,90 | Aceita número ou texto no formato brasileiro    |
| Data    | 02/09/2026             | Aceita DD/MM/AAAA, AAAA-MM-DD e datas do Excel  |

Formatos aceitos: `.xlsx`, `.xls` e `.csv` (separado por vírgula ou ponto e vírgula). Apenas a primeira aba é lida.

## O que o dashboard mostra

**Estatísticas de preços:** total, ticket médio, mediana, maior e menor valor, desvio padrão e número de registros.

**Estatísticas de datas:** primeira e última data, período, intervalo médio entre compras, mês de maior faturamento e dia da semana com mais compras.

**Gráficos:** valor por cliente, valor por data, distribuição por faixa de preço e faturamento por mês.

## Exportação

| Botão        | Arquivo                  | Conteúdo                                   |
|--------------|--------------------------|--------------------------------------------|
| Salvar PDF   | `dashboard-clientes.pdf` | Estatísticas, gráficos e tabela de dados   |
| Salvar CSV   | `dashboard-clientes.csv` | Tabela de dados (`;` como separador, UTF-8)|
| Salvar Word  | `dashboard-clientes.docx`| Estatísticas e tabela de dados (sem gráficos) |

> Os botões de exportação só funcionam na versão publicada no Claude. No arquivo HTML aberto localmente, eles ficam desativados.

## Tecnologias

Chart.js (gráficos), SheetJS (leitura de Excel), jsPDF e jsPDF-AutoTable (PDF) e JSZip (geração do Word). Todas são carregadas por CDN.

## Observações

- Os dados importados ficam apenas no navegador e não são enviados a nenhum servidor.
- Linhas sem um valor numérico válido são ignoradas na importação.
- Os dados de exemplo são fictícios.
