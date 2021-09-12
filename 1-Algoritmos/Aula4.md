# Operações Matemáticas

Sendo o computador uma máquina de calcular, os operadores matemáticos são parte importante, seguindo a mesma ordem da matemática tradicional:

 1. Potenciação;
 2. Multiplicação e Divisão;
 3. Soma e Subtração.

## Potenciação

Podem ser usados os símbolos ** ou ^, variando de linguagem para linguagem.

**Exemplos**

- <img src="https://render.githubusercontent.com/render/math?math=3^2$"> pode ser descrito como 3**2 ou 3^2;
- <img src="https://render.githubusercontent.com/render/math?math=4^3"> pode ser descrito como 4**3 ou 4^3;
- <img src="https://render.githubusercontent.com/render/math?math=2^8"> pode ser descrito como 2**8 ou 2^8.

## Multiplicação

É utilizado o símbolo * ao invés de <img src="https://render.githubusercontent.com/render/math?math=\times">.

**Exemplos**

- <img src="https://render.githubusercontent.com/render/math?math=3\times2"> fica 3*2;
- <img src="https://render.githubusercontent.com/render/math?math=4\times5"> fica 4*5;
- <img src="https://render.githubusercontent.com/render/math?math=10\times5"> fica 10*5.

## Divisão

É utilizado o símbolo / ao invés de <img src="https://render.githubusercontent.com/render/math?math=\div">.

**Exemplos**

- <img src="https://render.githubusercontent.com/render/math?math=4\div2"> fica 4/2;
- <img src="https://render.githubusercontent.com/render/math?math=10\div5"> fica 10/5;
- <img src="https://render.githubusercontent.com/render/math?math=32\div4"> fica 32/4.

> **Nota**: Diversas linguagens de programação conseguem tratar o caso de divisão por **zero**, mas isso não ocorre com todas. Em linguagens de baixo nível, é necessário criar tratamentos para evitar a divisão por zero, caso contrário o computador pode até travar. 
> Isso ocorre porque na divisão por zero há uma descontinuidade, conforme pode ser visto na figura abaixo:


![Gráfico de divisões](https://upload.wikimedia.org/wikipedia/commons/4/43/Hyperbola_one_over_x.svg)

> Em linguagens com o tratamento da divisão por zero, algumas assumem que essa operação resulta em infinito (<img src="https://render.githubusercontent.com/render/math?math=\infty">) ou *Not a Number* (*NaN*), enquanto outras resultam em uma mensagem de erro.

## Soma e Subtração

Permanece igual, usando + para adição e - para subtração.

**Exemplos**

- <img src="https://render.githubusercontent.com/render/math?math=3%2B2">;
- <img src="https://render.githubusercontent.com/render/math?math=4-3">;
- <img src="https://render.githubusercontent.com/render/math?math=120-240">.

## Expressões

 Na criação de algoritmos, é possível criar complexas expressões matemáticas usando parênteses "()", colchetes "[]" e chaves "{}". Porém nas linguagens de programação é comum que colchetes e chaves  estejam associados a outros tipos de operações.

### Validade de Expressões Matemáticas

Uma expressão matemática válida deve seguir as seguintes regras:

- Todos os números devem ser separados por uma operação entre si e em relação a blocos de parênteses:

-- **Válido:** <img src="https://render.githubusercontent.com/render/math?math=2%2B3">, <img src="https://render.githubusercontent.com/render/math?math=2*3"> , <img src="https://render.githubusercontent.com/render/math?math=2%2B(3)"> , <img src="https://render.githubusercontent.com/render/math?math=(2)-1">;

-- **Inválido:** 2 3 , <img src="https://render.githubusercontent.com/render/math?math=2(3)"> , <img src="https://render.githubusercontent.com/render/math?math=(2)1">;

- Todo o parênteses aberto deve ser fechado e um bloco não deve ser fechado sem antes ser aberto:

-- **Válido:** <img src="https://render.githubusercontent.com/render/math?math=(1%2B2)">, <img src="https://render.githubusercontent.com/render/math?math=(1)">, <img src="https://render.githubusercontent.com/render/math?math=(3*2)">;

-- **Inválido:** <img src="https://render.githubusercontent.com/render/math?math=(1">, <img src="https://render.githubusercontent.com/render/math?math=2%2B1)">;

- Todo bloco de parênteses deve ter pelo menos um número ou outro parênteses internamente:

-- **Válido:** <img src="https://render.githubusercontent.com/render/math?math=(1)"> , <img src="https://render.githubusercontent.com/render/math?math=((2%2B1))">;

-- **Inválido:** <img src="https://render.githubusercontent.com/render/math?math=()"> , <img src="https://render.githubusercontent.com/render/math?math=(()"> , <img src="https://render.githubusercontent.com/render/math?math=())"> , <img src="https://render.githubusercontent.com/render/math?math=(())">;

- Dois blocos de parênteses devem ser separados por uma operação matemática:

-- **Válido:** <img src="https://render.githubusercontent.com/render/math?math=(2)*(3)">, <img src="https://render.githubusercontent.com/render/math?math=((2%2B3)%20*%20(4%2F5))%20%2B%20(5*4)">;

-- **Inválido:** <img src="https://render.githubusercontent.com/render/math?math=(2)(3)"> , <img src="https://render.githubusercontent.com/render/math?math=((2%2B3)(4%2F5))(5*4)">;

### Ordem de Processamento de uma Expressão Matemática

 1. Bloco de parênteses mais interno:

-- **Exemplo:** (((1º) 2º) 3º) , (((( 1º ) 2º) 3º) 4º);

2. Bloco de parênteses mais à esquerda:

-- **Exemplo:** (( 1º ) + ( 2º ) 3º) , ((3º)+(((1º) 2º)4º)5º)

3. Números fora dos blocos de parênteses.