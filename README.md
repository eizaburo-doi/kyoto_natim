# kyoto_natim
Kyoto Natural Image Dataset

This is a dataset of calibrated color natural images.  The original raw images were acquired in RGB format with 10-bit depth per each color channel to estimate responses of three types of cone photoreceptors (i.e., long (L), medium (M), and short (S) wavelength sensitive cones).

Here we provide MATLAB mat files of nonlinear responses of L-cone (OL), M-cone (OM), and S-cone (OS).

## Description
62 images of natural scenes obtained using a 3CCD digital still camera (HC-2500, Fujifilm, Japan).  Each RGB image (1000x1280 pixels, 10 bits for each R, G, B) were corrected for gamma calibration, effect of iris size, and exposure time.  The linear RGB data were transformed into LMS cone responses using 3 by 3 matrix.  This matrix was derived by minimizing the square errors for 170 surface reflectance functions (Vrhel et al, 1994) rendered by 4 kinds of CIE daylight functions (D50, D55, D65, and D75), and the resulting errors were 0.23%, 0.14%, and 0.04% for L-, M-, and S-cone, respectively.  Its accuracy was validated by a different set of reflectance functions (ColorCheker(R), Macbeth, U.S.A.), and the estimation errors were reasonably small (0.39%, 0.23%, and 0.03% for L-, M-, and S-cone, respectively).  The linear cone response data were further transformed with an empirical cone nonlinear function (Baylor et al., 1987):<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
_r<sub>nl</sub> = 1 –_ exp( _– k  r<sub>l</sub>_ ) <br>
where _r<sub>l</sub>_ is linear cone responses, _r<sub>nl</sub>_ is non-linearly transformed cone responses in the range [0,1], and the parameter _k_ is determined so that the median of _r<sub>nl</sub>_ is 0.5 for each scene and for each cone-type.

For a more complete description, please refer to the appendix of <a href="https://tinyurl.com/bd3ty7ms">Doi et al. (2003)</a>.  Further details of the image calibration can be found in the chapter 2 of my <a href="https://drive.google.com/file/d/0B0YejhPIw9kRSC05N1ZTV0NZYzQ/view?usp=share_link&resourcekey=0-1f-JIDr2t44I8FOehU98sQ">thesis</a>.

## Acknowledgement
The construction of this dataset was supported by Grant-in-Aid for Scientific Research (A)(2) from MEXT (#11309007) to Toshio Inui and by JSPS Research Fellowships for Young Scientists (#200103140) to Eizaburo Doi. We acknowledge Toshikazu Wada for his help with the camera calibration and Kyoto Botanical Gardens for assistance with natural image collection. 

If you use this data set, please cite the following <a href="https://tinyurl.com/bd3ty7ms">paper</a>:<br>
E. Doi, T. Inui, T.-W. Lee, T. Wachtler, and T. J. Sejnowski. Spatiochromatic receptive field properties derived from information-theoretic analyses of cone mosaic responses to natural scenes. _Neural Computation,_ 15:397–417, 2003.






