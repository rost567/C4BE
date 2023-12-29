Thise section includes problems about:
1. Economic equilibrium...
   a) Implementing lambda functions for  𝑝𝐷(𝑞) and 𝑝𝑆(𝑞).
   b) Creating a numpy array with quantities ranging from 0 to 200 (e.g., using np.arange or np.linspace) and visualizing the two functions with the plt.plot() method.
   - c) Using the numerical methods to solve the following questions:
   > - >_i) What quantity 𝑞 is demanded only when the price is zero?_
   >   >_ii) What quantity 𝑞 would be supplied by producers if the price is 10?_
   >   >_iii) What is the equilibrium price $𝑝∗$ where $𝑝_𝑆(𝑞*) = 𝑝_𝐷(𝑞∗)$, and what is the corresponding quantity, $𝑞∗$?_
   - d) Comparing the numerical methods, is one method particularly well (or poorly) suited for this problem?
     All methods give similar answers. They are the same within the tolerance range. But, for a better reference let's compare the response times:
     %timeit bisection_root(equi,[80,110]) > 46.2 µs ± 2.35 µs per loop (mean ± std. dev. of 7 runs, 10,000 loops each)
     %timeit regula_falsi(equi, [80,110])  > 18.3 µs ± 752 ns per loop (mean ± std. dev. of 7 runs, 100,000 loops each)
     %timeit newton_root(equi, 110)        > 18.9 µs ± 181 ns per loop (mean ± std. dev. of 7 runs, 100,000 loops each)
