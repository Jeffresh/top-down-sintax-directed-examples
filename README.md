# Top down sintax directed examples
Design of translation scheme examples and implementation using SLY 

## Functional expression notation

Design translation scheme (offset parameters Pascal style. That is, the parameters are put on the stack form left ro right) of this grammar using
a top down analyzer:

### Grammar:

```
Def -> Tipo ID Resto
Resto -> ‘,’ Tipo ID Resto
Resto -> epsilon
Tipo -> INT
Tipo -> CHAR
Tipo -> FLOAT
```

### Example:

**Input:**

`f(int a, float b, char c)`

**Output:**

```
Offset de c = 4
Offset de b = 4 + sizeof(char)
Offset de a = 4 + sizeof(char) + sizeof(float)

```

### Implementation
[Functional expresion notebook](./src/functional_expressions_top_down.ipynb)
