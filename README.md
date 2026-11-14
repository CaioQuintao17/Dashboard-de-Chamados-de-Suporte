# Dashboard de Chamados de Suporte (Power BI)

## Problema
Como medir o tempo de resolução e o volume de chamados de um suporte de TI, pra identificar onde a equipe deveria focar.

## Dados
Base simulada com 4.000 chamados de janeiro a junho de 2026, com categoria, prioridade, status e datas de abertura e fechamento. Os dados são fictícios e não representam informações reais de nenhuma empresa.

## Ferramentas
- Power BI Desktop
- Power Query (limpeza e tipos de dados)
- DAX (medidas e colunas calculadas)

## Tratamento e modelagem
- **Power Query:** conversão de tipos de data e criação da coluna de tempo de resolução
- **DAX:** tabela calendário, colunas auxiliares de data, ordenação dos dias da semana e medida de tempo médio de resolução

## Principais números
- Total de chamados: 4.000
- Tempo médio de resolução: 5,53 horas

## Insights
1. **"Outros" e "Criação de usuário" são as categorias mais lentas.** Levam em média cerca de 9,7 e 8,3 horas, quase o triplo de VPN (cerca de 3 horas). Isso sugere que esses chamados precisam de um roteiro de atendimento mais claro, ou de mais autonomia pra quem atende.

2. **O volume se concentra nos dias úteis.** Segunda a sexta têm quase 750 chamados cada, enquanto sábado e domingo somam menos de 250, cerca de 6% do total. Isso ajuda a dimensionar a escala da equipe, já que o trabalho fica concentrado de segunda a sexta.

3. **A média geral esconde a diferença entre categorias.** O tempo médio de 5,53 horas parece razoável, mas as categorias variam de 3 a quase 10 horas. Por isso olhar o indicador por categoria muda a decisão, e a média sozinha não basta.

## Dashboard
![Dashboard](dashboard.png)

## Como reproduzir
1. Abra o arquivo `dashboard.pbix` no Power BI Desktop
2. Os dados estão em `chamados.csv`, caso queira refazer a importação
