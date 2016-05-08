# kyoto_natim
Kyoto Natural Image Dataset

This is a dataset of calibrated color natural images.  The original images are aquired in the RGB format with intrinsic 10-bit depth per each color channel. Here we also provide a converted version where each pixel consists of simulated responses of three type of cone photoreceptors (i.e., long (L), medium (M), and short (S) types) with a nonlinear (compressive) transform.

Key features:
color natural images, human cone photoreceptor spectral sensitivity, nonlinearity/gamma calibration, large number of samples (originally 1000x1280x3 pixels and 10 bit depth for each R G B plane, utilizing 3CCD chip).

Description:
62 images of natural scenes, obtained using 3CCD digital still camera system (HC-2500, Fujifilm, Japan). Each RGB image (1000x1280 pixels, 10 bits for each R, G, B) were corrected for gamma calibration, effect of iris size, and exposure time.

The linear RGB data were transformed into LMS cone responses using 3 by 3 matrix. This matrix was derived by minimizing the square errors for 170 surface reflectance functions (Vrhel et al, 1994) rendered by 4 kinds of CIE daylight functions (D50, D55, D65, and D75), and the resulting errors were 0.23%, 0.14%, and 0.04% for L-, M-, and S-cone, respectively. Its accuracy was validated by a different set of reflectance functions (ColorCheker(R), Macbeth, U.S.A.), and the estimation errors were reasonably small (0.39%, 0.23%, and 0.03% for L-, M-, and S-cone, respectively).

The linear cone response data were further transformed with an empirical cone nonlinear function (Baylor et al., 1987):
r_{nl} = 1-\exp(-k \cdot \r_l)
where r_l is linear cone responses, r_{rl} is non-linearly transformed cone responses in the range [0,1], and the parameter k is determined so that the median of r_{nl} is 0.5 for each scene and for each cone-type. 

Download:
1. MATLAB .mat files of nonlinear responses of L-cone (OL), M-cone (OM), and S-cone (OS). [download here]

Tips: if you don't need color components, we would suggest to use only "OL" component.

2. The original 30-bit RGB images (in 48-bit TIFF format) [download here]

Acknowledgement:
The construction of this dataset was supported by Grant-in-Aid for Scientific Research (A)(2) from MEXT (#11309007) to Toshio Inui and by JSPS Research Fellowships for Young Scientists (#200103140) to Eizaburo Doi. We acknowledge Toshikazu Wada for his help with the camera calibration and Kyoto Botanical Gardens for assistance with natural image collection. 

***

If you use this data set, please cite the following paper.

Doi, E., Inui, T., Lee, T.-W., Wachtler, T., & Sejnowski, T. J.

Spatiochromatic receptive field properties derived from information-theoretic analyses of cone mosaic responses to natural scenes.
Neural Computation, 2003, vol.15, pp.397-417.

If you have any questions about this dataset, please email me at doie@janelia.hhmi.org






