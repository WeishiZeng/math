## Peano Axioms

- **(Axiom 2.1)** Zero
    - 0 is a natural number
- **(Axiom 2.2)** $++$, the increment operation
    - if $n$ is a natrual number, then $n++$ is also a natural number.
- **(Axiom 2.3)** $0$ is the first
    - $n++ \neq 0$ for every natrual number n
- **(Axiom 2.4)** Uniqueness of increment
    - $n \neq m \implies n++ \neq m++$
- **(Axiom 2.5)** Principal of mathimatical induction
    - $[P(0) \land (P(n) \implies P(n++))] \implies [\forall n P(n)]$
      - $P(n)$ is a property pertaining to natural number $n$
- **(Proposition 2.2.14)** Strong principal of induction
    - $(\forall m \ge m_0) [[(\forall m_0 \le m' < m) P(m') \implies P(m)] \implies (\forall m \ge m_0) P(m)]$
      - $m_0$ is any natrual number, $P(m)$ is a property pertaining to natural number $m$
    - Break down version:
      - $\forall m_0 [(\forall m \ge m_0) Q(m) \implies (\forall m \ge m_0) P(m)]$
      - $Q(m)$ is defined as:
        - $(\forall m_0 \le m' < m) P(m') \implies P(m)$
