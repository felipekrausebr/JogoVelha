<h1 align="center">
🎮 Jogo da Velha 4x4 com Minimax em Python
</h1>

<p align="center">
Projeto acadêmico desenvolvido utilizando o algoritmo Minimax para implementação de uma Inteligência Artificial em um jogo da velha 4x4.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue" />
  <img src="https://img.shields.io/badge/IA-Minimax-green" />
  <img src="https://img.shields.io/badge/Projeto-Acadêmico-orange" />
</p>

---

# 📌 Objetivo

O objetivo deste projeto é implementar uma Inteligência Artificial utilizando o algoritmo **Minimax** para jogar uma versão 4x4 do jogo da velha.

O sistema permite que:

- o jogador humano jogue contra a IA
- a IA analise possíveis jogadas
- a melhor decisão seja escolhida utilizando Minimax

---

# 🧠 Sobre o Algoritmo Minimax

O algoritmo Minimax é amplamente utilizado em jogos de tomada de decisão.

Ele funciona simulando todas as possíveis jogadas futuras para:

- maximizar as chances da IA vencer
- minimizar as chances do adversário vencer

O algoritmo assume que:

- a IA sempre fará a melhor jogada possível
- o jogador humano também fará a melhor jogada possível

---

# 🎮 Sobre o Jogo

O jogo implementado é uma versão do jogo da velha em um tabuleiro 4x4.

## Regras

- O jogador humano utiliza o símbolo `O`
- A IA utiliza o símbolo `X`
- Vence quem completar:
  - 4 símbolos em linha
  - 4 símbolos em coluna
  - 4 símbolos na diagonal

---

# ⚙️ Funcionamento do Projeto

O projeto é dividido em diversas funções responsáveis pela lógica do jogo e da IA.

---

# 🏗️ Estrutura do Código

## 1️⃣ Criação do Tabuleiro

A função cria uma matriz 4x4 vazia.

```python
def criar_tabuleiro():
    return [[VAZIO for _ in range(TAMANHO)] for _ in range(TAMANHO)]
```

---

## 2️⃣ Impressão do Tabuleiro

Responsável por exibir o jogo no terminal.

Exemplo:

```bash
    0   1   2   3
  +---+---+---+---+
0 | X | O |   |   |
  +---+---+---+---+
1 |   | X |   |   |
  +---+---+---+---+
```

---

## 3️⃣ Verificação de Jogadas Possíveis

A função percorre o tabuleiro e identifica posições vazias.

```python
def jogadas_possiveis(tabuleiro):
```

---

## 4️⃣ Verificação de Vitória

O algoritmo verifica:

- linhas
- colunas
- diagonais

para identificar um vencedor.

```python
def verificar_vencedor(tabuleiro):
```

---

## 5️⃣ Função de Utilidade

A função atribui valores ao estado do jogo:

| Situação | Valor |
|---|---|
| Vitória da IA | +10 |
| Vitória do jogador | -10 |
| Empate | 0 |

---

# 🧬 Algoritmo Minimax

A principal lógica de Inteligência Artificial está implementada na função:

```python
def minimax(tabuleiro, jogador, profundidade):
```

---

# 📌 Funcionamento do Minimax

O algoritmo:

1. Simula todas as jogadas possíveis
2. Avalia os resultados futuros
3. Escolhe a melhor jogada possível

A IA tenta:

- maximizar sua pontuação
- minimizar a pontuação do adversário

---

# 📉 Profundidade Máxima

Foi utilizada uma profundidade máxima de:

```python
PROFUNDIDADE_MAXIMA = 4
```

Isso reduz o custo computacional da busca.

Sem limite de profundidade, o algoritmo poderia ficar muito lento devido à quantidade de possibilidades do tabuleiro 4x4.

---

# 🚀 Escolha da Melhor Jogada

A função:

```python
def melhor_jogada_minimax(tabuleiro):
```

é responsável por:

- testar todas as jogadas possíveis
- chamar o algoritmo Minimax
- escolher a jogada com maior valor

---

# 📊 Indicadores de Desempenho

Durante a execução, o programa exibe:

- número de nós avaliados
- tempo de execução
- melhor jogada encontrada
- valor da jogada

Exemplo:

```bash
Indicadores de desempenho:
Número de nós avaliados: 1250
Tempo de execução: 0.134 segundos
Melhor jogada encontrada: (1, 2)
Valor da jogada: 10
```

---

# 🛠️ Tecnologias Utilizadas

- Python 3
- Biblioteca `math`
- Biblioteca `time`

---

# ▶️ Como Executar

## 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
```

---

## 2. Acesse a pasta do projeto

```bash
cd seu-repositorio
```

---

## 3. Execute o programa

```bash
python main.py
```

---

# 🧠 Conceitos Aplicados

Durante o desenvolvimento deste projeto foram utilizados os seguintes conceitos:

- Inteligência Artificial
- Algoritmo Minimax
- Busca em Árvore
- Tomada de Decisão
- Jogos Competitivos
- Heurísticas
- Recursividade

---

# 👨‍🎓 Autor

Projeto desenvolvido por **Felipe Krause** para fins acadêmicos e aprendizado em Inteligência Artificial.
