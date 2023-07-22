---
layout: post
mathjax: true
categories: media
title: "Simulating and Analyzing Neutrino Interactions via GENIE"
---

This post aims to share the author's research experience in simulating and analyzing neutrino interactions via GENIE. Since the author is still green in neutrino physics research, the following content might not be very accurate. The readers may refer to the [GENIE manual](https://genie-docdb.pp.rl.ac.uk/cgi-bin/ShowDocument?docid=2) for detailed information.

To install GENIE, you might refer to my previous post about [installing GENIE on Ubuntu Linux]()

### Generating Neutrino Interaction Events
To begin with, for example, we generate 20,000 events of muon-neutrino with energy 0.1 GeV interacting with Carbon 12 at rest, using the pre-computed cross-section files from Fermi Lab:
```
$ gevgen -n 20000 -e 0.1 -p 14 -t 1000060120 --cross-sections /THE/PATH/TO/cross-sections/gxspl-NUsmall.xml
```
The `gevgen` command would generate a ROOT file named `gntp.0.ghep.root` under the same directory, in which all the interaction information is stored. The ROOT file could also be converted to other ROOT formats like `gst`, `rootracker` etc, from which users may operate the branches and obtain the information. However, the pre-determined branches in those converted files may not be exactly what we want. Thus here we focus on extracting the information from the event records directly, which is a more general method. An example of the event record is shown below:
```
1689147164 NOTICE gevdump : [n] <gEvDump.cxx::main (177)> :  ** Event: 0

|------------------------------------------------------------------------------------------------------------------|
|GENIE GHEP Event Record [print level:   3]                                                                        |
|------------------------------------------------------------------------------------------------------------------|
| Idx |          Name | Ist |        PDG |   Mother  | Daughter  |      Px |      Py |      Pz |       E |      m  | 
|------------------------------------------------------------------------------------------------------------------|
|   0 |         nu_mu |   0 |         14 |  -1 |  -1 |   4 |   4 |   0.000 |   0.000 |   0.100 |   0.100 |   0.000 | 
|   1 |           C12 |   0 | 1000060120 |  -1 |  -1 |   2 |   3 |   0.000 |   0.000 |   0.000 |  11.175 |  11.175 | 
|   2 |       neutron |  11 |       2112 |   1 |  -1 |   5 |   5 |   0.132 |  -0.033 |   0.151 |   0.919 | **0.940 | M = 0.896 
|   3 |           C11 |   2 | 1000060110 |   1 |  -1 |   7 |   7 |  -0.132 |   0.033 |  -0.151 |  10.256 |  10.254 | 
|   4 |         nu_mu |   1 |         14 |   0 |  -1 |  -1 |  -1 |   0.026 |   0.014 |  -0.018 |   0.035 |   0.000 | P = (-0.759,-0.403,0.511)
|   5 |       neutron |  14 |       2112 |   2 |  -1 |   6 |   6 |   0.106 |  -0.047 |   0.269 |   0.984 |   0.940 | FSI = 1
|   6 |       neutron |   1 |       2112 |   5 |  -1 |  -1 |  -1 |   0.070 |  -0.031 |   0.177 |   0.959 |   0.940 | 
|   7 |      HadrBlob |  15 | 2000000002 |   3 |  -1 |  -1 |  -1 |  -0.132 |   0.033 |  -0.151 |  10.256 | **0.000 | M = 10.254 
|   8 |      NucBindE |   1 | 2000000101 |  -1 |  -1 |  -1 |  -1 |   0.036 |  -0.016 |   0.092 |   0.025 | **0.000 | M = -0.097 
|------------------------------------------------------------------------------------------------------------------|
|       Fin-Init:                                                |   0.000 |   0.000 |  -0.000 |   0.000 |         | 
|------------------------------------------------------------------------------------------------------------------|
|       Vertex:          nu_mu @ (x =     0.00000 m, y =     0.00000 m, z =     0.00000 m, t =    0.000000e+00 s)  |
|------------------------------------------------------------------------------------------------------------------|
| Err flag [bits:15->0] : 0000000000000000    |  1st set:                                                     none | 
| Err mask [bits:15->0] : 1111111111111111    |  Is unphysical:    NO |   Accepted:   YES                          |
|------------------------------------------------------------------------------------------------------------------|
| sig(Ev) =       4.68711e-40 cm^2  | dsig(Q2;E)/dQ2 =          5.28640e-39 cm^2/GeV^2 | Weight =          1.00000 |
|------------------------------------------------------------------------------------------------------------------|

--------------------------------------------------------------------------------------------------------------
GENIE Interaction Summary
--------------------------------------------------------------------------------------------------------------
[-] [Init-State] 
 |--> probe        : PDG-code = 14 (nu_mu)
 |--> nucl. target : Z = 6, A = 12, PDG-Code = 1000060120 (C12)
 |--> hit nucleon  : PDC-Code = 2112 (neutron)
 |--> hit quark    : no set
 |--> probe 4P     : (E =     0.100000, Px =     0.000000, Py =     0.000000, Pz =     0.100000)
 |--> target 4P    : (E =    11.174863, Px =     0.000000, Py =     0.000000, Pz =     0.000000)
 |--> nucleon 4P   : (E =     0.918824, Px =     0.132484, Py =    -0.033330, Pz =     0.150874)
[-] [Process-Info]  
 |--> Interaction : Weak[NC]
 |--> Scattering  : QES
[-] [Kinematics]
 |--> *Selected* Bjorken x = 0.116015
 |--> *Selected* Inelasticity y = 0.589016
 |--> *Selected* Momentum transfer Q2 (>0) = 0.010496
 |--> *Selected* Hadronic invariant mass W = 0.939565
[-] [Exclusive Process Info] 
 |--> charm prod.  : false |--> strange prod.  : false
 |--> f/s nucleons : N(p) = 0 N(n) = 0
 |--> f/s pions    : N(pi^0) = 0 N(pi^+) = 0 N(pi^-) = 0
 |--> f/s Other    : N(gamma) = 0 N(Rho^0) = 0 N(Rho^+) = 0 N(Rho^-) = 0
 |--> resonance    : [not set]
 |--> final quark prod.  : false
 |--> final lepton prod.  : false
--------------------------------------------------------------------------------------------------------------
```
The event record contains all the particles involved in this reaction and their related information in the order of their appearance. As we could see, the incoming muon-neutrino $$\nu_\mu$$ (`Idx = 0`) interacts with $$^{12}C$$ (`Idx = 1`) at the beginning, thus their "mother" particle has `Idx = -1`. $$\nu_\mu$$ (Idx = 0)'s daughter particle has `Idx = 4`, which means that it produces $$\nu_\mu$$ (`Idx = 4`). For $$^{12}C$$, the indices of its daughter particles range from `2` to `3`, which means that $$^{12}C$$ produces a neutron (`Idx = 2`) and a $$^{11}C$$ (`Idx = 3`). This works for all the particles in the event record. One can find that if a particle has a daughter with `Idx = -1`, it should be a final-state particle. 

It should be noted that the particles with `PDG > 2000000000` are *pseudo particles* created by GENIE. For example, `HadrBlob` represents the final-state nucleus, and `NucBindE` stands for nuclear binding energy. When counting the final-state particles, `NucBindE` will not be included and the type of `HadrBlob` could be implied by writing down the reaction equation:

$$\nu_\mu+^{12}C\to\nu_\mu+n+^{11}C.$$

Then we use the `gevdump` command to output the event records into a text file named `example.txt`:


### Three C++/C Programs Used in Analyzing the Event Records
```
$ g++ getdata.cpp
$ ./a.out
```



```
 *************************************************************************
 Reading completed.
 Number of total input events: 20000
 *************************************************************************
 Please input the option command:
 0 - Quit;
 1 - Multiplicity of total, charged and uncharged final-state particles;
 2 - Types of final-state nuclei (HadrBlob);
 3 - Momentum and energy distribution for a specific final-state particle;
 4 - Momentum and energy versus multiplicity for a specific final-state particle.
 -------------------------------------------------------------------------
1
 -------------------------------------------------------------------------
 Multiplicity for final state particles
 Number of final state particles of all events: 85008
 Average final state particles per event: 4.2504
 Standard deviation of the average number: 0.0178508
 Denote the number of final state particles of a single event as n_i
 -------------------------------------------------------------------------
 n_0 = 0
 n_1 = 0
 n_2 = 0
 n_3 = 9687
 n_4 = 6747
 n_5 = 686
 n_6 = 522
 n_7 = 474
 n_8 = 440
 n_9 = 362
 n_10 = 313
 n_11 = 299
 n_12 = 228
 n_13 = 242
 n_14 = 0
 n_15 = 0
 n_16 = 0
 n_17 = 0
 n_18 = 0
 n_19 = 0
 n_20 = 0
 n_21 = 0
 n_22 = 0
 n_23 = 0
 n_24 = 0
 n_25 = 0
 n_26 = 0
 n_27 = 0
 n_28 = 0
 n_29 = 0
 -------------------------------------------------------------------------
 Denote the standard deviation of n_i as sigma_n_i
 -------------------------------------------------------------------------
 sigma_n_0 = 0
 sigma_n_1 = 0
 sigma_n_2 = 0
 sigma_n_3 = 98.4226
 sigma_n_4 = 82.1401
 sigma_n_5 = 26.1916
 sigma_n_6 = 22.8473
 sigma_n_7 = 21.7715
 sigma_n_8 = 20.9762
 sigma_n_9 = 19.0263
 sigma_n_10 = 17.6918
 sigma_n_11 = 17.2916
 sigma_n_12 = 15.0997
 sigma_n_13 = 15.5563
 sigma_n_14 = 0
 sigma_n_15 = 0
 sigma_n_16 = 0
 sigma_n_17 = 0
 sigma_n_18 = 0
 sigma_n_19 = 0
 sigma_n_20 = 0
 sigma_n_21 = 0
 sigma_n_22 = 0
 sigma_n_23 = 0
 sigma_n_24 = 0
 sigma_n_25 = 0
 sigma_n_26 = 0
 sigma_n_27 = 0
 sigma_n_28 = 0
 sigma_n_29 = 0
 -------------------------------------------------------------------------
 Multiplicity for charged final state particles
 Number of final state charged particles of all events: 22959
 Average final state particles per event: 1.14795
 Standard deviation of the average number: 0.0153347
 Denote the number of charged final state particles of a single event as n_i
 -------------------------------------------------------------------------
 n_0 = 5220
 n_1 = 11285
 n_2 = 1245
 n_3 = 854
 n_4 = 613
 n_5 = 528
 n_6 = 255
 n_7 = 0
 n_8 = 0
 n_9 = 0
 n_10 = 0
 n_11 = 0
 n_12 = 0
 n_13 = 0
 n_14 = 0
 n_15 = 0
 n_16 = 0
 n_17 = 0
 n_18 = 0
 n_19 = 0
 n_20 = 0
 n_21 = 0
 n_22 = 0
 n_23 = 0
 n_24 = 0
 n_25 = 0
 n_26 = 0
 n_27 = 0
 n_28 = 0
 n_29 = 0
 -------------------------------------------------------------------------
 Denote the standard deviation of n_i as sigma_n_i
 -------------------------------------------------------------------------
 sigma_n_0 = 72.2496
 sigma_n_1 = 106.231
 sigma_n_2 = 35.2846
 sigma_n_3 = 29.2233
 sigma_n_4 = 24.7588
 sigma_n_5 = 22.9783
 sigma_n_6 = 15.9687
 sigma_n_7 = 0
 sigma_n_8 = 0
 sigma_n_9 = 0
 sigma_n_10 = 0
 sigma_n_11 = 0
 sigma_n_12 = 0
 sigma_n_13 = 0
 sigma_n_14 = 0
 sigma_n_15 = 0
 sigma_n_16 = 0
 sigma_n_17 = 0
 sigma_n_18 = 0
 sigma_n_19 = 0
 sigma_n_20 = 0
 sigma_n_21 = 0
 sigma_n_22 = 0
 sigma_n_23 = 0
 sigma_n_24 = 0
 sigma_n_25 = 0
 sigma_n_26 = 0
 sigma_n_27 = 0
 sigma_n_28 = 0
 sigma_n_29 = 0
 -------------------------------------------------------------------------
 Multiplicity for uncharged final state particles
 Number of final state uncharged particles of all events: 62049
 Average final state particles per event: 3.10245
 Standard deviation of the average number: 0.0152847
 Denote the number of uncharged final state particles of a single event as n_i
 -------------------------------------------------------------------------
 n_0 = 0
 n_1 = 0
 n_2 = 5781
 n_3 = 10903
 n_4 = 1163
 n_5 = 813
 n_6 = 588
 n_7 = 483
 n_8 = 269
 n_9 = 0
 n_10 = 0
 n_11 = 0
 n_12 = 0
 n_13 = 0
 n_14 = 0
 n_15 = 0
 n_16 = 0
 n_17 = 0
 n_18 = 0
 n_19 = 0
 n_20 = 0
 n_21 = 0
 n_22 = 0
 n_23 = 0
 n_24 = 0
 n_25 = 0
 n_26 = 0
 n_27 = 0
 n_28 = 0
 n_29 = 0
 -------------------------------------------------------------------------
 Denote the standard deviation of n_i as sigma_n_i
 -------------------------------------------------------------------------
 sigma_n_0 = 72.2496
 sigma_n_1 = 106.231
 sigma_n_2 = 35.2846
 sigma_n_3 = 29.2233
 sigma_n_4 = 24.7588
 sigma_n_5 = 22.9783
 sigma_n_6 = 15.9687
 sigma_n_7 = 0
 sigma_n_8 = 0
 sigma_n_9 = 0
 sigma_n_10 = 0
 sigma_n_11 = 0
 sigma_n_12 = 0
 sigma_n_13 = 0
 sigma_n_14 = 0
 sigma_n_15 = 0
 sigma_n_16 = 0
 sigma_n_17 = 0
 sigma_n_18 = 0
 sigma_n_19 = 0
 sigma_n_20 = 0
 sigma_n_21 = 0
 sigma_n_22 = 0
 sigma_n_23 = 0
 sigma_n_24 = 0
 sigma_n_25 = 0
 sigma_n_26 = 0
 sigma_n_27 = 0
 sigma_n_28 = 0
 sigma_n_29 = 0
 -------------------------------------------------------------------------
 Multiplicity information output completed.
 *************************************************************************
 Please input the option command:
 0 - Quit;
 1 - Multiplicity of total, charged and uncharged final-state particles;
 2 - Types of final-state nuclei (HadrBlob);
 3 - Momentum and energy distribution for a specific final-state particle;
 4 - Momentum and energy versus multiplicity for a specific final-state particle.
 -------------------------------------------------------------------------
2
 -------------------------------------------------------------------------
 There are 19977 HadrBlob(s) in all the events
 H:       133; D:       109; T:        96
 H4:       81; H5:       64; H6:       31
 -------------------------------------------------------------------------
 He3:     100; He4:     110; He5:     109
 He6:     114; He7:      70; He8:      51
 He9:       0; He10:      0;
 -------------------------------------------------------------------------
 Li3:      47; Li4:      83; Li5:     128
 Li6:     176; Li7:     172; Li8:     124
 Li9:     124; Li10:      0; Li11:      0
 Li12:      0;
 -------------------------------------------------------------------------
 Be5:      46; Be6:      92; Be7:     132
 Be8:     190; Be9:     218; Be10:    549
 Be11:      0; Be12:      0
 -------------------------------------------------------------------------
 B6:       20; B7:       71; B8:      125
 B9:      232; B10:    5787; B11:    5018
 B12:       0;
 -------------------------------------------------------------------------
 C8:       32; C9:      135; C10:     388
 C11:    4646; C12:       0;
 -------------------------------------------------------------------------
 The output of HadrBlob types is competed.
 *************************************************************************
 Please input the option command:
 0 - Quit;
 1 - Multiplicity of total, charged and uncharged final-state particles;
 2 - Types of final-state nuclei (HadrBlob);
 3 - Momentum and energy distribution for a specific final-state particle;
 4 - Momentum and energy versus multiplicity for a specific final-state particle.
 -------------------------------------------------------------------------
3
 -------------------------------------------------------------------------
 Please input the PDG code of the particle you want.
 e.g. proton = 2212, neutron = 2112, gamma = 22,
 pi+ = 211, pi- = -211, nucleus = 2000000002
 -------------------------------------------------------------------------
2212
 -------------------------------------------------------------------------
 Please input the momentum / energy you want.
 i.e. Px, Py, Pz, E
 -------------------------------------------------------------------------
Px
 -------------------------------------------------------------------------
 The data has been stored in 'data.txt'.
 Please use 'distribution.C' to plot the histogram.
 *************************************************************************
 Please input the option command:
 0 - Quit;
 1 - Multiplicity of total, charged and uncharged final-state particles;
 2 - Types of final-state nuclei (HadrBlob);
 3 - Momentum and energy distribution for a specific final-state particle;
 4 - Momentum and energy versus multiplicity for a specific final-state particle.
 -------------------------------------------------------------------------
4
 -------------------------------------------------------------------------
 Please input the PDG code of the particle you want.
 e.g. proton = 2212, neutron = 2112, gamma = 22,
 pi+ = 211, pi- = -211, nucleus = 2000000002
 -------------------------------------------------------------------------
2212
 -------------------------------------------------------------------------
 Please input the momentum / energy you want.
 i.e. Px, Py, Pz, E
 -------------------------------------------------------------------------
E
 -------------------------------------------------------------------------
 The data has been stored in 'data2.txt'.
 Please use 'distribution2.C' to plot the histogram.
 *************************************************************************
 Please input the option command:
 0 - Quit;
 1 - Multiplicity of total, charged and uncharged final-state particles;
 2 - Types of final-state nuclei (HadrBlob);
 3 - Momentum and energy distribution for a specific final-state particle;
 4 - Momentum and energy versus multiplicity for a specific final-state particle.
 -------------------------------------------------------------------------
0

```


#### Multiplicity Histograms


#### Final-State Nuclei

#### Momentum/Energy Distributions of a Specific Final-State Particle



### Additional Information
Due to the limited page, the code of the 3 programs will not be shown here. If you are interested, please contact me via my email.
