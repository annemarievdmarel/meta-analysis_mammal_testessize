# meta-analysis_mammal_testessize

We provide the code and data to perform the analyses in the manuscript discussing the association between male (relative testes size) and female (litter size, litters per year) reproductive investment dependent on differing mating systems and care systems in terrestrial mammals. We were invited to write this manuscript for a special issue in Journal of Zoology. 

Annemarie van der Marel(a,b), Miyako H. Warrington(b), Jane M. Waterman(b,c) 

    a- Departamento de Ecología, Pontificia Universidad Católica de Chile, Santiago, Chile 
    b- Department of Biological Sciences, University of Manitoba, Winnipeg, MB, Canada
    c- Mammal Research Institute, Department of Zoology and Entomology, University of Pretoria, Pretoria 0002, South Africa

The Rmarkdown file called '2_run models(littersize1).Rmd' contains all the code to run the phylogenetically controlled mixed models. The file called '3.model results.Rmd' summarizes the results from the models and '4.visualise_results.Rmd' creates the figures. 

We compiled the terrestrial mammalian data into one data frame called "rts_life_mating_care.csv"

    order        = order of the species
    family       = family of the species
    common_name  = common name of the species
    Binomial     = scientific name of the species
    rts          = relative testes size calculated using the equation y = 0.035x^0.72, where the mass of the testes is y and the body mass is x. The relative testes    size is the ratio of observed testes size to the testes size predicted by this equation (Kenagy & Trombulak, 1986).  
    exp.testes   = expected testes size
    testes_g     = testes size in g
    log.testes.  = log testes size
    ref_testes   = the source from where we got testes size data
    BM_g         = body mass in g
    log.bm.      = log body mass
    ref_bm       = the source from where we got body mass data
    litter_size  = number of offspring in a single litter
    litter_year  = number of litters per year
    longevity    = maximum lifespan
    ref_lifehistory    = the source from where we got life history data
    mating_system      = primary mating system recorded, either monogamous, polygynous, or promiscuous
    ref_mating_system  = the source from where we got mating system data
    paternal_care      = whether paternal care is present or absent
    ref_paternal_care  = the source from where we got paternal care data

We obtained phylogenetic tree from http://vertlife.org/phylosubsets. The phylogenetic tree is called '571mammals.nex'. 

We also included the complete dataset ("testes_lifehistory_mating_care_Dec17.csv") where we did not filter out aquatic mammals. We offer this resource so that others could use this extensive dataset for their own research questions and can expand our dataset.

# License and citation

DOI code and data: 10.5281/zenodo.7853370 
Manuscript: van der Marel A, Warrington MH, Waterman JM. 2023. Size is not everything: Nuanced effects of female multiple mating and annual litter number on testes size in terrestrial mammals. Journal of Zoology 322(2):101-112. https://doi.org/10.1111/jzo.13132

# info of our R session
R version 4.2.2 (2022-10-31 ucrt)
Platform: x86_64-w64-mingw32/x64 (64-bit)
Running under: Windows 10 x64 (build 22621)

Matrix products: default

locale:
[1] LC_COLLATE=English_Canada.utf8  LC_CTYPE=English_Canada.utf8   
[3] LC_MONETARY=English_Canada.utf8 LC_NUMERIC=C                   
[5] LC_TIME=English_Canada.utf8    

attached base packages:
[1] stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
 [1] RColorBrewer_1.1-3  viridis_0.6.2       viridisLite_0.4.1   rlang_1.1.0        
 [5] rstan_2.26.16       StanHeaders_2.26.16 brms_2.19.0         Rcpp_1.0.10        
 [9] phytools_1.5-1      maps_3.4.1          ape_5.7-1           job_0.3.0          
[13] lubridate_1.9.2     forcats_1.0.0       stringr_1.5.0       dplyr_1.1.1        
[17] purrr_1.0.1         readr_2.1.4         tidyr_1.3.0         tibble_3.2.1       
[21] ggplot2_3.4.2       tidyverse_2.0.0    

loaded via a namespace (and not attached):
  [1] TH.data_1.1-1           colorspace_2.1-0        ellipsis_0.3.2         
  [4] estimability_1.4.1      markdown_1.5            base64enc_0.1-3        
  [7] rstudioapi_0.14         farver_2.1.1            optimParallel_1.0-2    
 [10] DT_0.27                 fansi_1.0.4             mvtnorm_1.1-3          
 [13] bridgesampling_1.1-2    codetools_0.2-18        splines_4.2.2          
 [16] mnormt_2.1.1            doParallel_1.0.17       knitr_1.42             
 [19] shinythemes_1.2.0       bayesplot_1.10.0        jsonlite_1.8.4         
 [22] shiny_1.7.4             compiler_4.2.2          emmeans_1.8.5          
 [25] backports_1.4.1         Matrix_1.5-1            fastmap_1.1.1          
 [28] cli_3.6.1               later_1.3.0             htmltools_0.5.5        
 [31] prettyunits_1.1.1       tools_4.2.2             igraph_1.4.1           
 [34] coda_0.19-4             gtable_0.3.3            glue_1.6.2             
 [37] clusterGeneration_1.3.7 reshape2_1.4.4          posterior_1.4.1        
 [40] V8_4.2.2                fastmatch_1.1-3         vctrs_0.6.1            
 [43] nlme_3.1-160            iterators_1.0.14        crosstalk_1.2.0        
 [46] tensorA_0.36.2          xfun_0.38               ps_1.7.4               
 [49] timechange_0.2.0        mime_0.12               miniUI_0.1.1.1         
 [52] lifecycle_1.0.3         phangorn_2.11.1         gtools_3.9.4           
 [55] MASS_7.3-58.1           zoo_1.8-11              scales_1.2.1           
 [58] colourpicker_1.2.0      hms_1.1.3               promises_1.2.0.1       
 [61] Brobdingnag_1.2-9       parallel_4.2.2          sandwich_3.0-2         
 [64] expm_0.999-7            inline_0.3.19           shinystan_2.6.0        
 [67] yaml_2.3.7              curl_5.0.0              gridExtra_2.3          
 [70] loo_2.6.0               stringi_1.7.12          dygraphs_1.1.1.6       
 [73] plotrix_3.8-2           foreach_1.5.2           checkmate_2.1.0        
 [76] pkgbuild_1.4.0          pkgconfig_2.0.3         matrixStats_0.63.0     
 [79] distributional_0.3.2    evaluate_0.20           lattice_0.20-45        
 [82] rstantools_2.3.1        htmlwidgets_1.6.2       processx_3.8.0         
 [85] tidyselect_1.2.0        plyr_1.8.8              magrittr_2.0.3         
 [88] R6_2.5.1                generics_0.1.3          combinat_0.0-8         
 [91] multcomp_1.4-23         pillar_1.9.0            withr_2.5.0            
 [94] fitdistrplus_1.1-8      xts_0.13.0              scatterplot3d_0.3-43   
 [97] survival_3.4-0          abind_1.4-5             crayon_1.5.2           
[100] utf8_1.2.3              tzdb_0.3.0              rmarkdown_2.21         
[103] grid_4.2.2              callr_3.7.3             threejs_0.3.3          
[106] digest_0.6.31           xtable_1.8-4            numDeriv_2016.8-1.1    
[109] httpuv_1.6.9            RcppParallel_5.1.7      stats4_4.2.2           
[112] munsell_0.5.0           quadprog_1.5-8          shinyjs_2.1.0     
