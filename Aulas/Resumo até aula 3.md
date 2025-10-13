# Resumo: Fundamentos de Inteligência Artificial

Este resumo aborda os conceitos essenciais de Inteligência Artificial, desde a sua definição e agentes até às diferentes metodologias de procura e aprendizagem, com base no documento fornecido.

---

## 1. O que é Inteligência Artificial (IA)?

A IA é a ciência de criar máquinas capazes de realizar tarefas que exigiriam inteligência se fossem feitas por humanos. Abrange sistemas que aprendem, resolvem problemas e tomam decisões.

- **Como Funciona**: Os algoritmos de IA são treinados com grandes volumes de dados (`datasets`) para aprender padrões e fazer previsões.
- **Aplicações Diárias**:
    - **Reconhecimento de Imagem**: Desbloqueio facial em telemóveis.
    - **Chatbots**: Suporte ao cliente.
    - **Navegação**: Serviços de mapas como o Google Maps.
    - **E-commerce**: Sugestão de produtos com base nas suas preferências.
- **Futuro da IA**: A IA tem um enorme potencial, mas é crucial abordar as considerações éticas e garantir um desenvolvimento responsável e sustentável.

---

## 2. Agentes em IA

Um **agente** é uma entidade (hardware ou software) que observa o seu ambiente através de **sensores** e age sobre ele através de **atuadores**.

### O Ciclo Percepção-Ação

O funcionamento de um agente baseia-se num ciclo contínuo:
1.  **Percepção (Perception)**: O agente recolhe informação do ambiente através dos sensores.
2.  **Predição (Prediction)**: O agente processa a informação e prevê resultados.
3.  **Ação (Action)**: O agente decide e executa uma ação através dos atuadores.
4.  **Resultado (Outcome)**: A ação modifica o ambiente.

### Desenhar um Agente: Framework PEAS

Para projetar um agente, utiliza-se o modelo PEAS:
- **P (Performance)**: Como a sua performance será avaliada.
- **E (Environment)**: O ambiente onde o agente opera.
- **A (Actuators)**: As ferramentas que o agente usa para interagir com o ambiente
- **S (Sensors)**: A forma como o agente perceciona o ambiente

---

## 3. Tipos de Agentes e Metodologias

### 3.1. Agentes Reativos

Estes são os agentes mais simples. Fazem um mapeamento direto entre o que percecionam e as ações que executam, tendo uma visão local e memória limitada.

- **Limitações**: Têm uma visão local do ambiente e um controlador fixo, o que limita a sua capacidade de resolver tarefas complexas.

### 3.2. Agentes de Procura

São agentes mais sofisticados que possuem mais memória para mapear **estados** e as relações entre eles. Usam a simulação para antever os resultados das suas ações.

#### Conceitos de Procura

- **Estado**: Uma representação completa de uma situação no problema.
- **Operadores**: Ações que permitem a transição entre estados.
- **Árvore de Procura**: A estrutura que resulta da aplicação de todos os operadores a partir do estado inicial.

#### Algoritmos de Procura

##### Procura Cega (Força Bruta)

Não utiliza informação sobre o problema para guiar a busca.
- **Procura em Profundidade**: Explora um ramo da árvore o mais fundo possível antes de retroceder. Pode ficar presa em ciclos infinitos.
- **Procura em Largura**: Explora a árvore nível a nível, garantindo encontrar a solução mais curta em número de passos.
- **Custo Uniforme**: Expande sempre o nó com o menor custo acumulado desde o início.

##### Procura Heurística

Usa conhecimento sobre o problema para realizar uma procura mais eficiente, testando apenas as soluções que parecem mais promissoras.
- **Algoritmo A***: Um algoritmo popular que combina o custo do caminho já percorrido com uma estimativa (heurística) do custo restante até ao objetivo.

##### Procura Adversarial

Aplicada em ambientes competitivos (jogos), onde um agente ganha e o outro perde.
- **Função de Recompensa**: Avalia a "utilidade" de um estado do jogo para decidir a melhor jogada.

### 3.3. Agentes Aprendizes

São agentes que alteram as suas estruturas internas de forma automática para melhorar o seu desempenho ao longo do tempo.

#### Árvores de Decisão (Abordagem Simbólica)

- **Como Funcionam**: Representam decisões de forma hierárquica, semelhante a um fluxograma.
- **Vantagens**: São fáceis de interpretar e explicar e conseguem lidar com dados qualitativos.
- **Desvantagens**: Têm uma capacidade de generalização limitada e uma performance inferior a métodos mais complexos.

#### Redes Neuronais (Abordagem Conexionista)

- **Como Funcionam**: Inspiradas no cérebro humano, são compostas por **neurónios** artificiais ligados por **conexões** com pesos ajustáveis. Aprendem através de um processo chamado **Retropropagação** (*Backpropagation*), onde o erro da rede é calculado e usado para ajustar os pesos das conexões.
- **Vantagens**: Conseguem modelar relações muito complexas e têm um desempenho superior em tarefas de imagem, som e linguagem natural.
- **Desvantagens**: Exigem grande poder computacional e são difíceis de interpretar (consideradas uma "caixa-preta").