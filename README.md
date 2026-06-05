# 🛍️ Sistema de Recomendação de Roupas com Filtragem Colaborativa

## 📋 Descrição do Projeto
Este projeto foi desenvolvido como requisito avaliativo de nivelamento (**Avaliação N1**) para a disciplina de **Machine Learning** do curso de **Bacharelado em Ciência da Computação (BCC)**, sob a orientação do **Professor Luciano Tadeu Pereira**.

O sistema consiste em um motor de recomendação baseado no algoritmo de **Filtragem Colaborativa Baseada em Itens (Item-Based Collaborative Filtering)** utilizando a métrica matemática de **Similaridade Cosseno**. O objetivo principal é sugerir de forma inteligente e preditiva peças de roupas a usuários finais baseando-se no padrão comportamental de consumo histórico de toda a base de clientes do e-commerce.

---

## 👥 Integrantes do Grupo
* **Arthur Santos Alves** - RA: `2025115208`
* **Luiz Carlos Fernandes Silva** - RA: `2025116655`
* **Miguel Poquini Lopes** - RA: `2025106744`
* **Tiago Felix da Silva** - RA: `2025108302`

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas
* **Linguagem:** Python 3.x
* **Ambiente Principal:** Google Colab
* **Manipulação de Dados:** `pandas`, `numpy`
* **Machine Learning & Pré-processamento:** `scikit-learn`
* **Visualização de Dados:** `matplotlib`, `seaborn`

---

## ⚙️ Arquitetura do Pipeline de ML (Artefatos de Entrega)

O notebook encontra-se compartimentado em **20 células lógicas** estruturadas de forma sequencial, cobrindo os seguintes artefatos técnicos exigidos para o ciclo completo de Machine Learning:

1. **Artefato 1 — Engenharia de Dados (Células 4 a 6):** Engenharia aplicada em dados sintéticos que simulam as interações de 150 clientes e 12 tipos de peças de roupas. Aplica tratamento de ausências por imputação estatística da mediana e normalização de escala por `MinMaxScaler` na janela padrão de $[0,1]$.
2. **Artefato 2 — Validação e Split (Células 7 e 8):** Divisão do dataset em Holdout (80% Treino / 20% Teste) para mitigar o risco de *data leakage* (vazamento de dados) e aplicação de validação cruzada robusta com `K-Fold (5 Splits)` para analisar a estabilidade da dispersão vetorial.
3. **Artefato 3 — Treinamento do Modelo (Células 9 e 10):** Treinamento da Matriz de Similaridade Cosseno mapeando a proximidade vetorial e correlação de preferência de cada peça de roupa em relação às outras.
4. **Artefato 4 — Motor de Inferência (Células 11 e 12):** Função preditiva parametrizável construída para realizar recomendações em tempo real ordenadas por score de relevância, contendo um filtro automático de exclusão para produtos previamente adquiridos pelo usuário ativo.
5. **Artefatos 5, 6 e 7 — Avaliação Estatística e Visualização (Células 13 e 14):** Binarização e extração de métricas de classificação tradicionais (`Acurácia`, `Precisão`, `Recall` e `F1-Score`) geradas no ambiente isolado de testes. Plotagem gráfica da `Matriz de Confusão` e do `Heatmap de Similaridade`.
6. **Camada Nova — Inteligência de Negócios e Segmentação (Células 16 e 17):** Classificação analítica do portfólio de produtos através de regras de engajamento, agrupando as roupas entre itens de *Alta Conversão (Best Sellers)*, *Boa Aceitação (Nicho)* ou *Baixo Giro (Alerta de Estoque)*.
7. **Camada Nova — Diagnóstico de Infraestrutura (Células 18 e 19):** Medição matemática do nível de esparsidade e densidade da matriz para prever gargalos em bancos de dados relacionais e garantir a confiabilidade dos vizinhos mais próximos.
8. **Visualização Avançada Expandida (Célula 20):** Gráfico de barras horizontal categorizado por paleta de cores (*viridis*) mapeando a volumetria absoluta de interações e o status de mercado de cada peça de roupa.
9. **Artefato 8 — Conclusão Geral Consolidada (Célula de Fechamento):** Análise analítica e autoexplicativa sobre o comportamento do modelo quanto a Overfitting/Underfitting, pontos fortes da arquitetura e mapeamento de limitações de engenharia.

---

## 🚀 Como Executar o Projeto

1. Faça o clone deste repositório na sua máquina local ou ambiente de preferência:
   ```bash
   git clone [https://github.com/miguelpoquini-eng/AVALIACAO-N1-APRENDIZADO-DE-MAQUINA.git](https://github.com/miguelpoquini-eng/AVALIACAO-N1-APRENDIZADO-DE-MAQUINA.git)
