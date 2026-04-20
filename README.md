# Desafio Técnico — Mapeamento de Skills

## 📌 Objetivo

Este projeto tem como objetivo mapear skills brutas para uma taxonomia padronizada, utilizando similaridade semântica.

---

## ⚙️ Abordagem

A solução utiliza embeddings para representar semanticamente os textos e cosine similarity para encontrar a skill mais próxima na taxonomia.

Etapas principais:
1. Limpeza dos textos com pandas basica 
2. Criação de embeddings
3. Cálculo de similaridade
4. Seleção do melhor match
5. Aplicação de threshold para validação

---

## 🧠 Decisões Técnicas

- Uso de embeddings para capturar semântica
- Modelo multilingual para lidar com português e inglês
- Cosine similarity para comparação e alinhamento vetorial
- Threshold para evitar matches de baixa confiança

---

## 📊 Avaliação de Qualidade

A qualidade pode ser medida por:
- Distribuição dos scores
- Amostragem manual
- Ajuste de threshold
- Monitoramento contínuo em produção

---

## 📁 Output

O resultado final é salvo em: output_mapping.csv

Contendo:
- new_skill_id
- skill_raw
- taxonomy_id
- skill_name
- confidence_score
- match_status

---

## 🚀 Execução

```bash
pip install -r requirements.txt

Executar o notebook:
solution.ipynb

## 🛠️ Melhorias Futuras

- Ajuste dinâmico de threshold
- Uso de modelos mais robustos
- Feedback humano no loop