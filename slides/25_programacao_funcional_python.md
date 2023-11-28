## Operações Acumulativas Sobre Iteradores (reduce)

<div class="small">

Quando queremos realizar operações acumulativas sobre elementos de um iterador, queremos aplicar uma função ao primeiro elemento, acumular seu resultado, aplicar a função ao segundo elemento e acumular seu resultado, e assim por diante. Esta operação acumulativa é chamada de `reduce` (redução) e fica fácil entender o seu nome ao verificar que todos os elementos do iterador são **reduzidos** a um único valor.

Python não oferece uma função nativa (como `map` ou `filter`) para realizar esta redução, porém, oferece um módulo de ferramentas para funções de ordem superior chamado `functools` que contém a função `reduce`. Para utilizá-la, precisamos importar o módulo `functools` e, em seguida, chamar a função `reduce` passando como argumentos uma função e um iterador.

Verifiquemos o exemplo do produtório sobre um iterador:

```python
from functools import reduce

def produto(a, b):
    return a * b

iteravel = range(1, 10)
resultado = reduce(produto, iteravel)
print(resultado) # 362880
```

</div>
