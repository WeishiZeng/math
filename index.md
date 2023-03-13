<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>MathJax example</title>
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>
<h1>hello</h1>
<body>
<p>
  When \(a \ne 0\), there are two solutions to \(ax^2 + bx + c = 0\) and they are
  \[x = {-b \pm \sqrt{b^2-4ac} \over 2a}.\]
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
</p>
</body>
</html>


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
