# C4BE Part 1
## Economic equilibrium...
   * a) Implementing lambda functions for  𝑝𝐷(𝑞) and 𝑝𝑆(𝑞).
   * b) Creating a numpy array with quantities ranging from 0 to 200 (e.g., using np.arange or np.linspace) and visualizing the two functions with the plt.plot() method.
   - c) Using the numerical methods to solve the following questions:
   > i) What quantity 𝑞 is demanded only when the price is zero?  
   > ii) What quantity 𝑞 would be supplied by producers if the price is 10?  
   > iii) What is the equilibrium price $𝑝∗$ where $𝑝_𝑆(𝑞*) = 𝑝_𝐷(𝑞∗)$, and what is the corresponding quantity, $𝑞∗$?  
   - d) Comparing the numerical methods, is one method particularly well (or poorly) suited for this problem?
     All methods give similar answers. They are the same within the tolerance range. But, for a better reference let's compare the response times:
     %timeit bisection_root(equi,[80,110]) > 46.2 µs ± 2.35 µs per loop (mean ± std. dev. of 7 runs, 10,000 loops each)
     %timeit regula_falsi(equi, [80,110])  > 18.3 µs ± 752 ns per loop (mean ± std. dev. of 7 runs, 100,000 loops each)
     %timeit newton_root(equi, 110)        > 18.9 µs ± 181 ns per loop (mean ± std. dev. of 7 runs, 100,000 loops each)
## Project investment - Present Value 
> **a)** Implementing a function PV that accepts appropriate inputs and returns the present value.  
> **b)** Assuming $𝑡 ∈ [0, 1, 2, 3, 4, ..., 10]$. Using list comprehension, create list that contains the corresponding present values and visualize the present values with respect to 𝑡.  
> **c)** Assuming $𝑘 ∈ [0, 0.01, ..., 0.10]$. Again, create a list with the corresponding present values.  
> **d)** Nested lists with two variables can be created in the fashion.

## Hasse's & Collatz's algorithm  
> **a)** Implementing a (regular) function Hasse(x) that accepts an integer value 𝑥𝑡 and returns it successor 𝑥𝑡+1. (Ensure that the argument is never less or equal to zero).  
> **b)** Implementing a function Collatz$(x0)$ that accepts the first element $𝑥_0$ as input and returns a list with the resulting series as a list, and the number of steps (iterations) it took to (first) reach $1$. Example: Collatz$(4)$ should return $([4, 2, 1], 2)$, Collatz(10) should return $([10, 5, 16, 8, 4, 2, 1], 6)$, and so on.  
> **c)** For $1 \le 𝑥_0 \le 10′000$, which creates the longest sequence before reaching 1?  

# C4BE Part 2
## Stock price 
Assuming a stock price follows a process $𝑆_𝑡 = 𝑆_{𝑡−1} * 𝑒^𝑟_𝑡$. Weekly returns $𝑟_𝑡$ are normally distributed with $𝑟_𝑡 ∼ 𝑁(0.005, 0.03^2)$ (all parameters per week; no further scaling required).  
Using Monte Carlo Simulation to answer the following questions for $𝑇 = 13$ and $𝑇 = 52$ weeks (quarter / whole year).

## Wealth distribution
>**a)** Implementing a function $Gini(L)$ where the input argument L is a function for the Lorenz curve $𝐿(𝑥)$, and which returns the Gini coefficient and the areas 𝐴 and 𝐵.  
>**b)** Using this function Gini(L), find the Gini coefficient when $𝐿(𝑥) = 0.7 ⋅ 𝑥^{2.5} + 0.3 ⋅ 𝑥^{1.2}$

## Optimal combination of two assets
>**a)** Implementing functions util(wA) and SR(wA) that return $𝑈_𝑝$ and $𝑆𝑅_𝑃$, respectively, and take $𝑤_𝐴$ as argument. (The risk aversion parameter 𝛾 and the assets’ parameters for 𝑟 and 𝜎 can be provided, e.g., as arguments with default values or as global variables, but calling the functions with just one argument, $𝑤_𝐴$, should return the correct values).  
>**b)** Assuming that weights have to be non-negative, ie., $0 \le 𝑤_𝐴 \le 1$. Visualize the objective functions as functions of $𝑤_𝐴$.  
>**d)** Now, assuming that weights can also be negative within certain limits; specifically “short-selling” is allowed up to $200%$, $−2.0 \le 𝑤_𝐴 \le 3.0.$. Visualizing SR again for these new bounds. Which of the numerical methods discussed in class can be used to reliably find (ie., are guaranteed to converge to) the maxima?











