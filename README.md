# Intralipid NIR optical parameter datasheet

Meng, Xiangxi

Georgia Institute of Technology, Emory University, Peking University

mengxiangxi#pku.edu.cn

| Version       | Description  |
| ------------- |:-------------| 
| 20171130      | initial commit |
| 20171212      | add 'Summary' and revise discussion on anisotropy |

## Introduction										
										
Intralipid (IL) has been widely used in the study of biophotonics, yet the optical parameters of absorption coefficient, scattering coefficient, anisotropy and refractive index are often incorrectly cited. Moreover, the parameters of differentconcentrations of IL need to be converted. Thus, I am summarizing various information and compiling it into this interactive Excel file for futre reference.			

I am not an expert on optics or photonics, so there might be some errors. Please contact me via email or GitHub if you think anything is inappropriate. Thank you!										
										
## Using the form										
										
Just input the wavelength and the concentration of IL in yellow cells, and the results will be shown in green cells.										
										
## Absorption coefficient

According to reference [1], within dilutions of 'practical interest' and withnin NIR region, the absorption coefficient is practically equal to that of pure water. This assumption has been adopted by many authors. Thus, the absorption coefficient is represented by the value of pure water taken and interpolated (spline) from reference [2].										
										
The wavelength input here must be an integer between 667 and 2500.										
										
## Scattering Coefficient				

Dependent scattering of IL in NIR range has been well studied by reference [3]. And Mie-theory-based equations have been derived by the authors, which showed good agreement with the experimental results.

The range of the input wavelength should be 600-1850, and the concentration should be no more than 20.

## Anisotropy

A fitted equation of g is provided by reference [4]. Anisotropy is not so significantly dependent on concentrations, thus here a representative value for 20% IL is provided. However, the anisotropy for concentrations less than 2% at a wavelength greater than 1050 nm is not reliable. See reference [4].

The range of the input wavelength should be 500-2500.

## Refractive index

Intralipid is a mixture, thus the refractive index is a nominal property. Real and imaginary refractive indeces have been given in reference [5] with s and p polarized light of the 20% IL as discrete points. In this form, an Akima spline is first interpolated/extrapolated based on the real refractive index of the p-polarized light.	

Next, no study on the concentration dependence of refractive index of IL has been found. Thus, the value for different concentrations is linear interpolated between the refractive index of water and that of the 20% IL. The refractive index of water was taken from reference [6].

The range of the input wavelength should be an integer between 325-1750, and the concentration should be no more than 20.

I am aware of the lack of rigorous derivation in the refractive index estimation. More studies need to be conducted.

## References

1. P. Ninni, F. Martelli, G. Zaccanti, Biomedical optics express 2, 2265–2278 (2011).

2. L. Kou, D. Labrie, P. Chylek, Applied Optics 32, 3531 (1993).

3. B. Aernouts, R. Beers, R. Watté, J. Lammertyn, W. Saeys, Opt Express 22, 6086–98 (2014).

4. B. Aernouts et al., Opt Express 21, 32450 (2013).

5. H. Ding, J. Q. Lu, K. M. Jacobs, X.-H. Hu, Journal of the Optical Society of America A 22, 1151 (2005).

6. G. M. Hale, M. R. Querry, Applied Optics 12, 555 (1973).
