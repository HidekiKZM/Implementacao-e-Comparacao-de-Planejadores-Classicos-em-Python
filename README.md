## 🤖 Projeto: Planejamento Clássico em IA - Logística Universitária

Este projeto, desenvolvido para a disciplina de Planejamento Inteligente e Raciocínio Automático da Pós-Graduação em Inteligência Artificial, foca na implementação e análise comparativa de três algoritmos clássicos de planejamento: **STRIPS**, **Graphplan** e **SATPlan**.

### 🎯 O Desafio

O objetivo foi criar um planejador capaz de resolver um problema complexo de logística em uma rede universitária distribuída. O cenário envolve o transporte de pacotes entre diferentes cidades, utilizando dois tipos de veículos:

* **Caminhões:** Para transporte terrestre *dentro* de uma mesma cidade (entre prédios e aeroportos locais).
* **Aviões:** Para transporte aéreo *entre* cidades (conectando os aeroportos).

A meta é encontrar a sequência ótima de ações (`load`, `unload`, `drive`, `fly`) para levar todos os pacotes de suas origens aos seus respectivos destinos.

### 🔧 Implementação

O projeto foi dividido em três entregáveis principais:

1.  **Modelagem do Domínio (`domain.pddl`)**: Criação de um domínio PDDL em formato STRIPS puro, capaz de modelar as ações e restrições do problema de logística.
2.  **Implementação dos Planejadores (Python)**:
    * **Planejador STRIPS**: Utilizando busca *forward* (como BFS ou A*).
    * **Planejador Graphplan**: Com construção de grafo de planejamento, detecção de *mutex* e extração de plano regressiva.
    * **Planejador SATPlan**: Com codificação do problema para Fórmulas Booleanas (CNF) e uso de um *solver* SAT externo.
3.  **Análise Experimental**: Comparação do desempenho dos três planejadores em diferentes instâncias do problema, avaliando métricas como tempo de execução, tamanho do plano e nós expandidos.
