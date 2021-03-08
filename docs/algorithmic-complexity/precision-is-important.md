# Precision is important
Often candidates are told that precision is not important when computing the time or space
complexity. Even more often candidates are told that precision does not matter in a very
limited or specific situation but the candidates extrapolate the guidance to take a lax attitude
towards complexity. For example CtCI mentions that candidates may think that they're being more
precise by saying $O(2N)$ instead of $O(N)$ but they're not. CtCI is correct but some candidates
may assume that all constants can be ignored. CtCI immediately provides a good counter example
where the constant is indeed quite important.

But, this causes another problem for the candidates
-- do we now need to remember when the constants are important and when they're not?
Some practitioners would argue that with practice you'll learn where the constants are important
and when they're not. This is a prime example of unsaid, interstitial knowledge that comes from
practicing a large number of complexity problems.

We take a different approach to this issue. We follow these rules:

1. Treat constants as important until the very end
2. Being a bit extra precise is better than ignoring something that shouldn't have ignored
3. Formal derivation beats intuition or graphical derivation

An example of two recursive calls --  if you ignore the constant, you'll get the wrong
complexity. $T(n) = c + 2 T(n-1)$. Ignore $c$, see what happens.


# Complexity is rooted in formal math
Often candidates wrongly believe that complexity mathematics is inherently hand-wavy and always
informal because:

1. Computing time complexity involves making simplifying assumptions. Since we can never obtain the
exact time complexity anyway, why not make any approximation anywhere.
3. Correct though poorly worded statement: $O(n)$ is also $O(n^2)$

But, complexity is a formal statement that is used in non-CS mathematics as well. It has a solid
formal footing. This means that derivations of time complexity have rules and you should be
careful. It is not until the end of the derivation that you know which terms are important and
which are not. This is why it's best to keep all of them around until the very end.


## When in doubt, use formal definitions
If you're unsure whether $O(n)$ is also $O(n^2)$ or $O(2n)$ is also $O(n + n^3)$, use formal
definition of the big-O to derive. Don't guess. Formal definitions are extremely simple to
remember and to use. Eventually, you may be able to use the formal definition in your mind without
needing pen and paper.
