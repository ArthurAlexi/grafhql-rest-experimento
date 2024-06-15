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
