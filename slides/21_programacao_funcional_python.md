## Programação Funcional — Iteradores

<div class="regular">

- Porquê iteradores são fundamentais para a programação funcional?

    1. **Promovem tratamento eficaz de sequências de dados**: programação funcional frequentemente lida com transformação de dados em sequências (listas, tuplas, etc) e iteradores são a forma mais eficiente de lidar com isso, permitindo percorrer, filtrar, mapear e reduzir dados de maneira expressiva e concisa.
    2. **Lazy Evaluation (Avaliação Preguiçosa)**: as execuções de funções só são realizadas quando estritamente necessário, ou seja, quando um dado estiver disponível. Iteradores respeitam este princípio, pois, seus elementos são obtidos sob demanda (**__next__**) um de cada vez. Isto economiza memória e tempo de processamento, sendo muito útil para lidar com grandes volumes de dados ou fluxos infinitos.
    3. **Imutabilidade e sem Estado**: Iteradores não armazenam estados (exceto pela sua posição atual) e são imutáveis — não alteram a esturuta dos dados ao serem percorridos. Tudo isto fortalece os princípios de **transparência referencial**.
    4. **Composição de Funções e Encadeamento**: Iteradores podem ser facilmente combindos com funções de ordem superior (como **map**, **filter** e **reduce**) permitindo a composição e o encadeamento de operações de maneira clara e lógica.

</div>
