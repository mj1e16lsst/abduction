# abduction
===========

This project is a collection of implementations of the possible world explorer (PWE). For tutorials on PWE usage, see https://github.com/idaks/PW-explorer. Each implementation starts with a dataset and then applies the following procedure:
 - transcribe the dataset to a datalog fact database;
 - create the allowed transformations in datalog;
 - combine the dataset and transformations and solve using clingo via PWE; 
 - create a DiGraph from the clingo output;
 - extract the relevant statistics from the graph. 
 
# Datasets
----------

 The following datasets were evaluated using the above procedue:
  - toyDataSet, a simple relational database contructed using values from (citation needed). Allowed transformations were SQL SELECT, PROJECT, and UPDATE commands.
  - qfix, a relational database example from [1]. Allowed transformations were SQL SELECT, PROJECT, and UPDATE commands.
  - flights, a database of flight logs from https://figshare.com/articles/flights_csv/9820139/1. Allowed transformations are airport-to-airport flight rountes
  
# Required Packages
-------------------

 - astropy
 - clingo
 - graphviz
 - jupyter
 - matplotlib
 - networkx
 - numpy 
 - nxpd 
 - pandas
 - PWE_NB_EXTENSION
 - PW_explorer
 - pygraphviz
  
# Installation 
--------------

 Please use the following commands to setup the required conda environment:
 - conda create -n PWE_explorer python=3.6 astropy jupyter matplotlib numpy nxpd pandas -c potassco clingo -c anaconda graphviz -c anaconda pygraphviz
 - source activate PWE_explorer
 - pip install PW_explorer
 - pip install PWE_NB_Extension
  
  
# References
------------
  
 [1] Wang, X., Meliou, A. and Wu, E., 2017, May. QFix: Diagnosing errors through query histories. In Proceedings of the 2017 ACM International Conference on Management of Data (pp. 1369-1384).


