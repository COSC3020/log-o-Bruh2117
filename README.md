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

- If $O(log_{2} n)$ is the same as $O(log_{5} n)$, that means asymptotically the log bases are arbitrary in terms of $O$, so to prove that we will have to prove that for any $T(n)$, $T(n) \in O(log_{a} n) -> T(n) \in O(log_{b} n)$ for arbitrary choices of a and b. 
- Thm: For any $T(n)$, $T(n) \in O(log_{a} n) -> T(n) \in O(log_{b} n)$ for arbitrary choices of a and b
- Proof: Suppose $T(n) \in O(log_{a} n)$, for an arbitrary a, which by the definition of $O(log_{a} n)$ means $\exists c, n_0: T(n) \leq c \cdot log_{a} n \forall n \geq n_0$. Say $c = log_{b} a$, for an arbitrary b, which gives $T(n) \leq log_{b} a \cdot log_{a} n = \frac {log a}{log b} \cdot \frac {log n}{log a} = \frac {log n}{log b} = log_{b} n$. So $T(n) \leq log_{b} n$, and by the definition of $O(log_{b} n)$, $T(n) \in O(log_{b} n)$, proving the theorem, showing that $O(log_{2} n)$ is the same as $O(log_{5} n)$. 
