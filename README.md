This repository contains code for Sections 5 and 6 of the paper 

D.B.Rokhlin "Relative utility bounds for empirically optimal portfolios"

Logical file sequence

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

    NYSE_1.cls contains 5651 daily returns of 36 stocks for the period ending in 1984. 

    NYSE_2.cls contains 11178 daily returns of 19 stocks for the period ending in 2006.

    Both datasets are available from the webpage of G.Ottucsak: http://www.cs.bme.hu/~oti/portfolio/data.html.

     NYSE_1_log_GDSEG.ipynb --> log_opt_portf_NYSE_1.txt
     
     """ Computes optimal portfolio weights for NYSE_1 dataset in the case of logarithmic utility.     
         The results for 30 experiments of the GDSEG algorithm are written to the file log_opt_portf_NYSE_1.txt
     """ 
     
    NYSE_1_Table_2.ipynb 
    """  
    (1) takes optimal portfolios from the file log_opt_portf_NYSE_1.txt, which correspond to n_experiment=30 runs
    of the GDSEG algorithm 
    (2) drops small weights and normalizes the remaining ones
    (3) constructs the table containing optimal weights, total wealth and annual return for each portolio
    (4) constructs the table containing minimal and maximal values of each weight in these portfolios 
    (Table 2 of the paper)
    The file log_opt_portf_NYSE_1.txt should be constructed by NYSE_1_log_GDSEG.ipynb beforehand
    """
    
    NYSE_2_log_GDSEG.ipynb --> log_opt_portf_NYSE_2.txt
    """ Computes optimal portfolio weights for NYSE_2 dataset in the case of logarithmic utility.
    The results for 30 experiments of the GDSEG algorithm are written to the file log_opt_portf_NYSE_2.txt
    """
    
    NYSE_2_Table_3.ipynb
    """ 
    (1) takes optimal portfolios from the file log_opt_portf_NYSE_2.txt, which correspond to n_experiment=30 runs
    of the GDSEG algorithm 
    (2) drops small weights and normalizes the remaining ones
    (3) constructs the table containing optimal weights, total wealth and annual return for each portolio
    (4) constructs the table containing minimal and maximal values of each weight in these portfolios 
    (Table 3 of the paper)
    The file log_opt_portf_NYSE_2.txt should be constructed by NYSE_2_log_GDSEG.ipynb beforehand
    """
    
    GDSEG_alpha_ordinary.ipynb --> alpha_ordinary_opt_portf.txt
     """ Computes optimal portfolio weights for NYSE_2 dataset in the case of ordinary power utility.
    For each alpha in alphas=[0.01,0.1,0.2,0.3,0.5,0.75] it takes an output of the GDSEG algorithm, corresponding
    to the largest value of the empirical utility function, obtained after n_experiments=10 experiments. 
    These optimal portfolios are written to the file alpha_ordinary_opt_portf.txt
    """
    
    GDSEG_alpha_relative.ipynb --> alpha_relative_opt_portf.txt
     """ Computes optimal portfolio weights for NYSE_2 dataset in the case of the relative power utility.
     For each alpha in alphas=[0.01,0.1,0.2,0.3,0.5,0.75] it takes an output of the GDSEG algorithm, corresponding
     to the largest value of the empirical utility function, obtained after n_experiments=10 experiments. 
    These optimal portfolios are written to the file alpha_relative_opt_portf.txt
    """
    
     alpha_Table_4.ipynb
    """  
    (1) takes optimal portfolios for ordinary and relative power utilies from the files 
    alpha_ordinary_opt_portf.txt and alpha_relative_opt_portf, computed by the notebooks 
    GDSEG_alpha_ordinary.ipynb and GDSEG_alpha_relative.ipynb  
    (2) drops small weights and normalizes the remaining ones
    (3) constructs the tables containing optimal weights, total wealth, annual return and annual
    olatility for each porftolio (Table 4 of the paper)
     """
     
    Table_5.ipynb
    """ 
    (1) computes the parameters of the Black-Scholes model for NYSE_2 dataset
    (2) takes optimal portfolios for ordinary and relative power utilies from the files 
    alpha_ordinary_opt_portf.txt and alpha_relative_opt_portf, formed by the notebooks 
    GDSEG_alpha_ordinary.ipynb and GDSEG_alpha_relative.ipynb  
    (3) drops small weights and normalizes the remaining ones
    (4) evaluates statistical characteristics of the cumulative wealth of these portfolios, using 
    large number (n_BS_realizations=100000) of realizations of the Black-Scholes model; the same for 
    uniform and log-optimal portfolios (Table 5 of the paper)
     """
    
    BS_model_opt_portf.ipynb
    """ Computes computes optimal portfolios, running GDSEG for n_realizations (number of realizations), 
    generated by the Black-Scholes model, whose parameters are evaluated for NYSE_2 dataset
    """
    
    BS_model_hist.ipynb
    """ This notebook computes Figure 4 of the paper
    (1) downloads optimal portfolio weights from the file portf_al02.txt
    (2) evaluates their true utilities
    (3) computes Figure 4 of the paper
    """

