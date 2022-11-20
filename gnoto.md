Developing Gnoto Tadpoles Manuscript
================
Abby Miller
11/20/2022

# Microbiome data from Experiment 1

#### OTU Richness

    ## Warning: package 'FSA' was built under R version 4.0.5

    ## ## FSA v0.9.3. See citation('FSA') if used in publication.
    ## ## Run fishR() for related website and fishR('IFAR') for related book.

    ##   Tukey multiple comparisons of means
    ##     95% family-wise confidence level
    ## 
    ## Fit: aov(formula = value ~ Treatment, data = richness_exp_1)
    ## 
    ## $Treatment
    ##                                                            diff       lwr
    ## Abx + sterile food-Abx + NonSter. food                -7.666667 -31.75351
    ## Nonsterile + NonSter. food-Abx + NonSter. food        72.833333  48.74649
    ## Nonsterile + sterile food-Abx + NonSter. food         46.666667  22.57982
    ## Nonsterile + NonSter. food-Abx + sterile food         80.500000  56.41315
    ## Nonsterile + sterile food-Abx + sterile food          54.333333  30.24649
    ## Nonsterile + sterile food-Nonsterile + NonSter. food -26.166667 -50.25351
    ##                                                             upr     p adj
    ## Abx + sterile food-Abx + NonSter. food                16.420181 0.8096028
    ## Nonsterile + NonSter. food-Abx + NonSter. food        96.920181 0.0000003
    ## Nonsterile + sterile food-Abx + NonSter. food         70.753514 0.0001432
    ## Nonsterile + NonSter. food-Abx + sterile food        104.586847 0.0000001
    ## Nonsterile + sterile food-Abx + sterile food          78.420181 0.0000204
    ## Nonsterile + sterile food-Nonsterile + NonSter. food  -2.079819 0.0302221

    ## 
    ##  Kruskal-Wallis rank sum test
    ## 
    ## data:  value by Treatment
    ## Kruskal-Wallis chi-squared = 19.361, df = 3, p-value = 0.0002303

    ## Dunn (1964) Kruskal-Wallis multiple comparison

    ##   p-values adjusted with the Holm method.

    ##                                               Comparison          Z
    ## 1               Abx + NonSter. food - Abx + sterile food  1.1039516
    ## 2       Abx + NonSter. food - Nonsterile + NonSter. food -2.8416532
    ## 3        Abx + sterile food - Nonsterile + NonSter. food -3.9456048
    ## 4        Abx + NonSter. food - Nonsterile + sterile food -1.9421371
    ## 5         Abx + sterile food - Nonsterile + sterile food -3.0460886
    ## 6 Nonsterile + NonSter. food - Nonsterile + sterile food  0.8995161
    ##        P.unadj        P.adj
    ## 1 2.696141e-01 0.5392282752
    ## 2 4.488029e-03 0.0179521149
    ## 3 7.959882e-05 0.0004775929
    ## 4 5.212051e-02 0.1563615311
    ## 5 2.318395e-03 0.0115919735
    ## 6 3.683778e-01 0.3683778182

There were violations in the normality assumption looking at the
histogram of the residuals, so I ended up running a Kruskal Wallace test
with a post-hoc Dunn test for pairwise comparison.

#### Shannon Diversity

    ##             Df Sum Sq Mean Sq F value  Pr(>F)   
    ## Treatment    3  3.016  1.0052   5.487 0.00645 **
    ## Residuals   20  3.664  0.1832                   
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

    ##   Tukey multiple comparisons of means
    ##     95% family-wise confidence level
    ## 
    ## Fit: aov(formula = value ~ Treatment, data = shannon_exp_1)
    ## 
    ## $Treatment
    ##                                                            diff          lwr
    ## Abx + sterile food-Abx + NonSter. food               -0.2512260 -0.942874144
    ## Nonsterile + NonSter. food-Abx + NonSter. food        0.6496248 -0.042023311
    ## Nonsterile + sterile food-Abx + NonSter. food         0.4391607 -0.252487477
    ## Nonsterile + NonSter. food-Abx + sterile food         0.9008508  0.209202689
    ## Nonsterile + sterile food-Abx + sterile food          0.6903867 -0.001261477
    ## Nonsterile + sterile food-Nonsterile + NonSter. food -0.2104642 -0.902112311
    ##                                                            upr     p adj
    ## Abx + sterile food-Abx + NonSter. food               0.4404221 0.7417620
    ## Nonsterile + NonSter. food-Abx + NonSter. food       1.3412730 0.0703905
    ## Nonsterile + sterile food-Abx + NonSter. food        1.1308088 0.3128457
    ## Nonsterile + NonSter. food-Abx + sterile food        1.5924990 0.0080479
    ## Nonsterile + sterile food-Abx + sterile food         1.3820348 0.0505240
    ## Nonsterile + sterile food-Nonsterile + NonSter. food 0.4811840 0.8291590

    ## 
    ##  Kruskal-Wallis rank sum test
    ## 
    ## data:  value by Treatment
    ## Kruskal-Wallis chi-squared = 9.1867, df = 3, p-value = 0.02691

    ## Dunn (1964) Kruskal-Wallis multiple comparison

    ##   p-values adjusted with the Holm method.

    ##                                               Comparison          Z     P.unadj
    ## 1               Abx + NonSter. food - Abx + sterile food  0.6531973 0.513629113
    ## 2       Abx + NonSter. food - Nonsterile + NonSter. food -2.0412415 0.041226833
    ## 3        Abx + sterile food - Nonsterile + NonSter. food -2.6944387 0.007050729
    ## 4        Abx + NonSter. food - Nonsterile + sterile food -1.3880442 0.165123590
    ## 5         Abx + sterile food - Nonsterile + sterile food -2.0412415 0.041226833
    ## 6 Nonsterile + NonSter. food - Nonsterile + sterile food  0.6531973 0.513629113
    ##        P.adj
    ## 1 1.00000000
    ## 2 0.20613417
    ## 3 0.04230437
    ## 4 0.49537077
    ## 5 0.16490733
    ## 6 0.51362911

There were violations in the normality assumption again looking at the
histogram of the residuals, so I ended up running a Kruskal Wallace test
with a post-hoc Dunn test for pairwise comparison.

I also tried to log-transform both the Shannon and OTU richness, but it
didn’t fix the violations.

#### Simpsons Diversity

    ##             Df Sum Sq Mean Sq F value Pr(>F)  
    ## Treatment    3  65.49  21.830   2.838  0.064 .
    ## Residuals   20 153.83   7.691                 
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

# Microbiome data from Experiment 2

#### OTU Richness

    ##                 Df Sum Sq Mean Sq F value Pr(>F)    
    ## treatment_group  4  10628    2657   10.03  8e-06 ***
    ## Residuals       43  11394     265                   
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

    ##   Tukey multiple comparisons of means
    ##     95% family-wise confidence level
    ## 
    ## Fit: aov(formula = OUT_Richness ~ treatment_group, data = div_2)
    ## 
    ## $treatment_group
    ##                  diff        lwr       upr     p adj
    ## AMX2-AMX1        -4.2 -26.181614 17.781614 0.9821090
    ## AMX3-AMX1        -2.7 -24.681614 19.281614 0.9966679
    ## AMX4-AMX1       -12.1 -34.081614  9.881614 0.5259868
    ## Nonsterile-AMX1  30.3   8.318386 52.281614 0.0027226
    ## AMX3-AMX2         1.5 -19.224464 22.224464 0.9995817
    ## AMX4-AMX2        -7.9 -28.624464 12.824464 0.8131025
    ## Nonsterile-AMX2  34.5  13.775536 55.224464 0.0002206
    ## AMX4-AMX3        -9.4 -30.124464 11.324464 0.6978818
    ## Nonsterile-AMX3  33.0  12.275536 53.724464 0.0004235
    ## Nonsterile-AMX4  42.4  21.675536 63.124464 0.0000063

We saw differences between all the AMX treated groups and the nonsterile
group.

#### Shannon Diversity

    ##                 Df Sum Sq Mean Sq F value   Pr(>F)    
    ## treatment_group  4  4.345  1.0862   12.08 1.15e-06 ***
    ## Residuals       43  3.868  0.0899                     
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

    ##   Tukey multiple comparisons of means
    ##     95% family-wise confidence level
    ## 
    ## Fit: aov(formula = shannon ~ treatment_group, data = div_2)
    ## 
    ## $treatment_group
    ##                        diff         lwr         upr     p adj
    ## AMX2-AMX1       -0.04402928 -0.44901904  0.36096049 0.9979275
    ## AMX3-AMX1       -0.18007348 -0.58506324  0.22491629 0.7130840
    ## AMX4-AMX1       -0.44982148 -0.85481124 -0.04483171 0.0227893
    ## Nonsterile-AMX1  0.45571512  0.05072536  0.86070489 0.0204587
    ## AMX3-AMX2       -0.13604420 -0.51787221  0.24578381 0.8473726
    ## AMX4-AMX2       -0.40579220 -0.78762021 -0.02396419 0.0322772
    ## Nonsterile-AMX2  0.49974440  0.11791639  0.88157241 0.0048532
    ## AMX4-AMX3       -0.26974800 -0.65157601  0.11208001 0.2780889
    ## Nonsterile-AMX3  0.63578860  0.25396059  1.01761661 0.0002197
    ## Nonsterile-AMX4  0.90553660  0.52370859  1.28736461 0.0000003

We saw differences between all the AMX treated groups and the nonsterile
group. We also saw differences between AMX 4 and AMX1 and AMX2.

#### Simpson Diversity

    ##                 Df Sum Sq Mean Sq F value   Pr(>F)    
    ## treatment_group  4  29.22   7.305    6.65 0.000294 ***
    ## Residuals       43  47.24   1.099                     
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

    ##   Tukey multiple comparisons of means
    ##     95% family-wise confidence level
    ## 
    ## Fit: aov(formula = invsimpson ~ treatment_group, data = div_2)
    ## 
    ## $treatment_group
    ##                       diff        lwr       upr     p adj
    ## AMX2-AMX1       -0.1110843 -1.5264424 1.3042739 0.9994239
    ## AMX3-AMX1       -0.1949139 -1.6102720 1.2204443 0.9948175
    ## AMX4-AMX1       -0.7730671 -2.1884252 0.6422911 0.5335688
    ## Nonsterile-AMX1  1.5214928  0.1061347 2.9368510 0.0295676
    ## AMX3-AMX2       -0.0838296 -1.4182420 1.2505828 0.9997613
    ## AMX4-AMX2       -0.6619828 -1.9963952 0.6724296 0.6232864
    ## Nonsterile-AMX2  1.6325771  0.2981647 2.9669895 0.0096377
    ## AMX4-AMX3       -0.5781532 -1.9125656 0.7562592 0.7321096
    ## Nonsterile-AMX3  1.7164067  0.3819943 3.0508191 0.0058328
    ## Nonsterile-AMX4  2.2945599  0.9601475 3.6289723 0.0001338

We saw differences between all the AMX treated groups and the nonsterile
group.

# Body condition from DNA extraction day (after 5 weeks developing) from Experiment 1

#### These data are from tadpoles before metamorphosis.

    ## tibble [92 × 8] (S3: tbl_df/tbl/data.frame)
    ##  $ Frog_ID         : chr [1:92] "AS_01" "AS_02" "AS_03" "AS_04" ...
    ##  $ Tank            : chr [1:92] "A1" "A3" "A1" "A3" ...
    ##  $ Treatment       : chr [1:92] "Antibiotics_sterile" "Antibiotics_sterile" "Antibiotics_sterile" "Antibiotics_sterile" ...
    ##  $ Experimental_day: num [1:92] 39 39 39 39 39 39 39 39 39 39 ...
    ##  $ Date            : POSIXct[1:92], format: "2021-08-28" "2021-08-28" ...
    ##  $ Mass_g          : num [1:92] 0.43 0.38 0.37 0.6 0.57 0.7 0.07 0.82 0.48 0.26 ...
    ##  $ SVL_mm          : num [1:92] 16.3 17.1 16.3 20.3 20.5 ...
    ##  $ Notes           : logi [1:92] NA NA NA NA NA NA ...

<img width="784" alt="Screen Shot 2022-11-20 at 3 51 17 PM" src="https://user-images.githubusercontent.com/118693385/202933310-920b068d-5bab-4546-9fa6-3fae32c387de.png">



    ##             Df   Sum Sq   Mean Sq F value Pr(>F)  
    ## Treatment    3 0.002033 0.0006776   2.724  0.049 *
    ## Residuals   88 0.021890 0.0002488                 
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

    ##   Tukey multiple comparisons of means
    ##     95% family-wise confidence level
    ## 
    ## Fit: aov(formula = condition ~ Treatment, data = massdat)
    ## 
    ## $Treatment
    ##                                                       diff           lwr
    ## Antibiotics_nonsterile-Antibiotics_sterile   -0.0097946618 -0.0280078469
    ## Nonsterile_nonsterile-Antibiotics_sterile     0.0053641584 -0.0085045804
    ## Nonsterile_sterile-Antibiotics_sterile        0.0057047753 -0.0080165066
    ## Nonsterile_nonsterile-Antibiotics_nonsterile  0.0151588202 -0.0003244128
    ## Nonsterile_sterile-Antibiotics_nonsterile     0.0154994371  0.0001481451
    ## Nonsterile_sterile-Nonsterile_nonsterile      0.0003406169 -0.0094718225
    ##                                                      upr     p adj
    ## Antibiotics_nonsterile-Antibiotics_sterile   0.008418523 0.4975783
    ## Nonsterile_nonsterile-Antibiotics_sterile    0.019232897 0.7423301
    ## Nonsterile_sterile-Antibiotics_sterile       0.019426057 0.6972771
    ## Nonsterile_nonsterile-Antibiotics_nonsterile 0.030642053 0.0572704
    ## Nonsterile_sterile-Antibiotics_nonsterile    0.030850729 0.0469266
    ## Nonsterile_sterile-Nonsterile_nonsterile     0.010153056 0.9997288

We saw differences here between Nonsterile group fed sterile food and
the Antimicrobial treated group fed nonsterile food.

# Body condition from DNA extraction day (after 5 weeks developing) from Experiment 2

#### These data are from tadpoles before metamorphosis.





    ## 
    ##  Kruskal-Wallis rank sum test
    ## 
    ## data:  condition by Treatment
    ## Kruskal-Wallis chi-squared = 12.413, df = 4, p-value = 0.01453

    ## Dunn (1964) Kruskal-Wallis multiple comparison

    ##   p-values adjusted with the Holm method.

    ##            Comparison          Z     P.unadj      P.adj
    ## 1       Abx_1 - Abx_2 -0.0460179 0.963295983 0.96329598
    ## 2       Abx_1 - Abx_3 -0.7362864 0.461556428 1.00000000
    ## 3       Abx_2 - Abx_3 -0.6902685 0.490025360 0.98005072
    ## 4       Abx_1 - Abx_4 -2.8837884 0.003929227 0.03929227
    ## 5       Abx_2 - Abx_4 -2.8377705 0.004542984 0.04088686
    ## 6       Abx_3 - Abx_4 -2.1475020 0.031753341 0.25402672
    ## 7  Abx_1 - Nonsterile -1.8560553 0.063445680 0.44411976
    ## 8  Abx_2 - Nonsterile -1.8100374 0.070289992 0.42173995
    ## 9  Abx_3 - Nonsterile -1.1197689 0.262812262 1.00000000
    ## 10 Abx_4 - Nonsterile  1.0277331 0.304075400 1.00000000

There were violations in normality, so I did a non parametric test
again.

We saw differences in all groups compared to AMX4.

# Body condition from exposure day Experiment 2

#### These data are from froglets after metamorphosis.

    ## tibble [93 × 10] (S3: tbl_df/tbl/data.frame)
    ##  $ Frog_ID         : chr [1:93] "ABX_1_002" "ABX_1_003" "ABX_1_004" "ABX_1_006" ...
    ##  $ Exp_ID          : num [1:93] 220519 220519 220519 220519 220519 ...
    ##  $ Treatment       : chr [1:93] "Bd" "Bd" "Bd" "Bd" ...
    ##  $ Treatment_group : Factor w/ 5 levels "Abx_1","Abx_2",..: 1 1 1 1 1 1 1 1 1 1 ...
    ##  $ Tank group      : num [1:93] 1.1 1.2 1.2 1.2 1.2 1.2 1.2 1.2 1.2 1.2 ...
    ##  $ Date            : num [1:93] 220519 220519 220519 220519 220519 ...
    ##  $ Experimental_day: num [1:93] 0 0 0 0 0 0 0 0 0 0 ...
    ##  $ Mass_g          : num [1:93] 0.76 0.68 0.59 0.67 0.58 0.45 0.51 0.64 1 0.44 ...
    ##  $ SVL_mm          : num [1:93] 20.9 17.4 15.8 18.8 14.6 ...
    ##  $ Notes           : chr [1:93] NA NA NA NA ...

![](gnoto_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

    ##                 Df   Sum Sq   Mean Sq F value   Pr(>F)    
    ## Treatment_group  4 0.004666 0.0011664   11.98 8.15e-08 ***
    ## Residuals       88 0.008569 0.0000974                     
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

    ##   Tukey multiple comparisons of means
    ##     95% family-wise confidence level
    ## 
    ## Fit: aov(formula = condition ~ Treatment_group, data = dat_may)
    ## 
    ## $Treatment_group
    ##                           diff          lwr          upr     p adj
    ## Abx_1-Nonsterile -0.0196137714 -0.029405178 -0.009822365 0.0000026
    ## Abx_2-Nonsterile -0.0225785873 -0.032369994 -0.012787181 0.0000001
    ## Abx_3-Nonsterile -0.0185509089 -0.028342315 -0.008759503 0.0000092
    ## Abx_4-Nonsterile -0.0193003382 -0.029091744 -0.009508932 0.0000038
    ## Abx_2-Abx_1      -0.0029648158 -0.011655916  0.005726285 0.8763170
    ## Abx_3-Abx_1       0.0010628625 -0.007628238  0.009753963 0.9970522
    ## Abx_4-Abx_1       0.0003134332 -0.008377667  0.009004534 0.9999765
    ## Abx_3-Abx_2       0.0040276783 -0.004663422  0.012718779 0.6975857
    ## Abx_4-Abx_2       0.0032782491 -0.005412851  0.011969350 0.8309560
    ## Abx_4-Abx_3      -0.0007494293 -0.009440530  0.007941671 0.9992505

![](gnoto_files/figure-gfm/unnamed-chunk-9-2.png)<!-- -->

We saw differences in all groups compared to the nonsterile group. Now
we saw no differences in antimicrobial groups compared to AMX4.

# Body condition over time

#### These data are from the Bd exposure

    ## Warning: package 'plyr' was built under R version 4.0.5

    ## 
    ## Attaching package: 'plyr'

    ## The following object is masked from 'package:FSA':
    ## 
    ##     mapvalues

    ## tibble [257 × 10] (S3: tbl_df/tbl/data.frame)
    ##  $ Frog_ID         : chr [1:257] "1_002" "1_003" "1_004" "1_006" ...
    ##  $ Exp_ID          : num [1:257] 220519 220519 220519 220519 220519 ...
    ##  $ Treatment       : chr [1:257] "Bd" "Bd" "Bd" "Bd" ...
    ##  $ Treatment_group : num [1:257] 1 1 1 1 1 1 1 1 1 1 ...
    ##  $ Tank group      : num [1:257] 1.1 1.2 1.2 1.2 1.2 1.2 1.2 1.2 1.2 1.2 ...
    ##  $ Date            : num [1:257] 220519 220519 220519 220519 220519 ...
    ##  $ Experimental_day: num [1:257] 0 0 0 0 0 0 0 0 0 0 ...
    ##  $ Mass_g          : num [1:257] 0.76 0.68 0.59 0.67 0.58 0.45 0.51 0.64 1 0.44 ...
    ##  $ SVL_mm          : num [1:257] 20.9 17.4 15.8 18.8 14.6 ...
    ##  $ Group           : chr [1:257] "Abx" "Abx" "Abx" "Abx" ...

    ## Loading required package: lme4

    ## Loading required package: Matrix

    ## Warning: package 'Matrix' was built under R version 4.0.5

    ## 
    ## Attaching package: 'lmerTest'

    ## The following object is masked from 'package:lme4':
    ## 
    ##     lmer

    ## The following object is masked from 'package:stats':
    ## 
    ##     step

    ## Warning: package 'nlme' was built under R version 4.0.5

    ## 
    ## Attaching package: 'nlme'

    ## The following object is masked from 'package:lme4':
    ## 
    ##     lmList

    ## Type III Analysis of Variance Table with Satterthwaite's method
    ##                                    Sum Sq  Mean Sq NumDF   DenDF   F value
    ## Treatment_group                  0.001129 0.000282     4  65.333    4.6051
    ## Experimental_day                 0.095342 0.095342     1 210.702 1555.9442
    ## Treatment_group:Experimental_day 0.000634 0.000159     4 210.603    2.5878
    ##                                     Pr(>F)    
    ## Treatment_group                   0.002451 ** 
    ## Experimental_day                 < 2.2e-16 ***
    ## Treatment_group:Experimental_day  0.037935 *  
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

    ## Linear mixed model fit by REML. t-tests use Satterthwaite's method [
    ## lmerModLmerTest]
    ## Formula: condition ~ Treatment_group * Experimental_day + (1 | Frog_ID)
    ##    Data: bd
    ## 
    ## REML criterion at convergence: -1538
    ## 
    ## Scaled residuals: 
    ##     Min      1Q  Median      3Q     Max 
    ## -2.1656 -0.5945 -0.1168  0.4895  3.3532 
    ## 
    ## Random effects:
    ##  Groups   Name        Variance  Std.Dev.
    ##  Frog_ID  (Intercept) 8.066e-05 0.008981
    ##  Residual             6.128e-05 0.007828
    ## Number of obs: 257, groups:  Frog_ID, 47
    ## 
    ## Fixed effects:
    ##                                     Estimate Std. Error         df t value
    ## (Intercept)                        4.978e-02  4.087e-03  6.354e+01  12.180
    ## Treatment_group1                  -1.985e-02  5.328e-03  6.354e+01  -3.726
    ## Treatment_group2                  -2.043e-02  5.348e-03  6.428e+01  -3.819
    ## Treatment_group3                  -1.664e-02  5.368e-03  6.508e+01  -3.099
    ## Treatment_group4                  -1.741e-02  5.368e-03  6.508e+01  -3.242
    ## Experimental_day                   8.645e-04  4.781e-05  2.053e+02  18.081
    ## Treatment_group1:Experimental_day -4.269e-05  6.234e-05  2.053e+02  -0.685
    ## Treatment_group2:Experimental_day -1.226e-04  6.349e-05  2.075e+02  -1.931
    ## Treatment_group3:Experimental_day -1.685e-04  6.489e-05  2.103e+02  -2.596
    ## Treatment_group4:Experimental_day -1.482e-04  6.489e-05  2.103e+02  -2.284
    ##                                   Pr(>|t|)    
    ## (Intercept)                        < 2e-16 ***
    ## Treatment_group1                  0.000416 ***
    ## Treatment_group2                  0.000304 ***
    ## Treatment_group3                  0.002866 ** 
    ## Treatment_group4                  0.001871 ** 
    ## Experimental_day                   < 2e-16 ***
    ## Treatment_group1:Experimental_day 0.494253    
    ## Treatment_group2:Experimental_day 0.054823 .  
    ## Treatment_group3:Experimental_day 0.010084 *  
    ## Treatment_group4:Experimental_day 0.023358 *  
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Correlation of Fixed Effects:
    ##             (Intr) Trtm_1 Trtm_2 Trtm_3 Trtm_4 Exprm_ T_1:E_ T_2:E_ T_3:E_
    ## Trtmnt_grp1 -0.767                                                        
    ## Trtmnt_grp2 -0.764  0.586                                                 
    ## Trtmnt_grp3 -0.761  0.584  0.582                                          
    ## Trtmnt_grp4 -0.761  0.584  0.582  0.580                                   
    ## Exprmntl_dy -0.472  0.362  0.361  0.359  0.359                            
    ## Trtmnt_1:E_  0.362 -0.472 -0.277 -0.276 -0.276 -0.767                     
    ## Trtmnt_2:E_  0.355 -0.273 -0.465 -0.271 -0.271 -0.753  0.578              
    ## Trtmnt_3:E_  0.348 -0.267 -0.266 -0.457 -0.265 -0.737  0.565  0.555       
    ## Trtmnt_4:E_  0.348 -0.267 -0.266 -0.265 -0.457 -0.737  0.565  0.555  0.543

![](gnoto_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->![](gnoto_files/figure-gfm/unnamed-chunk-10-2.png)<!-- -->

We saw differences between all groups compared to nonsterile group, as
well as a few significant interactions with treatment group over time,
however we saw no differences in change in body condition over time (see
below.)

#### Change in body condition over exposure

![](gnoto_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

    ##                         Df   Sum Sq   Mean Sq F value Pr(>F)
    ## change1$Treatment_group  4 0.001802 0.0004505   1.867  0.137
    ## Residuals               37 0.008927 0.0002413

    ##   Tukey multiple comparisons of means
    ##     95% family-wise confidence level
    ## 
    ## Fit: aov(formula = change1$changeincondition ~ change1$Treatment_group, data = change1)
    ## 
    ## $`change1$Treatment_group`
    ##                           diff          lwr        upr     p adj
    ## Abx_2-Abx_1      -0.0067622929 -0.027222487 0.01369790 0.8762897
    ## Abx_3-Abx_1      -0.0107466505 -0.031869158 0.01037586 0.5949232
    ## Abx_4-Abx_1      -0.0076693817 -0.028791889 0.01345313 0.8346850
    ## Nonsterile-Abx_1  0.0085989976 -0.013345703 0.03054370 0.7932313
    ## Abx_3-Abx_2      -0.0039843576 -0.025622124 0.01765341 0.9839080
    ## Abx_4-Abx_2      -0.0009070888 -0.022544855 0.02073068 0.9999505
    ## Nonsterile-Abx_2  0.0153612905 -0.007079798 0.03780238 0.3039746
    ## Abx_4-Abx_3       0.0030772689 -0.019187809 0.02534235 0.9945691
    ## Nonsterile-Abx_3  0.0193456481 -0.003700897 0.04239219 0.1361897
    ## Nonsterile-Abx_4  0.0162683793 -0.006778166 0.03931492 0.2750780

![](gnoto_files/figure-gfm/unnamed-chunk-11-2.png)<!-- --> No
differences in change in body condition.

\#Bd load for Experiment 2

    ## tibble [252 × 6] (S3: tbl_df/tbl/data.frame)
    ##  $ Sample_ID    : chr [1:252] "ABX_4_068_220609" "ABX_4_073_220609" "ABX_1_002_220609" "ABX_1_003_220609" ...
    ##  $ Frog_ID      : chr [1:252] "ABX_4_068" "ABX_4_073" "ABX_1_002" "ABX_1_003" ...
    ##  $ Bd_Load      : num [1:252] 73.2 183.2 22.7 121.2 56.8 ...
    ##  $ Day          : num [1:252] 21 21 21 21 21 21 21 21 21 21 ...
    ##  $ Treatment    : chr [1:252] "Abx" "Abx" "Abx" "Abx" ...
    ##  $ Abx_Treatment: num [1:252] 4 4 1 1 1 1 1 1 1 1 ...

![](gnoto_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

    ## Warning: package 'DHARMa' was built under R version 4.0.5

    ## This is DHARMa 0.4.5. For overview type '?DHARMa'. For recent changes, type news(package = 'DHARMa')

    ## Linear mixed model fit by REML. t-tests use Satterthwaite's method [
    ## lmerModLmerTest]
    ## Formula: logload ~ Abx_Treatment * Day + (1 | Frog_ID)
    ##    Data: bdload1
    ## 
    ## REML criterion at convergence: 1071.5
    ## 
    ## Scaled residuals: 
    ##     Min      1Q  Median      3Q     Max 
    ## -2.5294 -0.3805  0.1110  0.5182  1.7904 
    ## 
    ## Random effects:
    ##  Groups   Name        Variance Std.Dev.
    ##  Frog_ID  (Intercept) 2.626    1.620   
    ##  Residual             3.966    1.991   
    ## Number of obs: 252, groups:  Frog_ID, 81
    ## 
    ## Fixed effects:
    ##                        Estimate Std. Error         df t value Pr(>|t|)    
    ## (Intercept)           1.982e-13  9.704e-01  1.292e+02   0.000    1.000    
    ## Abx_Treatment1        1.224e-01  1.254e+00  1.418e+02   0.098    0.922    
    ## Abx_Treatment2       -2.016e-13  1.294e+00  1.292e+02   0.000    1.000    
    ## Abx_Treatment3       -1.855e-13  1.329e+00  1.292e+02   0.000    1.000    
    ## Abx_Treatment4       -6.332e-02  1.323e+00  1.345e+02  -0.048    0.962    
    ## Day21                 5.126e+00  1.064e+00  1.384e+02   4.816 3.80e-06 ***
    ## Day35                 4.910e+00  1.064e+00  1.384e+02   4.613 8.94e-06 ***
    ## Day48                 4.997e+00  1.064e+00  1.384e+02   4.695 6.35e-06 ***
    ## Day62                 4.786e+00  1.064e+00  1.384e+02   4.496 1.45e-05 ***
    ## Day75                 6.197e+00  1.372e+00  1.292e+02   4.516 1.40e-05 ***
    ## Abx_Treatment1:Day21  1.864e-01  1.388e+00  1.384e+02   0.134    0.893    
    ## Abx_Treatment2:Day21  4.119e-01  1.419e+00  1.384e+02   0.290    0.772    
    ## Abx_Treatment3:Day21  6.547e-01  1.458e+00  1.384e+02   0.449    0.654    
    ## Abx_Treatment4:Day21 -4.034e-01  1.458e+00  1.384e+02  -0.277    0.782    
    ## Abx_Treatment1:Day35 -1.024e+00  1.406e+00  1.389e+02  -0.729    0.468    
    ## Abx_Treatment2:Day35  2.886e-01  1.419e+00  1.384e+02   0.203    0.839    
    ## Abx_Treatment3:Day35 -1.585e-02  1.458e+00  1.384e+02  -0.011    0.991    
    ## Abx_Treatment4:Day35 -7.311e-02  1.446e+00  1.419e+02  -0.051    0.960    
    ## Abx_Treatment1:Day48  6.456e-01  1.388e+00  1.384e+02   0.465    0.643    
    ## Abx_Treatment2:Day48  8.847e-01  1.419e+00  1.384e+02   0.623    0.534    
    ## Abx_Treatment3:Day48  5.637e-01  1.458e+00  1.384e+02   0.387    0.700    
    ## Abx_Treatment4:Day48  8.642e-01  1.458e+00  1.384e+02   0.593    0.554    
    ## Abx_Treatment1:Day62  4.267e-01  1.388e+00  1.384e+02   0.307    0.759    
    ## Abx_Treatment2:Day62 -6.497e-01  1.419e+00  1.384e+02  -0.458    0.648    
    ## Abx_Treatment3:Day62  9.550e-02  1.458e+00  1.384e+02   0.066    0.948    
    ## Abx_Treatment4:Day62  6.478e-01  1.458e+00  1.384e+02   0.444    0.657    
    ## Abx_Treatment1:Day75 -3.800e-01  1.698e+00  1.792e+02  -0.224    0.823    
    ## Abx_Treatment2:Day75 -2.188e+00  1.830e+00  1.292e+02  -1.196    0.234    
    ## Abx_Treatment3:Day75 -6.324e-01  1.879e+00  1.292e+02  -0.337    0.737    
    ## Abx_Treatment4:Day75  3.045e-01  1.875e+00  1.318e+02   0.162    0.871    
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

    ## 
    ## Correlation matrix not shown by default, as p = 30 > 12.
    ## Use print(x, correlation=TRUE)  or
    ##     vcov(x)        if you need it

    ## Type III Analysis of Variance Table with Satterthwaite's method
    ##                   Sum Sq Mean Sq NumDF   DenDF F value Pr(>F)    
    ## Abx_Treatment       1.18   0.294     4  37.929  0.0742 0.9896    
    ## Day               929.37 185.874     5 137.906 46.8721 <2e-16 ***
    ## Abx_Treatment:Day  38.52   1.926    20 138.450  0.4857 0.9684    
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

![](gnoto_files/figure-gfm/unnamed-chunk-12-2.png)<!-- -->![](gnoto_files/figure-gfm/unnamed-chunk-12-3.png)<!-- -->

No differences among groups.

# Survival to metamorphosis in Experiment 1

    ## Warning: package 'survival' was built under R version 4.0.5

    ## Loading required package: ggpubr

    ## Registered S3 methods overwritten by 'car':
    ##   method       from
    ##   hist.boot    FSA 
    ##   confint.boot FSA

    ## 
    ## Attaching package: 'ggpubr'

    ## The following object is masked from 'package:plyr':
    ## 
    ##     mutate

    ## 
    ## Attaching package: 'survminer'

    ## The following object is masked from 'package:survival':
    ## 
    ##     myeloma

    ## tibble [1,728 × 4] (S3: tbl_df/tbl/data.frame)
    ##  $ Treatment: Factor w/ 4 levels "Abx_nonster",..: 1 1 1 1 1 1 1 1 1 1 ...
    ##  $ Day      : num [1:1728] 1 1 1 1 1 1 1 1 1 1 ...
    ##  $ Survival : num [1:1728] 0 0 0 0 0 0 0 0 0 0 ...
    ##  $ Frog_ID  : chr [1:1728] "AN1" "AN10" "AN11" "AN12" ...

    ## Call: survfit(formula = Surv(surv_1$Day, surv_1$Survival) ~ surv_1$Treatment, 
    ##     type = "kaplan-meier")
    ## 
    ##                 surv_1$Treatment=Abx_nonster 
    ##  time n.risk n.event survival std.err lower 95% CI upper 95% CI
    ##     6    285      31    0.891  0.0184        0.856       0.9281
    ##    28    228      45    0.715  0.0278        0.663       0.7719
    ##    37    171      48    0.515  0.0317        0.456       0.5805
    ##    83    114      48    0.298  0.0300        0.244       0.3630
    ##   150     57      48    0.047  0.0151        0.025       0.0884
    ## 
    ##                 surv_1$Treatment=Abx_ster 
    ##  time n.risk n.event survival std.err lower 95% CI upper 95% CI
    ##     6    285      30   0.8947  0.0182       0.8598        0.931
    ##    28    228      42   0.7299  0.0273       0.6782        0.786
    ##    37    171      45   0.5378  0.0318       0.4790        0.604
    ##    83    114      47   0.3161  0.0310       0.2607        0.383
    ##   150     57      47   0.0555  0.0168       0.0306        0.101
    ## 
    ##                 surv_1$Treatment=Non_nonster 
    ##  time n.risk n.event survival std.err lower 95% CI upper 95% CI
    ##     6    435      43   0.9011  0.0143       0.8735       0.9296
    ##    28    348      58   0.7510  0.0216       0.7098       0.7945
    ##    37    261      57   0.5870  0.0256       0.5389       0.6393
    ##    83    174      73   0.3407  0.0265       0.2925       0.3968
    ##   150     87      73   0.0548  0.0141       0.0331       0.0907
    ## 
    ##                 surv_1$Treatment=Non_ster 
    ##  time n.risk n.event survival std.err lower 95% CI upper 95% CI
    ##     6    435      44   0.8989  0.0145       0.8710        0.928
    ##    28    348      44   0.7852  0.0204       0.7462        0.826
    ##    37    261      46   0.6468  0.0250       0.5996        0.698
    ##    83    174      66   0.4015  0.0284       0.3495        0.461
    ##   150     87      66   0.0969  0.0197       0.0651        0.144

![](gnoto_files/figure-gfm/unnamed-chunk-13-1.png)<!-- -->

    ## Call:
    ## survdiff(formula = Surv(surv_1$Day, surv_1$Survival) ~ surv_1$Treatment)
    ## 
    ##                                N Observed Expected (O-E)^2/E (O-E)^2/V
    ## surv_1$Treatment=Abx_nonster 342      220      198   2.41765    4.8204
    ## surv_1$Treatment=Abx_ster    342      211      198   0.83807    1.6710
    ## surv_1$Treatment=Non_nonster 522      304      302   0.00862    0.0198
    ## surv_1$Treatment=Non_ster    522      266      302   4.37818   10.0323
    ## 
    ##  Chisq= 12.2  on 3 degrees of freedom, p= 0.007

    ## 
    ##  Pairwise comparisons using Log-Rank test 
    ## 
    ## data:  surv_1 and Treatment 
    ## 
    ##             Abx_nonster Abx_ster Non_nonster
    ## Abx_ster    0.5801      -        -          
    ## Non_nonster 0.2262      0.4941   -          
    ## Non_ster    0.0079      0.0282   0.0905     
    ## 
    ## P value adjustment method: BH

# Survival to metamorphosis in Experiment 2

    ## tibble [3,515 × 4] (S3: tbl_df/tbl/data.frame)
    ##  $ Abx_Treatment   : Factor w/ 5 levels "Abx_1","Abx_2",..: 1 1 1 1 1 1 1 1 1 1 ...
    ##  $ Treatment       : Factor w/ 2 levels "Abx","Nonsterile": 1 1 1 1 1 1 1 1 1 1 ...
    ##  $ Experimental_day: num [1:3515] 0 0 0 0 0 0 0 0 0 0 ...
    ##  $ Survival        : num [1:3515] 0 0 0 0 0 0 0 0 0 0 ...

    ## Call: survfit(formula = Surv(surv_2$Experimental_day, surv_2$Survival) ~ 
    ##     surv_2$Abx_Treatment, type = "kaplan-meier")
    ## 
    ##                 surv_2$Abx_Treatment=Abx_1 
    ##  time n.risk n.event survival std.err lower 95% CI upper 95% CI
    ##     5    645      23    0.964  0.0073        0.950        0.979
    ##    21    516      38    0.893  0.0130        0.868        0.919
    ##    42    387      59    0.757  0.0197        0.720        0.797
    ##    82    258      60    0.581  0.0250        0.534        0.632
    ##   150    129      60    0.311  0.0288        0.259        0.373
    ## 
    ##                 surv_2$Abx_Treatment=Abx_2 
    ##  time n.risk n.event survival std.err lower 95% CI upper 95% CI
    ##     5    700      39    0.944 0.00867        0.927        0.961
    ##    21    560      46    0.867 0.01354        0.841        0.894
    ##    42    420      65    0.733 0.01910        0.696        0.771
    ##    82    280      69    0.552 0.02373        0.507        0.601
    ##   150    140      69    0.280 0.02625        0.233        0.336
    ## 
    ##                 surv_2$Abx_Treatment=Abx_3 
    ##  time n.risk n.event survival std.err lower 95% CI upper 95% CI
    ##     5    651      49    0.925  0.0103        0.905        0.945
    ##    21    511      60    0.816  0.0160        0.785        0.848
    ##    42    371      30    0.750  0.0187        0.714        0.788
    ##    82    280      97    0.490  0.0246        0.444        0.541
    ##   150    140      97    0.151  0.0206        0.115        0.197
    ## 
    ##                 surv_2$Abx_Treatment=Abx_4 
    ##  time n.risk n.event survival std.err lower 95% CI upper 95% CI
    ##     5    670      53    0.921  0.0104        0.901        0.942
    ##    21    536      61    0.816  0.0157        0.786        0.847
    ##    42    402      75    0.664  0.0203        0.625        0.705
    ##    82    268      93    0.433  0.0234        0.390        0.482
    ##   150    134      93    0.133  0.0187        0.101        0.175
    ## 
    ##                 surv_2$Abx_Treatment=Nonsterile 
    ##  time n.risk n.event survival std.err lower 95% CI upper 95% CI
    ##     5    255      17    0.933  0.0156        0.903        0.964
    ##    21    204      21    0.837  0.0243        0.791        0.886
    ##    42    153      24    0.706  0.0320        0.646        0.772
    ##    82    102      23    0.547  0.0383        0.477        0.627
    ##   150     51      23    0.300  0.0435        0.226        0.399

![](gnoto_files/figure-gfm/unnamed-chunk-14-1.png)<!-- -->

    ## Call:
    ## survdiff(formula = Surv(surv_2$Experimental_day, surv_2$Survival) ~ 
    ##     surv_2$Abx_Treatment)
    ## 
    ##                                   N Observed Expected (O-E)^2/E (O-E)^2/V
    ## surv_2$Abx_Treatment=Abx_1      774      240      295    10.297    18.078
    ## surv_2$Abx_Treatment=Abx_2      840      288      320     3.255     5.857
    ## surv_2$Abx_Treatment=Abx_3      791      333      305     2.505     4.477
    ## surv_2$Abx_Treatment=Abx_4      804      375      307    15.277    27.119
    ## surv_2$Abx_Treatment=Nonsterile 306      108      117     0.645     0.968
    ## 
    ##  Chisq= 43.8  on 4 degrees of freedom, p= 7e-09

    ## 
    ##  Pairwise comparisons using Log-Rank test 
    ## 
    ## data:  surv_2 and Abx_Treatment 
    ## 
    ##            Abx_1   Abx_2   Abx_3   Abx_4  
    ## Abx_2      0.22871 -       -       -      
    ## Abx_3      0.00017 0.01052 -       -      
    ## Abx_4      5.2e-08 1.8e-05 0.09217 -      
    ## Nonsterile 0.22871 0.77054 0.12229 0.00590
    ## 
    ## P value adjustment method: BH
