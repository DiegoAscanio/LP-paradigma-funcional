## Programação Funcional em Python — Composição de Funções

- Cálculo das raízes de uma equação do segundo grau por composição de funções:

\\[
    x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
\\]

- Implementação em Python:

```python
menos_b_sobre_2a = lambda a, b: -b / (2 * a)
raiz_delta_sobre_2_a = lambda a, b, c: ((b ** 2 - 4 * a * c) ** 0.5) / (2 * a)
raizes = lambda a, b, c: menos_b_sobre_2a(a, b) + raiz_delta_sobre_2_a(a, b, c),
                         menos_b_sobre_2a(a, b) - raiz_delta_sobre_2_a(a, b, c)
```
