# Isomorphism

Prove that if two graphs $A$ and $B$ are isomorphic they do *not* have to
be completely connected. I have started with the formal definition of
isomorphism below. Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$G_1=(V_1 , E_1)$ is isomorphic to $G_2 = (V_2, E_2)$ if there exists a
one-to-one and onto function (bijection) $f: V_1 \rightarrow V_2$ such that $(u,v)
\in E_1$ iff $(f(u),f(v)) \in E_2$.

# Answer

Proof by Counter Example:

Let $A=(V_1,E_1)$ and $B=(V_2,E_2)$, such that $$V_1=\{a,b,c\}, \hspace{5mm} E_1=\{(a,b),(b,c)\}$$

$$V_2= \{x,y,z\}, \hspace{5mm}E_2=\{(x,y),(y,z)\}.$$

Now observe that $|V_1|=3$ and $|V_2|=3$, however the $deg(u)$ of any $u\in V_1,V_2$ it is the case that $deg(u)$ $\in\{1,2\}$.

This shows us that neither graph is completley connected due to the fact that a completely connected graph has a $deg(u) =n-1$ $\forall u \hspace{2mm} \in V$ where $V$ is a some completely connected graph.

With that in mind we can now construct an isomorphism.

Let $\phi$ be a function $\phi:V_1\longrightarrow V_2$, with the following mapping:

$$\phi:\begin{pmatrix} a&b&c\\
x&y&z\end{pmatrix}$$
This is obviously a bijective function. Now we just need to verify that the edges map properly.

$(a,b)\in E_1$ now take $\phi((a,b))=\phi((x,y))\in E_2$

$(b,c)\in E_2$ now take $\phi(b,c)=\phi((b,c))\in E_2.$ Therefore $A \cong B$, however neither A or B is a complete graph.

We have thus shown that is cannot be the case that for two graphs $A',B'$ $A'\cong B' $ iff A and B are completely connected.

