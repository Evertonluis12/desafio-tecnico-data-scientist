## Teste realizado com threshold = 0.6 e 0.7

## Ajuste de Threshold e Impacto nos Resultados

Durante os testes, observei o impacto do threshold na classificação dos matches.

- Com threshold = 0.7:
  - menor quantidade de matches
  - maior rigor na aceitação
  - maior número de `no_match`

- Com threshold = 0.6:
  - maior quantidade de matches
  - maior cobertura
  - maior risco de matches menos precisos

Esse comportamento evidencia o trade-off entre precisão e cobertura, sendo o threshold um parâmetro crítico que deve ser ajustado de acordo com o objetivo do sistema.


----------------------------------------------------------------------------------


## Estratégia de Avaliação de Qualidade

Como não é viável rotular manualmente milhares de skills, a qualidade do mapeamento pode ser avaliada por meio de estratégias indiretas:

### 1. Distribuição dos Scores
Analisar a distribuição dos valores de similaridade (confidence_score). Scores muito baixos indicam baixa confiança nos matches, enquanto scores altos indicam maior proximidade semântica.

### 2. Análise de Threshold
O threshold (ex: 0.7) pode ser ajustado com base em amostras validadas manualmente, equilibrando precisão e cobertura.

### 3. Amostragem Manual
Selecionar amostras aleatórias e validar manualmente os matches para estimar a precisão do modelo.

### 4. Monitoramento Contínuo
Em produção, monitorar:
- % de no_match
- média dos scores
- distribuição dos matches por skill

### 5. Feedback do Usuário
Incorporar feedback de usuários para corrigir mapeamentos incorretos e melhorar continuamente o sistema.




## 📁 Outputs gerados

Os resultados do mapeamento foram exportados para a pasta `outputs/`, incluindo:

- `output_mapping_threshold_0.6.csv`
- `output_mapping_threshold_0.7.csv`

Isso permite comparar o impacto do threshold na qualidade dos matches.