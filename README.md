# Como escrever expressões matemáticas

Use o Markdown para exibir expressões matemáticas no GitHub.

## Sobre como escrever expressões matemáticas

Para permitir a comunicação clara das expressões matemáticas, o GitHub dá suporte à matemática formatada LaTeX no Markdown. Para obter mais informações, confira [LaTeX/matemática](http://en.wikibooks.org/wiki/LaTeX/Mathematics) no Wikibooks.

A capacidade de renderização matemática do GitHub usa MathJax, um mecanismo de exibição baseado em JavaScript de código aberto. O MathJax dá suporte a uma ampla variedade de macros LaTeX e a várias extensões de acessibilidade úteis. Para obter mais informações, confira [a documentação do MathJax](http://docs.mathjax.org/en/latest/input/tex/index.html#tex-and-latex-support) e [a documentação de Extensões de Acessibilidade do MathJax](https://mathjax.github.io/MathJax-a11y/docs/#reader-guide).

A renderização das expressões matemáticas está disponível em GitHub Issues, GitHub Discussions, pull requests, wikis e arquivos Markdown.

## Como escrever expressões embutidas

Há duas opções para delimitar uma expressão matemática integrada com seu texto. Você pode colocar a expressão entre símbolos de dólar (`$`) ou iniciar a expressão com <code>$\`</code> e encerrá-la com <code>\`$</code>. A segunda sintaxe é útil quando a expressão que você está escrevendo contém caracteres que se sobrepõem à sintaxe de markdown. Para saber mais, confira [Sintaxe básica de escrita e formatação](/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

```text
This sentence uses `$` delimiters to show math inline: $\sqrt{3x-1}+(1+x)^2$
```

![Captura de tela do Markdown renderizado mostrando uma expressão matemática embutida: a raiz quadrada de 3x menos 1 mais (1 mais x) ao quadrado.](/assets/images/help/writing/inline-math-markdown-rendering.png)

```text
This sentence uses $\` and \`$ delimiters to show math inline: $`\sqrt{3x-1}+(1+x)^2`$
```

![Captura de tela do Markdown renderizado mostrando uma expressão matemática embutida com sintaxe backtick: a raiz quadrada de 3x menos 1 mais (1 mais x) ao quadrado.](/assets/images/help/writing/inline-backtick-math-markdown-rendering.png)

## Como escrever expressões como blocos

Para adicionar uma expressão matemática como um bloco, inicie uma nova linha e delimite a expressão com dois símbolos de dólar `$$`.

> \[!TIP] Se você estiver escrevendo em um arquivo .md, precisará usar a formatação específica para criar uma quebra de linha, como terminar a linha com uma barra invertida, conforme mostrado no exemplo abaixo. Para saber mais sobre quebras de linha no Markdown, confira [Sintaxe básica de escrita e formatação](/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#line-breaks).

```text
**The Cauchy-Schwarz Inequality**\
$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$
```

![Captura de tela do Markdown renderizado mostrando uma equação complexa. O texto em negrito diz "The Cauchy-Schwarz Inequality" acima da fórmula para a desigualdade.](/assets/images/help/writing/math-expression-as-a-block-rendering.png)

Como alternativa, você pode usar a sintaxe do bloco de código <code>\`\`\`math</code> para exibir uma expressão matemática como um bloco. Com essa sintaxe, você não precisa usar delimitadores `$$`. O seguinte renderizará igual à opção acima:

````text
**The Cauchy-Schwarz Inequality**

```math
\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
```
````

## Como escrever sinais de dólar em linha com e dentro de expressões matemáticas

Para exibir um sinal de dólar como um caractere na mesma linha que uma expressão matemática, você precisa fazer o escape do não delimitador `$` para garantir que a linha seja renderizada corretamente.

* Dentro de uma expressão matemática, adicione um símbolo `\` antes do `$` explícito.

  ```text
  This expression uses `\$` to display a dollar sign: $`\sqrt{\$4}`$
  ```

  ![Captura de tela do Markdown renderizado mostrando como uma barra invertida antes de um sinal de dólar exibe o sinal como parte de uma expressão matemática.](/assets/images/help/writing/dollar-sign-within-math-expression.png)

* Fora de uma expressão matemática, mas na mesma linha, coloque o `$` explícito entre tags span.

  ```text
  To split <span>$</span>100 in half, we calculate $100/2$
  ```

  ![Captura de tela do Markdown renderizado mostrando como as tags de span ao redor de um sinal de dólar exibem o sinal como um texto em linha, e não como parte de uma equação matemática.](/assets/images/help/writing/dollar-sign-inline-math-expression.png)

## Leitura adicional

* [O site do MathJax](http://mathjax.org)
* [Começando com escrita e formatação no GitHub](/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github)
* ```
            [Especificação do GitHub Flavored Markdown](https://github.github.com/gfm/)
  ```
