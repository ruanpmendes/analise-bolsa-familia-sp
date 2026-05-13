# 📊 Análise de Distribuição: Bolsa Família SP (2025 - 2026)

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Microsoft Power BI](https://img.shields.io/badge/Microsoft_Power_BI-F2C811?style=for-the-badge&logo=microsoft-power-bi&logoColor=black)

🔗 Clique na imagem para interagir com o projeto completo  
<a href="https://app.fabric.microsoft.com/view?r=eyJrIjoiNjJjYmE1ZWEtOGI3ZC00Y2U3LTk1MTQtYWUwNTlkMDA5MGVhIiwidCI6ImQ0ZjBiOGY0LTQ2NTAtNDNmYi05YWFiLWE1YmM4OGRkMDM0NSJ9" target="_blank">
    <img width="1481" height="830" alt="image" src="https://github.com/user-attachments/assets/86f162ea-41a3-4ae0-89e8-da3a82983cfe" />
</a>

> Pipeline de ETL e visualização de dados focado em analisar a distribuição de R$ 22,62 Bilhões do programa Bolsa Família no estado de São Paulo, cobrindo o período de Janeiro de 2025 a Março de 2026.

## 🎯 Objetivo do Projeto
O objetivo deste projeto é mapear e entender como os recursos do Bolsa Família estão sendo distribuídos geograficamente pelo estado de São Paulo. Ao invés de olhar apenas para totais brutos, a análise foca em responder perguntas estruturais: 
- Qual a diferença de repasse entre a Capital/Região Metropolitana e o Interior? 
- Quais cidades apresentam o maior Ticket Médio real por família?
- Como a sazonalidade e o volume se comportam ao longo dos meses?

## 🛠️ Stack Tecnológica
- **Processamento & ETL:** Python (Pandas)
- **Visualização de Dados:** Microsoft Power BI
- **Ambiente:** Jupyter Notebook / VS Code

## 📂 Estrutura dos Dados
Os dados englobam pagamentos realizados em todo o estado de São Paulo.
- **Período:** Janeiro/2025 a Março/2026.
- **Volume:** R$ 22,62 Bi distribuídos para mais de 2,79 Milhões de beneficiários.
- **Principais Variáveis Trabalhadas:** `NOME MUNICÍPIO`, `VALOR PARCELA`, `MÊS COMPETÊNCIA`, `NIS FAVORECIDO`.

## ⚙️ Pipeline e Metodologia Aplicada
O script em Python foi desenhado para garantir integridade estatística antes que os dados chegassem ao dashboard:
1. **Agrupamento de Volume (Sum):** Cálculo do total absoluto de recursos por município.
2. **Tratamento de Outliers (Ticket Médio):** Para evitar que cidades minúsculas distorcessem a média com tickets artificialmente altos, foi aplicado um filtro rigoroso (`QTD_FAVORECIDOS >= 1000`), garantindo que apenas municípios com amostragem relevante entrassem no ranking de Ticket Médio.
3. **Clusterização Geográfica:** Criação de uma lista de controle contendo 21 municípios da Região Metropolitana de São Paulo para segmentar dinamicamente os montantes financeiros entre "Capital/Metropolitana" e "Interior".

## 💡 Principais Insights e Resultados
A junção do tratamento em Python com o dashboard no Power BI revelou:
1. **Predominância do Interior:** Contrariando o senso comum de que a capital concentraria esmagadoramente os repasses, o Interior lidera a recepção de fundos (R$ 12 Bi) em comparação com a Capital e Região Metropolitana combinadas (R$ 11 Bi).
2. **Concentração Absoluta:** O município de São Paulo, de forma isolada, é o destino de R$ 6,3 Bi do montante total.
3. **Variação do Ticket Médio:** A média estadual do benefício é de **R$ 672,78**. No entanto, o ranking de maiores tickets é amplamente dominado por cidades do interior, como Vargem Grande do Sul (R$ 715,53) e São Vicente (R$ 711,43).
4. **Estabilidade de Distribuição:** A linha de tendência temporal mostra uma distribuição consistente ao longo do ano, com picos discretos em Maio e um vale no mês de Novembro de 2025.

## 🚀 Como Executar o Projeto

**Pré-requisitos:** Python 3.9+, Pandas, Power BI Desktop.

1. Clone este repositório:
   
   git clone https://github.com/ruanpmendes/analise-bolsa-familia-sp

2. Instale as dependências necessárias do Python:

    pip install pandas

3. Execute o script de análise exploratória:

    python scripts/analise_bolsa_familia.py


🤝 Autor
Ruan Mendes - https://www.linkedin.com/in/ruan--mendes/
   