[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12071342&assignment_repo_type=AssignmentRepo)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

- Thm: $O(log_{2}n)$ is the same as $O(log_{5}n)$
- Proof: Suppose we have the function $log_{2}n$. By the change of base formula, we can say $log_{2}n = \frac {log_{a}n}{log_{a}2}$. Then, by the mathematical definition of $O$, clearly $log_{2}n \leq c \cdot log_{a}n$, where $c = \frac {1}{|{log_{a}2}|}$ and $n_{0} \geq 1$, meaning for any positive real number base $a$, $log_{2}n \in O(log_{a}n)$, proving the theorem. 