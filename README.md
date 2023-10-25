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

- Thm: $O(log_{2}n) and O(log_{5}n)$ are the same
- Proof:
- From the definition of $O$, suppose $T(n) \in O(log_{2}n) \iff \exists c, n_0: T(n) \leq c \cdot log_{2}n \forall n \geq n_0$
- Using the change of base formula for logs, we can write this as $T(n) \in O(log_{2}n) \iff \exists c, n_0: T(n) \leq c \cdot \frac {log_{5}n}{log_{5}2} \forall n \geq n_0$
- Since log_{5}2 is just some constant, we see that $T(n) \in O(log_{2}n) \iff \exists c, n_0: T(n) \leq c \cdot log_{5}n \forall n \geq n_0$
- Therefore $T(n) \in O(log_{5}n)$

- And vice versa, $T(n) \in O(log_{5}n) \iff \exists c, n_0: T(n) \leq c \cdot log_{5}n \forall n \geq n_0$
- = $T(n) \in O(log_{5}n) \iff \exists c, n_0: T(n) \leq c \cdot \frac {log_{2}n}{log_{2}5} \forall n \geq n_0$
- = $T(n) \in O(log_{5}n) \iff \exists c, n_0: T(n) \leq c \cdot log_{2}n \forall n \geq n_0$
- Therefore $T(n) \in O(log_{2}n)$

- This shows $\forall T(n), T(n) \in O(log_{2}n) -> T(n) \in O(log_{5}n)$
- Thus $O(log_{2}n)$ and $O(log_{5}n)$ are the same
