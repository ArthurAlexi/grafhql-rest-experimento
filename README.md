# GraphQL vs REST: Um Experimento Controlado


## Desenho do Experimento

### Hipóteses

#### Hipótese Nula (H0):

- **H0_1:** Não há diferença significativa no tempo de resposta entre consultas GraphQL e consultas REST.

- **H0_2:** Não há diferença significativa no tamanho das respostas entre consultas GraphQL e consultas REST.

#### Hipótese Alternativa (H1):

- **H1_1:** As consultas GraphQL têm tempos de resposta significativamente mais rápidos que as consultas REST.

- **H1_2:** As respostas das consultas GraphQL têm tamanho significativamente menor que as respostas das consultas REST.


### Variáveis Dependentes

- **Tempo de resposta:** Medido em milissegundos (ms).

- **Tamanho da resposta:** Medido em kilobytes (KB).

### Variáveis Independentes

- **Tipo de API:** GraphQL vs REST.

- **Tipo de consulta:** Tipos específicos de dados solicitados.

### Tratamentos

Os tratamentos serão os diferentes tipos de consultas realizadas em ambas as APIs :

- Consulta de repositórios do usuário.
- Consulta de issues abertas em um repositório.
- Consulta de commits em um repositório.

### Objetos Experimentais

Os objetos experimentais serão as respostas das APIs do GitHub para as consultas mencionadas. Utilizaremos a API GraphQL e a API REST do GitHub para obter essas respostas.

### Tipo de Projeto Experimental

O experimento será um estudo comparativo empírico com amostras pareadas, em que  cada tipo de consulta será realizada tanto na API GraphQL quanto na API REST, permitindo comparações diretas.

### Quantidade de Medições

Para garantir a significância estatística, cada consulta será realizada múltiplas vezes. Proponho que cada consulta seja realizada pelo menos 10 vezes em cada API

### Ameaças à Validade

#### Validade Interna.

- **Flutuações na Rede:** Variações na latência da rede podem afetar o tempo de resposta.

- **Cache:** Efeitos de cache nas respostas das APIs devem ser mitigados.

- **Carregamento do Servidor:** A carga do servidor GitHub no momento da consulta pode variar.

#### Validade Externa:

- **Generalização:** Os resultados podem ser específicos para a API do GitHub e podem não se aplicar a outras APIs.

- **Variedade das Consultas:** A seleção limitada de consultas pode não representar completamente o uso geral das APIs.

## Resultados

### Query 1:

|||
|:-:|:-:|
| Tempo (segundos) | <img  src="https://github.com/ArthurAlexi/graphql-rest-experimento/assets/90854173/3c76134b-f216-4bd2-89bd-1a7eacfc0c6e" alt="" align="left" height="250"  width="auto"> | 
Tamanho (bytes) | <img  src="https://github.com/ArthurAlexi/graphql-rest-experimento/assets/90854173/35681e8e-4cb1-46f6-838a-ef6174e141fb" alt="" align="left" height="250" width="auto"> |
Velocidade (bytes/segundo) | <img  src="https://github.com/ArthurAlexi/graphql-rest-experimento/assets/90854173/43bbe58b-0bd2-4030-91ed-8f3dcfd465eb" alt="" align="230" height="auto" width="auto">|

### Query 2:

|||
|:-:|:-:|
| Tempo (segundos) | <img  src="https://github.com/ArthurAlexi/graphql-rest-experimento/assets/90854173/07e315df-a2ed-4de2-acd7-55e370cd1e1e" alt="" align="left" height="250"  width="auto"> | 
Tamanho (bytes) | <img  src="https://github.com/ArthurAlexi/graphql-rest-experimento/assets/90854173/fb81c145-7e79-49f7-a099-6db56310683d" alt="" align="left" height="250" width="auto"> |
Velocidade (bytes/segundo) | <img  src="https://github.com/ArthurAlexi/graphql-rest-experimento/assets/90854173/71068ec5-6f09-4e79-903e-0eb591879747" alt="" align="230" height="auto" width="auto">|

### Query 3:

|||
|:-:|:-:|
| Tempo (segundos) | <img  src="https://github.com/ArthurAlexi/graphql-rest-experimento/assets/90854173/6d39a1aa-ed6a-42c4-a5d9-8c6918a9ebcb" alt="" align="left" height="250"  width="auto"> | 
Tamanho (bytes) | <img  src="https://github.com/ArthurAlexi/graphql-rest-experimento/assets/90854173/f9d05740-f80a-4555-9132-1e6cc7645996" alt="" align="left" height="250" width="auto"> |
Velocidade (bytes/segundo) | <img  src="https://github.com/ArthurAlexi/graphql-rest-experimento/assets/90854173/73f83598-6ac1-4525-b157-6d8031b09dc0" alt="" align="230" height="auto" width="auto">|

## Conclusão

Com base nos dados observados nas tabelas anteriores, podemos concluir que a API GraphQL apresenta várias vantagens significativas em relação à API REST. Além da flexibilidade oferecida pela GraphQL, que permite aos usuários decidir exatamente quais tabelas e campos serão retornados em uma consulta, a análise quantitativa revelou que as respostas da API GraphQL também são mais eficientes em termos de velocidade. Especificamente, a API GraphQL demonstrou uma maior taxa de transferência de dados, medida em bytes por segundo, indicando uma performance superior em termos de tempo de resposta e eficiência no uso da largura de banda. Esses benefícios tornam a GraphQL uma alternativa atraente para o desenvolvimento de APIs, oferecendo tanto flexibilidade quanto desempenho aprimorado.


