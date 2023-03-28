# aps-langprog-2023-1
# Cifra de César - Uma Linguagem de Programação

<p> A ideia dessa APS é desenvolver uma linguagem de programação que utilize a famosa Cifra de Csar.</p>

<img src=https://user-images.githubusercontent.com/49698335/199146390-87d1b8b3-4cd5-429b-963b-acad86dda87b.png width="600"/>

>Referência retirada do site: https://www.printables.com/model/226087-caesar-shift-cipher-wheel

### Explicação:
<p> No momento pensei na seguinte motivação: quero escrever um programa de computador, mas que somente eu e quem tiver a combinação (numeração de quantos espaços pular) descobrirá o que está escrito no código. Para isso no começo estou definindo uma <strong>combinação fixa de 3</strong>. Sendo assim é uma linguagem baseada na linguagem que nós desenvolvemos no compilador, então para que ela funcione é só seguir a mesma lógica utilizando a cifra para reescrever as palavras chaves de acordo com o deslocamento de letras.</p>

<p> A linguagem aceita apenas palavras-chave somente <em><strong>upper case</strong></em> ou <em><strong>lower case</strong></em>.
 
<p><strong>Exemplo:</strong> A palavra <em>if</em> se torna <em>li</em> já que a letra <em>i</em> deslocada 3 letras para frente se torna a letra <em>l</em> o mesmo vale para a letra <em>f</em> que se torna <em>i</em>.</p>


<p><em>Disclaimer:</em> A princípio está muito simples, mas a ideia é expandir para ser uma linguagem que seja mudada para o compilador sempre interpretar o código à partir de um input com a combinação e consequentemente aprimorar a implementação para incluir os símbolos também.</p>

<p>EBNF:</p> 

<pre><code>BLOCK = "{", { STATEMENT }, "}" ;
STATEMENT = ( λ | ASSIGNMENT | PRINT | WHILE | BLOCK | IF), ";" ;
ASSIGNMENT = IDENTIFIER, "=", RELATIVE-EXPRESSION ;
PRINT = ("SULQW" | "sulqw"), "(", RELATIVE-EXPRESSION, ")" ;
WHILE = ("ZKLOH" | "zkloh"), "(", RELATIVE-EXPRESSION, ")", STATEMENT ;
IF = ("LI" | "li"), "(", RELATIVE-EXPRESSION, ")", STATEMENT, [("HOVH" | "hovh"), STATEMENT] ; 
RELATIVE-EXPRESSION = EXPRESSION, { ("==" | ">" | "<"), EXPRESSION } ;
EXPRESSION = TERM, { ("+" | "-" | "||"), TERM } ;
TERM = FACTOR, { ("*" | "/" | "&&"), FACTOR } ;
FACTOR = (("+" | "-" | "!"), FACTOR) | NUMBER | "(", RELATIVE-EXPRESSION, ")" | IDENTIFIER | (("UHDG" | "uhdg") , "(", ")") ;
IDENTIFIER = LETTER, { LETTER | DIGIT | "_" } ;
NUMBER = DIGIT, { DIGIT } ;
LETTER = ( a | ... | z | A | ... | Z ) ;
DIGIT = ( 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 0 ) ;
</code></pre>

