# 🤖 Projeto Integrado – Aprendizado por Reforço Aplicado ao Mercado Financeiro

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Este projeto foi desenvolvido como parte do **MBA em Ciência de Dados e Inteligência Artificial** da **FIAP** pela turma **9DTSR**, com foco em aplicar técnicas de **Reinforcement Learning (RL)** para decisões automatizadas de compra e venda de ações.

Utilizamos **Deep Q-Network (DQN)** para treinar um agente capaz de operar no mercado com base em dados históricos dos ativos **VALE3.SA**, **PETR4.SA** e **BRFS3.SA**.

---

## 🎯 Objetivo

Desenvolver um agente de RL capaz de **decidir entre comprar, vender ou manter** ações com base em estados do mercado financeiro, visando:

- Maximizar retorno acumulado
- Reduzir risco com decisões otimizadas
- Automatizar estratégias de investimento com IA

---

## 📊 Dados Utilizados

Os dados foram obtidos por meio da biblioteca `yfinance`, com o período de **01/01/2022 a 31/12/2024** e representam os preços ajustados dos ativos:

- VALE3.SA (Vale)
- PETR4.SA (Petrobras)
- BRFS3.SA (Brasil Foods)

---

## 🧠 Definição do Ambiente de RL

| Componente | Descrição |
|------------|-----------|
| **Estados** | Preço atual dos ativos, posições em carteira, saldo disponível, indicadores técnicos |
| **Ações**   | Comprar, Vender ou Manter (por ativo, com base em saldo/estoque) |
| **Recompensas** | Lucro/prejuízo obtido após cada ação, baseado na variação patrimonial |

---

## 🧪 Treinamento do Agente

Utilizamos o algoritmo **DQN (Deep Q-Network)** do pacote `stable-baselines3`, com arquitetura MLP (Multilayer Perceptron) e os seguintes parâmetros principais:

- **Política:** `MlpPolicy`
- **Total timesteps:** `50.000`
- **Exploração final (epsilon):** `0.05`

Durante o treinamento, o agente:

- Aprende a maximizar as recompensas acumuladas
- Explora diferentes estratégias até consolidar sua política ótima
- Mostra sinais de aprendizado com aumento consistente do patrimônio

---

## 📈 Resultados

- O agente partiu com **R$10.000** e alcançou um patrimônio superior a **R$13.500**
- Demonstrou aprendizado real, com decisões eficazes e sustentadas
- Foi avaliado com base em métricas como **retorno total**, **índice de Sharpe** e **máximo drawdown**

---

## 🔍 Principais Conclusões

- **RL é promissor** na automação de investimentos, com capacidade adaptativa e tomada de decisão autônoma
- É fundamental aplicar técnicas de **validação robusta** e **controle de risco**
- Ajustes finos de hiperparâmetros e maior volume de dados podem melhorar a estabilidade e desempenho do agente

---

## 🛠️ Tecnologias e Bibliotecas

- Python 3.11+
- [stable-baselines3](https://github.com/DLR-RM/stable-baselines3)
- yfinance
- pandas / numpy / matplotlib

---

## 👥 Autores

- **Jéssica Portela de Castro** – RM: 359735  
- **Tiago Freire Barbosa** – RM: 358404

Projeto desenvolvido para a disciplina de **Aprendizado por Reforço** no MBA FIAP – Quantum Finance.

---

## 📜 Licença

Distribuído sob a licença [MIT](LICENSE).  
Uso livre para fins acadêmicos, pessoais e de pesquisa.

---

## 📚 Referência

> TATSAT, Hariom; PURI, Sahil; LOOKABAUGH, Brad. *Blueprints de aprendizado de máquina e ciência de dados para finanças: desenvolvendo desde estratégias de trades até robôs advisors com Python*. Rio de Janeiro: Alta Books, 2021.

---

## 🔖 Tags

`#ReinforcementLearning` `#DQN` `#FIAP` `#MercadoFinanceiro` `#QuantumFinance` `#MachineLearning` `#StableBaselines3` `#YFinance` `#OpenSource`
