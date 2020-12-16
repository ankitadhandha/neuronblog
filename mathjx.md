
# Math support

Neuron's Markdown syntax supports [MathJax](https://www.mathjax.org/).


## LaTeX input

You can type LaTeX code in zettels in three ways:

* **Inline**: by surrounding your code with ``` $...$ ```
* **Block**: by surrounding your code with ``` $$...$$ ```
* **Multi-line block, centered**: 
```markdown
$$    
\begin{split}
    x+1 &= 2 \\
    y+2 &= 3 
\end{split}
$$
```

## Examples

* Inline LaTeX when written as ``` $a^2+b^2$ ``` looks like this: $a^2+b^2$

* Block LaTeX looks like this: $$(A = B) \cong (A \cong B)$$

* The multi-line block example shown above will render like this:
$$    
\begin{split}
    x+1 &= 2 \\
    y+2 &= 3 
\end{split}
$$


$$
 \begin{align}AAE8=\sum_{1}^8(essential-amino-acids)\end{align}
$$

$$
 \begin{align}
   AAE8=[isoleucine]\\
   +[leucine]\\
   +[lysine]\\
   +[methionine]\\
   +[phenylalanine]\\
   +[threonine]\\
   +[tryptophan]\\
   +[valine]
   \end{align}
$$

$$
\begin{align}[infoods:AAE8]=[infoods:ILE]\\
   +[infoods:LEU]\\
   +[infoods:LYS]\\
   +[infoods:MET]\\
   +[infoods:PHE]\\
   +[infoods:THR]\\
   +[infoods:TRP]\\
   +[infoods:VAL]
   \end{align}
$$

$$
 \begin{align}
   [infoods:AAE8]=[infoods:ILE]\\
   [ncit:C64911][infoods:LEU]\\
   [ncit:C64911][infoods:LYS]\\
   [ncit:C64911][infoods:MET]\\
   [ncit:C64911][infoods:PHE]\\
   [ncit:C64911][infoods:THR]\\
   [ncit:C64911][infoods:TRP]\\
   [ncit:C64911][infoods:VAL]
   \end{align}
$$

$$
\begin{align}
   [infoods:AAE8]_{g-100-g-EP}=\\
   ([infoods:ILE][vocal:v62177])\\
   [ncit:C64911]([infoods:LEU][vocal:v62177])\\
   [ncit:C64911]([infoods:LYS][vocal:v62177])\\
   [ncit:C64911]([infoods:MET][vocal:v62177])\\
   [ncit:C64911]([infoods:PHE][vocal:v62177])\\
   [ncit:C64911]([infoods:THR][vocal:v62177])\\
   [ncit:C64911]([infoods:TRP][vocal:v62177])\\
   [ncit:C64911]([infoods:VAL][vocal:v62177])
   \end{align}
$$

$$
 \begin{align}
   [infoods:AAE8]_{[vocal:v62177]}=\\
   ([infoods:ILE][vocal:v62177][xsd:float]<value>)\\
   [ncit:C64911]([infoods:LEU][vocal:v62177][xsd:float]<value>)\\
   [ncit:C64911]([infoods:LYS][vocal:v62177][xsd:float]<value>)\\
   [ncit:C64911]([infoods:MET][vocal:v62177][xsd:float]<value>)\\
   [ncit:C64911]([infoods:PHE][vocal:v62177][xsd:float]<value>)\\
   [ncit:C64911]([infoods:THR][vocal:v62177][xsd:float]<value>)\\
   [ncit:C64911]([infoods:TRP][vocal:v62177][xsd:float]<value>)\\
   [ncit:C64911]([infoods:VAL][vocal:v62177][xsd:float]<value>)
   \end{align}
$$
    
    
   
   
