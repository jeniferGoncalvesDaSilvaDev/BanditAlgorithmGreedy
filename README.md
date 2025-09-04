# 🎰 Algoritmo ε-Greedy Interativo

Uma aplicação web interativa que demonstra o algoritmo ε-Greedy, uma estratégia fundamental de aprendizado por reforço usado em problemas de Multi-Armed Bandit.

## 📋 Sobre o Projeto

Este projeto implementa uma simulação visual do algoritmo ε-Greedy, permitindo que usuários experimentem com diferentes parâmetros e vejam em tempo real como o algoritmo equilibra **exploração** (testar novas opções) e **explotação** (usar a melhor opção conhecida).

### 🎯 O Problema Multi-Armed Bandit

Imagine que você está em um cassino com várias máquinas caça-níqueis (bandits), cada uma com uma probabilidade diferente de dar prêmio. Seu objetivo é maximizar seus ganhos, mas você não sabe qual máquina é a melhor. Você precisa:

- **Explorar**: Testar diferentes máquinas para descobrir qual é melhor
- **Explotar**: Usar a máquina que parece ser a melhor até agora

O algoritmo ε-Greedy resolve este dilema usando uma estratégia simples mas eficaz.

## 🚀 Como Usar

1. **Acesse a aplicação**: Abra o arquivo `index.html` em um navegador moderno
2. **Ajuste os parâmetros**:
   - **k**: Número de alavancas/opções (2-50)
   - **T**: Número de tentativas (100-5000)
   - **ε inicial**: Probabilidade de exploração (0.1-10.0)
3. **Execute**: Clique em "🚀 Executar Simulação"
4. **Analise**: Observe os gráficos de regret e ações ótimas

## 📊 Interpretando os Resultados

### Gráfico 1: Regret Acumulado
- **O que mostra**: O "arrependimento" médio por não escolher sempre a melhor opção
- **Tendência ideal**: Deve diminuir ao longo do tempo
- **Interpretação**: Valores menores = algoritmo está aprendendo melhor

### Gráfico 2: Ações Ótimas (%)
- **O que mostra**: Porcentagem de vezes que o algoritmo escolheu a melhor opção
- **Tendência ideal**: Deve aumentar ao longo do tempo
- **Interpretação**: Valores maiores = algoritmo está melhorando suas decisões

## 🔬 Como Funciona o Algoritmo ε-Greedy

```python
# Pseudocódigo simplificado
for cada tentativa t:
    if random() < ε:
        # EXPLORAÇÃO: escolha uma alavanca aleatória
        alavanca = escolha_aleatoria()
    else:
        # EXPLOTAÇÃO: escolha a melhor alavanca conhecida
        alavanca = melhor_alavanca_atual()
    
    recompensa = puxar_alavanca(alavanca)
    atualizar_estimativas(alavanca, recompensa)
    
    # Reduzir ε ao longo do tempo (mais explotação)
    ε = ε * fator_decaimento
```

### Parâmetros Principais

- **ε (epsilon)**: Controla o equilíbrio exploração/explotação
  - ε alto = mais exploração (arriscado, mas pode encontrar melhores opções)
  - ε baixo = mais explotação (conservador, usa conhecimento atual)
  
- **Decaimento de ε**: O valor de ε diminui ao longo do tempo
  - Início: Mais exploração para descobrir as opções
  - Final: Mais explotação para maximizar ganhos

## 🛠️ Tecnologias Utilizadas

- **HTML5**: Estrutura da interface
- **CSS3**: Estilização responsiva e moderna
- **PyScript**: Execução de Python no navegador
- **Matplotlib**: Geração de gráficos interativos
- **NumPy**: Cálculos matemáticos e estatísticos

## 📁 Estrutura do Projeto

```
├── index.html          # Aplicação principal
├── README.md           # Este arquivo
└── replit.md          # Documentação técnica do projeto
```

## 🎮 Experimentos Sugeridos

### Experimento 1: Efeito do ε inicial
- Execute com ε = 0.1, 1.0, e 5.0
- Observe como valores diferentes afetam a velocidade de aprendizado

### Experimento 2: Número de alavancas
- Compare k = 5 vs k = 20
- Veja como mais opções tornam o problema mais difícil

### Experimento 3: Duração da simulação
- Execute com T = 500 vs T = 2000
- Observe como mais tentativas melhoram o desempenho

## 📚 Conceitos de Aprendizado por Reforço

Este projeto demonstra conceitos fundamentais:

- **Multi-Armed Bandit**: Problema clássico de tomada de decisão
- **Exploration vs Exploitation**: Dilema fundamental em IA
- **Regret**: Métrica para avaliar qualidade das decisões
- **ε-Greedy Strategy**: Algoritmo simples mas eficaz
- **Convergência**: Como algoritmos melhoram ao longo do tempo

## 🔄 Como Executar Localmente

1. Clone ou baixe o projeto
2. Abra `index.html` em um navegador moderno
3. Aguarde o PyScript carregar (pode levar alguns segundos)
4. Comece a experimentar!

**Requisitos**: Navegador moderno com suporte a WebAssembly (Chrome, Firefox, Safari, Edge)

## 🎓 Aplicações Práticas

O algoritmo ε-Greedy é usado em:

- **Recomendações online**: Testar novos produtos vs recomendar favoritos
- **Testes A/B**: Equilibrar coleta de dados com performance
- **Publicidade**: Escolher anúncios para maximizar cliques
- **Games**: NPCs que aprendem estratégias
- **Robótica**: Explorar ambiente vs usar conhecimento atual

## 📈 Métricas de Performance

A aplicação calcula automaticamente:

- **Regret médio final**: Qualidade geral das decisões
- **% de ações ótimas final**: Eficácia do aprendizado
- **Convergência visual**: Através dos gráficos ao longo do tempo

## 🤝 Créditos

Baseado no trabalho de: https://github.com/petroud/E-greedy_and_UCB_algorithms/

## 📄 Licença

Este projeto é educacional e está disponível para uso livre em contextos acadêmicos e de aprendizado.

---

**Desenvolvido para ensinar conceitos de Aprendizado por Reforço de forma visual e interativa** 🎯