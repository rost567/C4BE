Thise section includes problems about:
## Economic equilibrium...
   * a) Implementing lambda functions for  𝑝𝐷(𝑞) and 𝑝𝑆(𝑞).
   * b) Creating a numpy array with quantities ranging from 0 to 200 (e.g., using np.arange or np.linspace) and visualizing the two functions with the plt.plot() method.
   - c) Using the numerical methods to solve the following questions:
   > - >_i) What quantity 𝑞 is demanded only when the price is zero?  
   >   >_ii) What quantity 𝑞 would be supplied by producers if the price is 10?  
   >   >_iii) What is the equilibrium price $𝑝∗$ where $𝑝_𝑆(𝑞*) = 𝑝_𝐷(𝑞∗)$, and what is the corresponding quantity, $𝑞∗$?  
   - d) Comparing the numerical methods, is one method particularly well (or poorly) suited for this problem?
     All methods give similar answers. They are the same within the tolerance range. But, for a better reference let's compare the response times:
     %timeit bisection_root(equi,[80,110]) > 46.2 µs ± 2.35 µs per loop (mean ± std. dev. of 7 runs, 10,000 loops each)
     %timeit regula_falsi(equi, [80,110])  > 18.3 µs ± 752 ns per loop (mean ± std. dev. of 7 runs, 100,000 loops each)
     %timeit newton_root(equi, 110)        > 18.9 µs ± 181 ns per loop (mean ± std. dev. of 7 runs, 100,000 loops each)
## Project investment - Present Value 
> **a)** Implementing a function PV that accepts appropriate inputs and returns the present value.
> **b)** Assuming $𝑡 ∈ [0, 1, 2, 3, 4, ..., 10]$. Using list comprehension, create list that contains the corresponding present values and visualize the present values with respect to 𝑡.
> **c)** Assuming $𝑘 ∈ [0, 0.01, ..., 0.10]$. Again, create a list with the corresponding present values.
> **d)** Nested lists with two variables can be created in the fashion

## Hasse's & Collatz's algorithm  
> **a)** Implementing a (regular) function Hasse(x) that accepts an integer value 𝑥𝑡 and returns it successor 𝑥𝑡+1. (Ensure that the argument is never less or equal to zero.)
> **b)** Implementing a function Collatz$(x0)$ that accepts the first element $𝑥_0$ as input and returns a list with the resulting series as a list, and the number of steps (iterations) it took to (first) reach $1$. Example: Collatz$(4)$ should return $([4, 2, 1], 2)$, Collatz(10) should return $([10, 5, 16, 8, 4, 2, 1], 6)$, and so on.
> **c)** For $1 \le 𝑥_0 \le 10′000$, which creates the longest sequence before reaching 1?

