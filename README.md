This repository contains code for Sctions 4 and 5 of the paper "Relative utility bounds for empirically optimal portfolios"

Logical file sequences

Section 4

    1_risky_bisection.ipynb
  
    """Bisection method for the power utility u(x)=x**alpha in the case of 1 risky asset. Computes Table 1"""
    
    1_risky_figures.ipynb
    
    """ This notebook computes Figures 1-3 """
    
Section 5

     NYSE_1_log_GDSEG.ipynb --> log_opt_portf_NYSE_1.txt
     
     """ This notebook computes optimal portfolio weights for NYSE_1 dataset in the case of logarithmic utility.     
         The results for 30 experiments of the GDSEG algorithm are written to the file log_opt_portf_NYSE_1.txt
     """ 
     
 NYSE_1_Table_2.ipynb 
   """ This notebook 
  (1) takes optimal portfolios from the file log_opt_portf_NYSE_1.txt, which correspond to n_experiment=30 runs of the GDSEG algorithm 
  (2) drops small weights and normalizes the remaining ones
  (3) constructs the table containing optimal weights, total wealth and annual return for each portolio
  (4) constructs the table containing minimal and maximal values of each weight in these portfolios (Table 2 of the paper)
  The file log_opt_portf_NYSE_1.txt should be constructed by NYSE_1_log_GDSEG.ipynb beforehand
  """
 NYSE_2_log_GDSEG.ipynb --> log_opt_portf_NYSE_2.txt
  """ This notebook computes optimal portfolio weights for NYSE_2 dataset in the case of logarithmic utility.
  The results for 30 experiments of the GDSEG algorithm are written to the file log_opt_portf_NYSE_2.txt
  """
  """ This notebook 
 NYSE_2_Table_3.ipynb
  """ This notebook 
  (1) takes optimal portfolios from the file log_opt_portf_NYSE_2.txt, which correspond to n_experiment=30 runs of the GDSEG algorithm 
  (2) drops small weights and normalizes the remaining ones
  (3) constructs the table containing optimal weights, total wealth and annual return for each portolio
  (4) constructs the table containing minimal and maximal values of each weight in these portfolios (Table 3 of the paper)
  The file log_opt_portf_NYSE_2.txt should be constructed by NYSE_2_log_GDSEG.ipynb beforehand
  """
 GDSEG_alpha_ordinary.ipynb --> alpha_ordinary_opt_portf.txt
  """ This notebook computes optimal portfolio weights for NYSE_2 dataset in the case of ordinary power utility.
  For each alpha in alphas=[0.01,0.1,0.2,0.3,0.5,0.75] it takes an output of the GDSEG algorithm, corresponding to the largest value of the empirical utility function, obtained after n_experiments=10 experiments. 
  These optimal portfolios are written to the file alpha_ordinary_opt_portf.txt
  """
 GDSEG_alpha_relative.ipynb --> alpha_relative_opt_portf.txt
  """ This notebook computes optimal portfolio weights for NYSE_2 dataset in the case of the relative power utility.
  For each alpha in alphas=[0.01,0.1,0.2,0.3,0.5,0.75] it takes an output of the GDSEG algorithm, corresponding to the largest value of the empirical utility function, obtained after n_experiments=10 experiments. 
  These optimal portfolios are written to the file alpha_relative_opt_portf.txt
  """
 alpha_Table_4.ipynb
  """ This notebook 
  (1) takes optimal portfolios for ordinary and relative power utilies from the files alpha_ordinary_opt_portf.txt and alpha_relative_opt_portf, computed by the notebooks GDSEG_alpha_ordinary.ipynb and GDSEG_alpha_relative.ipynb  
  (2) drops small weights and normalizes the remaining ones
  (3) constructs the tables containing optimal weights, total wealth, annual return and annual volatility for each porftolio (Table 4 of the paper)
  """
 Table_5.ipynb
  """ This notebook 
  (1) computes the parameters of the Black-Scholes model for NYSE_2 dataset
  (2) takes optimal portfolios for ordinary and relative power utilies from the files alpha_ordinary_opt_portf.txt and alpha_relative_opt_portf, 
  formed by the notebooks GDSEG_alpha_ordinary.ipynb and GDSEG_alpha_relative.ipynb  
  (3) drops small weights and normalizes the remaining ones
  (4) evaluates statistical characteristics of the cumulative wealth of these portfolios, using large number (n_BS_realizations=100000) of realizations of the Black-Scholes model; 
  the same for uniform and log-optimal portfolios (Table 5 of the paper)
  """
