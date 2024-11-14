# Introdução

O problema das 8 Rainhas é um desafio em IA, onde o objetivo é colocar as rainhas em um tabuleiro de xadrez de maneira que nenhuma rainha possa atacar outra. Esse problema se enquadra na categoria de problemas de otimização combinatória, já que existem inúmeras possibilidades de disposição das peças, mas apenas algumas configurações atendem ao requisito do desafio. A resolução desse problema é importante para compreender algoritmos de busca e otimização.

A escolha de um algoritmo genético para resolver esse problema deve-se à eficiência desse método ao lidar com grandes quantidades de solução. Os algoritmos genéticos são inspirados no processo de evolução natural, aplicando seleção natural, crossover e mutação em uma população de soluções diferentes. Nosso objetivo com este projeto é desenvolver uma solução utilizando Python, que seja capaz de encontrar uma formação válida das oito rainhas no tabuleiro.

# Fundamentação Teórica

Algoritmos genéticos são métodos de busca baseados na evolução biológica e são amplamente utilizados para problemas de otimização, onde a solução não é evidente. No contexto do problema das Oito Rainhas, cada indivíduo representa uma configuração específica de rainhas no tabuleiro, e o processo evolutivo visa maximizar o número de pares de rainhas que não se atacam mutuamente. Esses são os principais conceitos do algoritmo genético para conseguir uma solução:

- **População**: É composta por um conjunto de soluções. Cada indivíduo é uma permutação dos números de 0 a 7, representando a posição das rainhas nas colunas do tabuleiro.
- **Fitness**: A função de fitness mede o desempenho de cada indivíduo, avaliando o número de pares de rainhas que não se atacam.

### Operadores Genéticos

- **Seleção**: Foi utilizada a seleção por torneio, em que são selecionados aleatoriamente cinco indivíduos, e os dois com melhor fitness são escolhidos para gerar descendentes.
- **Crossover**: A operação de crossover combina dois indivíduos (pais) para gerar descendentes, promovendo a diversidade genética.
- **Mutação**: Aplicada com uma taxa de 10%, envolve a troca de duas posições em uma permutação, permitindo que o algoritmo explore novas configurações de maneira mais ampla.

# Projeto de Implementação

A implementação do algoritmo genético foi estruturada conforme as etapas e operações principais descritas anteriormente:

1. **Criação de Indivíduos**: Cada indivíduo é uma permutação única de números de 0 a 7, correspondendo à posição de cada rainha.
2. **Função de Fitness**: Implementada para contar o número de pares de rainhas que não se atacam, permitindo calcular o fitness de cada indivíduo.
3. **Operadores Genéticos**: Foram implementadas as funções de seleção, crossover e mutação, sendo estas essenciais para a evolução da população a cada geração.

### Parâmetros do Algoritmo

- **Tamanho da população**: 100
- **Taxa de mutação**: 10%
- **Máximo de gerações**: 1000

Foi também implementada uma função de visualização utilizando a biblioteca `matplotlib`, que apresenta o tabuleiro de xadrez com a posição das rainhas.

# Considerações Finais

O algoritmo genético desenvolvido foi capaz de encontrar uma solução válida para o problema das Oito Rainhas em todas as execuções. A visualização permitiu validar a posição das rainhas e verificar se nenhuma se encontrava em posição de ataque. Entre os desafios enfrentados, podemos destacar a seleção de parâmetros apropriados, como a taxa de mutação e o tamanho da população, que influenciam diretamente no algoritmo.

# Bibliografia

- [https://www.ic.unicamp.br/~lehilton/cursos/2s2022/mc202e/tarefas/03-m-rainhas/](https://www.ic.unicamp.br/~lehilton/cursos/2s2022/mc202e/tarefas/03-m-rainhas/)
- [https://www.youtube.com/watch?v=OzZU9JnK5GY](https://www.youtube.com/watch?v=OzZU9JnK5GY)
- [https://didatica.tech/como-funcionam-os-algoritmos-geneticos/](https://didatica.tech/como-funcionam-os-algoritmos-geneticos/)
