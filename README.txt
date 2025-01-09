EDP v1.0: [https://github.com/Tony-Van/EDP-v1.0]
Tutorial and demo: [https://github.com/Tony-Van/EDP-v1.0/master]

#################################################################################
####################################  README  ####################################
#################################################################################

## 1. Environment
¡¤The EDP v1.0 program is built based on Python 3.7.1 and R 4.2.2. Please run EDP.exe in the appropriate Python or R environment.
       Users may need to install Python in advance (https://www.python.org/)
       Users may need to install RTools in advance (https://cran.r-project.org/bin/windows/Rtools/)

## 2. Packages
¡¤Users may need to install necessary packages in advance to ensure the program can run normally:
#The following are the packages used by developers.
#This does not mean that users must use these versions of the packages.
#They are only for reference.
       1) Python packages£º
	pip install pandas==1.3.5
	pip install joblib==1.2.0
	pip install numpy==1.19.5
	pip install sklearn==1.0.2
	pip install tkinter==8.6
	pip install rpy2==3.5.15
       2) R packages£º
	if (!requireNamespace('stats', quietly = TRUE)) {
	  install.packages('stats', version = "4.2.2", dependencies = TRUE)
	}
	if (!requireNamespace('tcltk', quietly = TRUE)) {
	  install.packages('tcltk', version = "4.2.2", dependencies = TRUE)
	}
   	if (!requireNamespace('jsonlite', quietly = TRUE)) {
	  install.packages('jsonlite', version = "1.8.4", dependencies = TRUE)
	}

## 3. Set R path
¡¤When the user runs EDP.exe for the first time, needs to manually set the "R installation path" and "R user directory" of RTool to complete the settings.
       If you need to modify the RTool address, you can modify it in "EDP_v1.0/path/r_paths.txt", or delete the file and re-run EDP.txt to add the address.

## 4. Input
¡¤EDP v1.0 enables high-throughput analysis of multiple chemicals
¡¤Please save the input dose-response gene data as a "drg.csv" format file
       The example file is in "EDP_v1.0/input/r_paths.txt".
¡¤The following is the input data format:
	Sample1	Sample2	 <--  Column Name (Do not use special characters)
	ESR1	AR             <--  Dose-response gene
	AKT1	TNF
	CYP1A1		 <--  There is no need to fill the rows with NA
	...		 <--  ...

## 4. Run
¡¤Double-click the EDP.exe ("EDP_v1.0/EDP.exe") program and wait for the TK window to display the final result (automatic output):

## 5. Output
¡¤All results are saved in the "EDP_v1.0/output" folder
(5-1)The active substance prediction results are saved in result.txt
       I.EDC represent endocrine-disrupting chemical with clear characteristics
       S.EDC represent suspected endocrine-disrupting chemical
       N.EDC represent not endocrine-disrupting chemical

(5-2)KEGG and Wikipathways pathway enrichment results for each substance are shown in the following files:
       Enrichment_K_{Sample1}.csv for KEGG
       Enrichment_W_{Sample1}.csv for Wikipathway

###########################################################################################################
###########################################################################################################
PS. 
Certainly, it is necessary to clarify that in the current screening process of EDCs by authoritative institutions, in vitro screening is just one tier.
The goal of EDP v1.0 is to facilitate the analysis of high-throughput in vitro sequencing data and provide analysis and evidence for potential endocrine disrupting substances.
