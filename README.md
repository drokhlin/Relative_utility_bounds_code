This repository contains code for Sections 5 and 6 of the paper 

D.B.Rokhlin "Relative utility bounds for empirically optimal portfolios"

Section 5

    1_risky_bisection.ipynb
  
    """ Bisection method for the power utility u(x)=x**alpha in the case of 1 risky asset. 
    (1) computes Table 1
    (2) computes the optimal weight of the risky asset and its true utility, using large sample
    """
    
    1_risky_bis_hist.ipynb
    
    """ For alpha=0.2 and n_experiments=200 realizations of daily returns of the risky asset this notebook 
    (1) computes optimal portfolios, usiong the bisection method
    (2) evaluates true utilities of these portfolios, usinng a large sample 
    (3) computes histograms in Fig.1-3 of the paper
    """
    
Section 6

    working_with_datasets.ipynb: computes Tables 2,3 and Figers 2,3. 
    
    Also includes some computations that supports the comments of the paper, concerning risk-return properties of the 
    portfolios obtained by quadratic approximations (1) for the analysed datasets and (2) for the artificial data generated 
    by the geometric Browinian motion model with parameters estimated from the same datasets.  
    
    NYSE_1.cls: 5651 daily returns of 36 stocks from New York Stock Exchange for the period ending in 1984, 
    NYSE_2.cls: 11178 daily returns of 19 stocks from New York Stock Exchange for the period ending in 2006,
    SP500: 1276 daily returns of 25 stocks from SP500 with the largest market capitalization for the period ending in 2003,
    DJIA: 507 daily returns of 30 stocks composing the Dow Jones Industrial Average for the period ending in 2003.

    http://www.cs.bme.hu/~oti/portfolio/data.html
    http://www.cs.technion.ac.il/~rani/portfolios 
    
     
