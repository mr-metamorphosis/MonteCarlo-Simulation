# MonteCarlo-Simulation

### Practical Steps in Monte Carlo Simulation
1. Generate Uncorrelated Normal Random Variables: Start by generating a vector ZZ of uncorrelated standard normal random variables.
2. Covariance Matrix Decomposition: Compute the Cholesky decomposition of the covariance matrix ΣΣ to get LL.
3. Transform to Correlated Variables: Multiply LL by ZZ to obtain the correlated random variables. The resulting vector X=LZX=LZ will have the desired covariance structure ΣΣ.
Example in Finance
In financial applications, such as pricing derivatives or risk management, assets often exhibit correlated movements. For instance, the returns of different stocks might be correlated. To simulate the joint distribution of these returns, Cholesky decomposition is used:

<li> Suppose you have a covariance matrix ΣΣ representing the covariances between the returns of several assets. </li>
<li> Perform Cholesky decomposition on ΣΣ to get LL. </li>
<li> Generate independent standard normal random variables.</li>
<li> Multiply these by LL to get correlated normal variables representing the simulated returns.</li>

This allows you to simulate scenarios that more accurately reflect the real-world correlations between different assets or risk factors.

### Using Cholesky Decomposition
Cholesky decomposition is used in Monte Carlo simulations primarily for generating correlated random variables. Here are the key reasons:
1. Generating Correlated Random Variables: In many Monte Carlo simulations, particularly those used in finance and risk management, it's important to model variables that are not independent but have a specific correlation structure. Cholesky decomposition helps in achieving this by transforming a set of uncorrelated standard normal random variables into correlated normal variables.
2. Efficiency: Cholesky decomposition is computationally efficient. Given a positive definite matrix ΣΣ (the covariance matrix), the Cholesky decomposition produces a lower triangular matrix LL such that Σ=LLTΣ=LLT. This is less computationally intensive than other matrix decompositions like the eigenvalue decomposition.
3. Simplicity: The process is straightforward. You first decompose the covariance matrix ΣΣ into LL. Then, if ZZ is a vector of independent standard normal variables, the product LZLZ yields a vector of normal variables with the desired covariance structure.

### Methods of Calculating Different Aspects During the Simulation.
Ending balances of a portfolio can be calculated using Final account balance
Yearly Returns of a portfolio can be calculated using Interest year over year (in simulation) Overall average rate of return of the portfolio can be calculated using IRR cash flow Fluctuating rate of return year over year
Randomly generated rates of return each year = Rand( ) function
<li> Follows the statistical distribution either Normal or LogNormal(mostly LogNormal) </li>
<li> norm.inv(rand(),mean,std.Dev) —> Normal distribution </li>
<li> Randbetween(a,b)=uniform distribution with lower and upper limits (a,b) </li>
<li> Lognorm </li>
