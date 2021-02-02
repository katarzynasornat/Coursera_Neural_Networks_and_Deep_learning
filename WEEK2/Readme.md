## Logistic regression


## Loss & Cost function for logistic regression


## Gradient Descent method


### Derivatives

### Chain rule to calculate derivatives

\[\newline \frac{\partial L}{\partial w} = \frac{\partial L}{\partial g}\frac{\partial g}{\partial z}\frac{\partial z}{\partial w} \newline\newline \frac{\partial L}{\partial b} = \frac{\partial L}{\partial g}\frac{\partial g}{\partial z}\frac{\partial z}{\partial b}\]

Suppose we want the derivative of $f(g(x))$. Again, let's set up the derivative and play some algebraic tricks:
ddxf(g(x))=limΔx→0f(g(x+Δx))−f(g(x))Δx=limΔx→0f(g(x+Δx))−f(g(x))g(x+Δx)−g(x)g(x+Δx)−g(x)Δx
Now we see immediately that the second fraction turns into g′(x) when we take the limit. The first fraction is more complicated, but it too looks something like a derivative. The denominator, g(x+Δx)−g(x), is a change in the value of g, so let's abbreviate it as Δg=g(x+Δx)−g(x), which also means g(x+Δx)=g(x)+Δg. This gives us
limΔx→0f(g(x)+Δg)−f(g(x))Δg.
As Δx goes to 0, it is also true that Δg goes to 0, because g(x+Δx) goes to g(x). So we can rewrite this limit as
limΔg→0f(g(x)+Δg)−f(g(x))Δg.
Now this looks exactly like a derivative, namely f′(g(x)), that is, the function f′(x) with x replaced by g(x). If this all withstands scrutiny, we then get
ddxf(g(x))=f′(g(x))g′(x).
Unfortunately, there is a small flaw in the argument. Recall that what we mean by limΔx→0 involves what happens when Δx is close to 0 but not equal to 0. The qualification is very important, since we must be able to divide by Δx. But when Δx is close to 0 but not equal to 0, Δg=g(x+Δx))−g(x) is close to 0 and possibly equal to 0. This means it doesn't really make sense to divide by Δg. Fortunately, it is possible to recast the argument to avoid this difficulty, but it is a bit tricky; we will not include the details, which can be found in many calculus books. Note that many functions g do have the property that g(x+Δx)−g(x)≠0 when Δx is small, and for these functions the argument above is fine.

The chain rule has a particularly simple expression if we use the Leibniz notation for the derivative. The quantity f′(g(x)) is the derivative of f with x replaced by g; this can be written df/dg. As usual, g′(x)=dg/dx. Then the chain rule becomes
dfdx=dfdgdgdx.
This looks like trivial arithmetic, but it is not: dg/dx is not a fraction, that is, not literal division, but a single symbol that means g′(x). Nevertheless, it turns out that what looks like trivial arithmetic, and is therefore easy to remember, is really true.

It will take a bit of practice to make the use of the chain rule come naturally—it is more complicated than the earlier differentiation rules we have seen.

### Computational graphs - examples

### Computational graphs for logistic regression
