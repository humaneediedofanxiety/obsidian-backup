**Tags |** #nand2tetris #computer-science

Boolean algebra is a system of mathematics where variables take values in the set {0,1}, representing false and true respectively [Wikipedia](https://en.wikipedia.org/wiki/Boolean_algebra?utm_source=chatgpt.com). This formal system defines operations analogous to arithmetic—AND (·), OR (+), and NOT (′)—but over binary logic values [GeeksforGeeks](https://www.geeksforgeeks.org/boolean-algebra/?utm_source=chatgpt.com).

#### Basic Operations

- **AND (·):** Outputs 1 only if both inputs are 1.
    
- **OR (+):** Outputs 1 if at least one input is 1.
    
- **NOT (′):** Outputs the complement of its single input.
    
- **NAND, NOR, XOR, XNOR:** Derived or composite operations used frequently in circuit design [All About Circuits](https://www.allaboutcircuits.com/technical-articles/boolean-basics/?utm_source=chatgpt.com).
    

#### Axioms and Laws

Boolean algebra obeys a set of foundational axioms (postulates), including:

1. **Commutative laws:** A + B = B + A, A·B = B·A.
    
2. **Associative laws:** (A + B) + C = A + (B + C), (A·B)·C = A·(B·C).
    
3. **Distributive laws:** A·(B + C) = A·B + A·C, A + (B·C) = (A + B)·(A + C).
    
4. **Identity laws:** A + 0 = A, A·1 = A.
    
5. **Null laws:** A + 1 = 1, A·0 = 0.
    
6. **Complement laws:** A + A′ = 1, A·A′ = 0.
    
7. **Idempotent laws:** A + A = A, A·A = A.
    
8. **Absorption laws:** A + A·B = A, A·(A + B) = A.
    
9. **Involution:** (A′)′ = A [GeeksforGeeks](https://www.geeksforgeeks.org/axioms-of-boolean-algebra/?utm_source=chatgpt.com).
    
10. **De Morgan’s theorems:** (A·B)′ = A′ + B′ and (A + B)′ = A′·B′ [Wikipedia](https://en.wikipedia.org/wiki/De_Morgan%27s_laws?utm_source=chatgpt.com).
    

#### Boolean Functions

A Boolean function maps n binary inputs to a single binary output, f: {0,1}ⁿ → {0,1}. These functions abstract the behavior of digital circuits, with each input combination producing a defined output [Wikipedia](https://en.wikipedia.org/wiki/Boolean_function?utm_source=chatgpt.com).

#### Representation

- **Truth table:** Tabulates all 2ⁿ input combinations alongside their outputs.
    
- **Algebraic expression:** Uses Boolean operators (AND, OR, NOT) to denote output logic.
    
- **Logic diagram:** Visualizes gates and connections that realize the function [Basic Electronics Tutorials](https://www.electronics-tutorials.ws/boolean/bool_7.html?utm_source=chatgpt.com).
    

#### Boolean Manipulation and Simplification

By leveraging the axioms above, designers apply identities like consensus (AB + A′C + BC = AB + A′C) and duality to reduce expression complexity [All About Circuits](https://www.allaboutcircuits.com/textbook/digital/chpt-7/boolean-rules-for-simplification/?utm_source=chatgpt.com).

#### De Morgan’s Transformations

Enables converting between AND/OR forms by pushing negations inward, critical for implementing minimal gate-level circuits and for moving expressions into normal forms [Wikipedia](https://en.wikipedia.org/wiki/De_Morgan%27s_laws?utm_source=chatgpt.com).

#### Systematic Simplification

- **Karnaugh maps (K‑maps):** Grid‑based visual tool for up to 6 variables that groups adjacent 1’s to derive simplified SOP expressions without deep algebraic work [GeeksforGeeks](https://www.geeksforgeeks.org/introduction-of-k-map-karnaugh-map/?utm_source=chatgpt.com).
    
- **Quine–McCluskey algorithm:** Tabular method for finding all prime implicants and selecting a minimum cover, scalable to software tools for many variables [Wikipedia](https://en.wikipedia.org/wiki/Quine%E2%80%93McCluskey_algorithm?utm_source=chatgpt.com).

#### Sum of Products (SOP)

Also called **minterm expansion**, SOP expresses a function as a sum (OR) of minterms, where each minterm is the AND of all variables in either true or complemented form. Every function has a unique canonical SOP [GeeksforGeeks](https://www.geeksforgeeks.org/canonical-and-standard-form/?utm_source=chatgpt.com).

#### Product of Sums (POS)

Also called **maxterm expansion**, POS represents a function as a product (AND) of maxterms, where each maxterm is the OR of all variables in true or complemented form. This yields a dual canonical form [GeeksforGeeks](https://www.geeksforgeeks.org/canonical-and-standard-form/?utm_source=chatgpt.com).

#### Applications in Chip Design

Boolean algebra underpins every stage of digital IC design: from high‑level functional specification (truth tables and Boolean functions) through logic optimization (canonical forms and simplification) to gate‑level netlists (NAND‑only or mixed‑gate implementations) and ultimately physical layout [All About Circuits](https://www.allaboutcircuits.com/textbook/digital/chpt-7/boolean-rules-for-simplification/?utm_source=chatgpt.com).

**References.**
[[How to build a computer]]