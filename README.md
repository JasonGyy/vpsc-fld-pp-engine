# VPSC-FLD-PP-ENGINE
Essential python scripts incorporated in VPSC-FLD-YLD to enable multi-threaded and
highly efficient computations to *predict* forming limit diagram (FLD) on the basis of
ViscoPlastic Self-Consistent (VPSC) crystal plasticity code developed by R. Lebensohn and C. Tome.
VPSC-FLD-YLD can be also used to characterize anisotropic yield functions on the basis of virtual experiments using VPSC.

Note that VPSC-FLD-YLD is a separate repository but maintained in a private sector of USNISTGOV account in GitHub.
The essential portion of VPSC-FLD-YLD (other than VPSC portion) is publicly stored in this repository
for those who want to have a quick look at how Marciniak-Kuczynski model was incorporated into VPSC and how the multi-threaded
computation for VPSC-FLD was realized using Python's multiprocessing package.


## FEATURES
1. FLD calculation using the micro-mechanical descriptions as employed in
 the original VPSC7b(7d) code (Ref. [3,7]).
 An FLD prediction example can be found in the below figures:
![image of VPSC-FLD result for an aluminum](https://github.com/youngung/vpsc-fld-pp-engine/blob/dev/images/vpsc-fld-ex01.png)
2. Link with anisotropic yield function (VPSC-YLD)
  One can charcterize anisotropic yield function (e.g., yld2000-2d) through virtual tests
  Various examples are included
  1. Various types of polycrystal yield surfaces using different amount of offset strains
  ![image of VPSC-YLD-ex02](https://github.com/youngung/vpsc-fld-pp-engine/blob/dev/images/vpsc-yld-ex02.png)
  2. Subsequent evolution of polycrystalline yield surface by sequential uniaxial tension tests along RD, TD and again RD.
  ![image of VPSC-YLD-ex06](https://github.com/youngung/vpsc-fld-pp-engine/blob/dev/images/vpsc-yld-ex06.png)
  3. Polycrystalline backstress can be mapped to the macro-scopic stress space as well
  ![image of VPSC-YLD-ex06c](https://github.com/youngung/vpsc-fld-pp-engine/blob/dev/images/vpsc-yld-ex06c.png)
  4. Modules that can *characterize* state variables for the homogeneous anisotropic hardening (HAH) model.
  ![image of VPSC-YLD-ex08](https://github.com/youngung/vpsc-fld-pp-engine/blob/dev/images/vpsc-yld-ex08.png)
3. Characterize homogeneous anisotropic hardening parameters.
The homogeneous anisotropic hardening (HAH) parameters can be obtained
through virtual experiments using the crystallographic RGVB model that account
for dislocation-density based hardening (Ref. [1,2,4])
  1. Through virtual experiments using VPSC-RGVB, one directly compare with distortional yield surface evolution by HAH approach
  ![image of VPSC-YLD-ex08b](https://github.com/youngung/vpsc-fld-pp-engine/blob/dev/images/vpsc-yld-ex08b.png)


------------------------------------------------------------------------
## REFERENCES (This software has been used in below)
1. [A comparative study between micro- and macro-mechanical constitutive models developed for complex loading scenarios](http://dx.doi.org/10.1016/j.ijplas.2016.07.015),
 **Y. Jeong**, F. Barlat, C. Tome, W. Wen, International Journal of Plasticity (In press).
2. Advances in Constitutive Modelling of Plasticity for forming Applications,
 F. Barlat, **Y. Jeong**, J. Ha, C. Tome, M-G. Lee, W. Wen, (submitted) AEPA 2016
3. [Forming limit predictions using a self-consistent crystal plasticity framework: a case study for body-centered cubic materials](http://dx.doi.org/10.1088/0965-0393/24/5/055005),
 **Y. Jeong**,  M-S. Pham, M. Iadicola, A. Creuziger, T. Foecke, Modelling and Simulation in Materials Science and Engineering 24 (5), 2016
4. [Validation of Homogeneous Anisotropic Hardening Approach Based on Crystal Plasticity](http://dx.doi.org/10.1063/1.4963544), **Y. Jeong**, F. Barlat, C. Tome, W. Wen (Accepted)
 ESAFORM 2016
5. [Multiaxial constitutive behavior of an interstitial-free steel: measurements through X-ray and digital image correlation](http://dx.doi.org/10.1016/j.actamat.2016.04.013),
 **Y. Jeong**, T. Gnaeupel-Herold, M. Iadicola, A. Creuziger, Acta Materialia 112, 84-93 (2016)
6. [Texture-based forming limit prediction for Mg sheet alloys ZE10 and AZ31](http://dx.doi.org/10.1016/j.ijmecsci.2016.08.013),
Dirk Steglich, **Y. Jeong**, International Journal of Mechanical Sciences 117, p102-114 (2016)
7. [Forming limit diagram predictions using a self-consistent crystal plasticity model: a parametric study](https://doi.org/10.4028/www.scientific.net/KEM.651-653.193),
 **Y. Jeong**, M-S. Pham, M. Iadicola, A. Creuziger, Key Engineering Materials 651,
 193-198 (2015)


Do you want a copy of VPSC-FLD-YLD?
-------------------------------
This repository is not complete since VPSC-FLD-YLD requires VPSC source code.
For those who would like to have an access or to have a copy of the full
VPSC-FLD-YLD code, please contact me via youngung.jeong@gmail.com
