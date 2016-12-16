# Getting started
`./mvqtlcim -i example.txt -b 5 -m 1`  
`./mvqtlcim -i example.txt -b 5 -w 15.0 -p 1000 -t 20`  
`./Rscript lrPlot.r -i example_CIM_M1Rst.txt -p example_CIMPermuM1Rst.txt -w 1`
# Introduction
MVQTLCIM is a software package for composite inverval mapping QTLs with multivariate phenotype data in an outbred full-sib family. The software utilizes a genetic linkage map constructed with different segregation molecular markers such as 1:1, 1:2:1 and 1:1:1:1, and assumes that QTL may segregate in the five different segregation patterns on a specific position of the genetic map. It allows users to select the best QTL segregation pattern with AIC, BIC and TIC for a significant QTL. It also provides command line parameters to be chosen for alternative analyses, including the number of background markers, window size ([Basten, et al., 1994](http://statgen.ncsu.edu/qtlcart/WinQTLCart.pdf)), QTL segregation type, genetic map function and number of permutations. Specifically, when performing permutations to determine the empirical threshold of significant QTLs, `mvqtlcim` permits to use multithreads to accelerate computing speed. When an analysis completes, the software will generate two files for each QTL model, of which one contains the parameter estimates and the corresponding statistic values at every 1 cM on the genome, and the other saves the maximum LR value of each permutation. With these result files, we wrote an R script, `lrPlot.r`, to summarize the significant QTL information and generate scatter plots of LR against genome position. These plots can be optionally saved in pdf, jpg, png, tif or bmp format. 
# Usage
With the embedded example input file `example.txt`, users can get started the with following commands:  
`./mvqtlcim -i example.txt -b 5 -m 1`  
`./mvqtlcim -i example.txt -b 5 -w 15.0 -p 1000 -t 20`  
`./Rscript lrPlot.r -i example_CIM_M1Rst.txt -p example_CIMPermuM1Rst.txt -w 1`
