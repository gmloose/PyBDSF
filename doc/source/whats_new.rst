.. _new:

**********
What's New
**********

    Version 1.12.0 (2024/11/25):
    * Fix string checks and clean up (#243)

    * Fix unintended removal of handlers from the root logger (#245)

    * Fix outdir being ignored (#244)

    * rmsimage negative rms fallback, fixes #215 (#242)

    * Fix bug that resulted in ncores being at most 8 and improve method for getting no. of available cores (#240)

    Version 1.11.1 (2024/09/06):
    * Add macos arm binary wheels (#238)

    * Remove manylinux2014 directory (#237)

    * GitHub action download artifact security update (#236)

    Version 1.11.0 (2024/07/26):
    * Add checks of output to tests (#231)

    * Set upper limit on NumPy version (#230)

    * Output island rms and mean values for wavelet Gaussians (#228)

    * Use setuptools_scm (#224)

    * Fix ReadtheDocs (#223)

    * Remove pyfits version checks (#222)

    * Fix issue with frequency_sp being ignored (#219)

    * Fix python3.12 build (#217)

    * Replace distutils for Python 3.12 (#216)

    * Fix save of residual image and add option to save model image (#213)

    * Fix issues with error estimation (#211)

    * Fix various issue with the spectral index module (#210)

    * Add options for use with a detection image (#209)

    * Use scikit-build (#204)

Version 1.10.3 (2023/05/22):

    * Fix build issue with Python 3.11 (#205)

    * Use cibuildwheel to build binary wheels for Linux and MacOS (Intel); drop support for Python 3.6 (#203)

    * Fix #198. Use the new method call `canvas.manager.set_window_title` (#199)

    * Replace Travis CI with GitHub actions (#196)

Version 1.10.2 (2023/02/10):
    * Fix issues with numpy versions >= 1.24 (#193)

    * Switch to `manylinux2014` for building binary wheels (#191)

    * Fix ImportError in setuptools (#190)

    * Add binary wheels for Python 3.10 (#186)

    * Fix various documentation issues (#185)

    * Add logfilename option (#181)

    * Use len() instead of numpy.alen() (#180)

Version 1.10.1 (2022/02/14):
    * Fix NumPy API compatibility issue

Version 1.10.0 (2022/02/09):
    * Update some functions as required by scipy version >= 1.8.0 (PR #172)

    * Fix build issues with Python 3.8, end support for Python < 3.6, add support for Python 3.8 and 3.9, and make installation of the interactive pybdsf shell optional (PR #169)

    * Improve handling of the beam in the spectral index module (PR #165)

    * Improve handling of large, complex islands (PR #160)

    * Allow a file to be supplied for the ch0 image used in the spectral index module (PR #127)

Version 1.9.2 (2019/12/05):
    * Fix exception behaviour if spline order change does not work

    * Add check for frequency info in header

Version 1.9.1 (2019/09/25):

    * Fix various shapelet decomposition issues

    * Fix crash in Gaussian fitting (#96)

    * Fix blank_limit check_low error (#100)

    * Fix various minor bugs

Version 1.9.0 (2019/03/25):

    * Add support for Python 3

    * Fix various minor bugs

Version 1.8.15 (2018/10/12):

    * Fix segfault in Gaussian fitting (#63)

    * Fix math domain error (#76)

    * Fix setup.py for boost versions > 1.63 (#58)

Version 1.8.14 (2018/05/18):

    * Fix an error on total flux density (#50)

    * Add the possibility to provide an external noise and mean maps (#43)

    * Append the image FITS header into catalog FITS header (#53)

    * Make PyBDSF compatible with newer boost libraries, specifically those used in Ubuntu 18.04 (#55)

Version 1.8.13 (2017/11/17):

    * Remove deprecated boolean operators

Version 1.8.12 (2017/09/01):

    * Fix crash with tiny regions

    * Fix very low centroid peak fluxes

    * Fix compile error with numpy 1.13

Version 1.8.11 (2017/06/01):

    * Fix for interactive shell problem

Version 1.8.10 (2017/05/31):

    * Fixes for various installation and runtime issues on modern systems.

Version 1.8.9 (2017/03/23):

    * Fix to bug that causes an error when grouping Gaussians into sources

Version 1.8.8 (2017/03/17):

    * Rename to PyBDSF

    * Move to python setuptools

    * Move out of the LOFAR tree to github

    * Fix to issues related to numpy versions >= 1.12.0

Version 1.8.7 (2016/06/10):

    * Fix to bug that caused incorrect output images when input image was not square.

Version 1.8.6 (2016/01/20):

    * Fix to bug that caused incorrect island mask when two islands are very close together.

    * Fix to bug that caused crash when image is masked and the ``src_ra_dec`` option is used.

Version 1.8.5 (2015/11/30):

    * Fix to bug in ``export_image`` that resulted in incorrect output image when both ``trim_box`` and ``pad_image`` were used.

    * Fix to bug in wavelet module related to merging of islands.

    * Fix to bug in polarization module related to numbering of new islands.

    * Added option to use much faster (but also much more memory intensive) SciPy ``fftconvolve`` function instead of custom PyBDSM one. The option (``use_scipy_fft``) defaults to ``True``.

    * Increased number of digits for values in output text catalogs

Version 1.8.4 (2015/08/06):

    * Improved speed of wavelet module.

    * Added option to use PyFFTW in wavelet module if available.

    * Fix to IPython version check.

    * Fix to bug that caused a failure to write shapelet models in FITS format.

    * Fix to bug that caused a crash when both ``atrous_do = True`` and ``output_all = True``.

    * Fixed a bug that caused a crash on machines with only one core.

Version 1.8.3 (2014/09/26):

    * Fix to bug that caused a crash when using the wavelet module and all Gaussians in an island were flagged.

Version 1.8.2 (2014/05/14):

    * Island masks generated by the ``export_image`` task will now be expanded to match input image shape (as required by the AWimager).

    * Fix to bug that caused image read failure when image lacks a Stokes axis.

    * Fix to bug in CASA masks generated with ``export_image`` that caused cleaning to fail in CASA 4.2 and above.

    * Fix to bug that resulted in output file names being converted to lower case inappropriately.

Version 1.8.1 (2014/01/14):

    * Added option (``bbs_patches = 'mask'``) to allow patches in an output BBS sky model to be defined using a mask image (set with the ``bbs_patches_mask`` option).

    * Fix to bug that caused the ``incl_empty`` option to be ignored when ``format = 'fits'`` in the ``write_catalog`` task.

    * Enabled output of images in CASA format in the ``export_image`` task (``img_format = 'casa'``).

    * Added an option to ``export_image`` to export an island-mask image, with ones where there is emission and zeros elsewhere (``image_type = 'island_mask'``). Features in the island mask may be optionally dilated by specifying the number of dilation iterations with the ``mask_dilation`` parameter. The mask image may be padded with zeros to match the original image when the ``trim_box`` option was used to analyze only a portion of the image (``pad_image = True``).

    * Added an option to write a CASA region file to the ``write_catalog`` task (``format = 'casabox'``).

    * Added an option to write a CSV catalog to the ``write_catalog`` task (``format = 'csv'``).

    * Added error message when the rms is zero in some part of the rms map.

Version 1.8.0 (2013/10/16):

    * Improved wavelet fitting. Added option so that wavelet fitting can be done to the sum of images on the remaining wavelet scales, improving the signal for fitting (controlled with the ``atrous_sum`` option). Added option so that user can choose whether to include new islands found only in the wavelet images in the final fit or not (controlled with the ``atrous_orig_isl`` option).

    * Fixed a bug that could lead to incomplete fitting of some islands.

    * Improved overall convergence of fits.

Version 1.7.7 (2013/10/10):

    * Improved fitting of bright sources under certain circumstances.

Version 1.7.6 (2013/09/27):

    * Changed caching behavior to ensure that temporary files are always deleted after they are no longer needed or on exit.

    * Renamed ``blank_zeros`` to ``blank_limit``. The ``blank_limit`` option now specifies a limit below which pixels are blanked.

    * Enabled SAGECAL sky-model output.

Version 1.7.5 (2013/09/02):

    * Fix to bug that caused a crash when images with 2 or 3 axes were used.

    * Improved rms and mean calculation (following the implementation used in PySE, see http://dare.uva.nl/document/174052 for details). The threshold used to determine the clipped rms and mean values is now determined internally by default (i.e., ``kappa_clip = None``).

Version 1.7.4 (2013/08/29):

    * Fix to bug in ``show_fit`` that caused error when ``i`` is pressed in the plot window and shapelet decomposition had not been done.

    * Tweak to ``pybdsm`` startup shell script to avoid problems with the Mac OS X matplotlib backend on non-framework Python installations (such as Anaconda Python).

    * Fix to bug in ``process_image`` that could result in wavelet Gaussians being excluded from model image under certain conditions.

Version 1.7.3 (2013/08/27):

    * Fix to bug in image reading that caused images to be distorted.

Version 1.7.2 (2013/08/23):

    * Improved handling of non-standard FITS CUNIT keywords.

    * Improved loading of FITS images when ``trim_box`` is specified.

Version 1.7.1 (2013/08/22):

    * Fix to bug that caused cached images to be deleted when rerunning an analysis.

    * Fix to bug in ``show_fit`` due to undefined images.

    * Fix to bug in ``process_image`` (and ``img.process()``) that would result in unneeded reprocessing.

Version 1.7.0 (2013/08/20):

    * PyBDSM will now use Astropy if installed for FITS and WCS modules.

    * Fix to avoid excessive memory usage in the wavelet module (replaced ``scipy.signal.fftconvolve`` with a custom function).

    * Added option to use disk caching for internally derived images (``do_cache``). Caching can reduce memory usage and is therefore useful when processing large images.

    * Implemented a variable operation chain for process_image (and ``img.process()``) that allows unneeded steps to be skipped if the image is being reprocessed.

    * Fixed a bug that could cause Gaussian fitting to hang during iterative fitting of large islands.

    * Added option (``fix_to_beam``) to fix the size and position angle of Gaussians to the restoring beam during fitting.

    * Fix to bug that caused the position angle used to initialize fitting to be incorrect.

Version 1.6.1 (2013/03/22):

    * Fix to bug in ds9 and kvis catalog files that resulted in incorrect position angles.

    * Fix to bug in position-dependent WCS transformations that caused incorrect source parameters in output catalogs.

    * Added option to output uncorrected source parameters to a BBS sky model file (``correct_proj``).

    * Removed sky transformations for flagged Gaussians, as these could sometimes give math domain errors.

    * Disabled aperture flux measurement on wavelet images as it is not used/needed.

Version 1.6.0 (2013/03/05):

    * Improved speed and accuracy of aperture flux calculation.

    * Added option to use the curvature map method of Hancock et al. (2012) for the initial estimation of Gaussian parameters (``ini_method = 'curvature'``) and for grouping of Gaussians into sources (``group_method = 'curvature'``).

    * Fix to bug in spectral index module that caused sources with multiple Gaussians to be skipped. Minor adjustments to the wavelet module to improve performance.

    * Implemented position-dependent WCS transformations.

    * Added option to fit to any arbitrary location in the image within a given radius (``src_ra_dec`` and ``src_radius_pix``).

    * Fix to bug in wavelet module that caused crash when no Gaussians were fit to the main image.

    * Fix to bug that resulted in incorrect numbering of wavelet Gaussians. Added ``'srl'`` output in ds9 format when using ``output_all = True``.

    * Fix to bug in source grouping algorithm. Improved fitting when background mean is nonzero. Fix to allow images with GLAT and GLON WCS coordinates. Fix to bug when equinox is taken from the epoch keyword.


Version 1.5.1 (2012/12/19):

    * Fix to bug in wavelet module that occurred when the center of the wavelet Gaussian lies outside of the image.

    * Fix to re-enable srl output catalogs in ds9 region format.

    * Fix to bug that resulted in the output directory not always being created.

    * Added an option (``aperture_posn``), used when aperture fluxes are desired, to specify whether to center the aperture on the source centroid or the source peak.

    * Changes to reduce memory usage, particularly in the wavelet module.

    * Fix to bypass bug in matplotlib when display variable is not set.

    * Fixed bug that caused a crash when a detection image was used.

    * Fixed a bug with incorrect save directory when "plot_allgaus" is True.

Version 1.5.0 (2012/10/29):

    * Improved WCS handling. PyBDSM can now read images with a much greater variety of WCS systems (e.g., the ``VOPT`` spectral system).

    * Fixed a bug related to the use of a detection image when a subimage is specified (with ``trim_box``).

Version 1.4.5 (2012/10/12):

    * Added option (``incl_empty``) to include empty islands (that have no un-flagged Gaussians) in output catalogs. Any such empty islands are given negative source IDs and have positions given by the location of the peak of the island.

    * Fixed a bug in Gaussian fitting that could cause a crash when fitting fails.

    * Fixed a bug in parallelization that could cause a crash due to improper concatenation of result lists.

Version 1.4.4 (2012/10/09):

    * Fixed a bug related to the parallelization of Gaussian fitting that could cause a crash due to improper mapping of island lists to processes.

    * Improved logging.

    * Added a warning when one or more islands are not fit (i.e., no valid, unflagged Gaussians were found).

    * Added code to handle images with no unblanked pixels.

    * Improved fitting robustness.

Version 1.4.3 (2012/10/04):

    * Fixed a bug in the mean map calculation that caused mean maps with constant values (i.e., non-2D maps) to have values of 0.0 Jy/beam unless ``mean_map = 'const'`` was explicitly specified.

    * Fixed a bug in the PSF vary module that resulted in incorrect PSF generators being used. Added an option to smooth the resulting PSF images (``psf_smooth``). Parallelized the PSF interpolation and smoothing steps. Improved PSF vary documentation.

Version 1.4.2 (2012/09/25):

    * Dramatically reduced time required to identify valid wavelet islands. Fixed bug that resulted in output FITS gaul tables being improperly sorted.

Version 1.4.1 (2012/09/11):

    * Added SAMP (Simple Application Messaging Protocol) support to the write_catalog, export_image, and show_fit tasks. These tasks can now use SAMP to communicate with other programs connected to a SAMP hub (e.g., ds9, Topcat, Aladin).

Version 1.4.0 (2012/09/11):

    * Parallelized Gaussian fitting, shapelet decomposition, validation of wavelet islands, and mean/rms map generation. The number of cores to be used can be specified with the ``ncores`` option (default is to use all).

Version 1.3.2 (2012/08/22):

    * Fixed a bug that could cause the user-specified ``rms_box`` value to be ignored. Added an option to enable the Monte Carlo error estimation for 'M'-type sources (the ``do_mc_errors`` option), which is now disabled by default.

Version 1.3.1 (2012/07/11):

    * Fixed a bug that caused images written when ``output_all = True`` to be transposed. Added frequency information to all output images. Improved fitting robustness to prevent rare cases in which no valid Gaussians could be fit to an island. Modified the island-finding routine to handle NaNs properly.

Version 1.3.0 (2012/07/03):

    * Fixed a bug in the calculation of positional errors for Gaussians.

    * Adjusted ``rms_box`` algorithm to check for negative rms values (due to interpolation with cubic spline). If negative values are found, either the box size is increased or the interpolation is done with ``order=1`` (bilinear) instead.

    * Output now includes the residual image produced using only wavelet Gaussians (if any) when ``atrous_do=True`` and ``output_all=True``.

    * Improved organization of files when ``output_all=True``.

    * Added logging of simple statistics (mean, std. dev, skew, and kurtosis) of the residual images.

    * Included image rotation (if any) in beam definition. Rotation angle can vary across the image (defined by image WCS).

    * Added Sagecal output format for Gaussian catalogs.

    * Added check for newer versions of the PyBDSM software ``tar.gz`` file available on ftp.strw.leidenuniv.nl.

    * Added total island flux (from sum of pixels) to ``gaul`` and ``srl`` catalogs.

Version 1.2 (2012/06/06):

    * Added option to output flux densities for every channel found by the spectral index module.

    * Added option to spectral index module to allow use of flux densities that do not meet the desired SNR.

    * Implemented an adaptive scaling scheme for the ``rms_box`` parameter that shrinks the box size near bright sources and expands it far from them (enabled with the ``adaptive_rms_box`` option when ``rms_box`` is None). This scheme generally results in improved rms and mean maps when both strong artifacts and extended sources are present.

    * Improved speed of Gaussian fitting to wavelet images.

    * Added option to calculate fluxes within a specified aperture radius in pixels (set with the ``aperture`` option). Aperture fluxes, if measured, are output in the ``srl`` format catalogs.

Version 1.1 (2012/03/28):

    * Tweaked settings that affect fitting of Gaussians to improve fitting in general.

    * Modified calculation of the ``rms_box`` parameter (when the ``rms_box`` option is None) to work better with fields composed mainly of point sources when strong artifacts are present.

    * Modified fitting of large islands to adopt an iterative fitting scheme that limits the number of Gaussians fit simultaneously per iteration to 10. This change speeds up fitting of large islands considerably.

    * Added the option to use a "detection" image for island detection (the ``detection_image`` option); source properties are still measured from the main input image. This option is particularly useful with images made with LOFAR's AWImager, as the uncorrected, flat-noise image (the ``*.restored`` image) is better for source detection than the corrected image (the ``*.restored.corr`` image).

    * Modified the polarization module so that sources that appear only in Stokes Q or U (and hence not in Stokes I) are now identified. This identification is done using the polarized intensity (PI) image.

    * Improved the plotting speed (by a factor of many) in ``show_fit`` when there are a large number of islands present.

    * Simplified the spectral index module to make it more user friendly and stable.

    * Altered reading of images to correctly handle 4D cubes.

    * Extended the ``psf_vary`` module to include fitting of stacked PSFs with Gaussians, interpolation of the resulting parameters across the image, and correction of the deconvolved source sizes using the interpolated PSFs.

    * Added residual rms and mean values to source catalogs. These values can be compared to background rms and mean values as a quick check of fit quality.

    * Added output of shapelet parameters as FITS tables.

    * Fixed many minor bugs.

See the changelog (accessible from the interactive shell using ``help changelog``) for details of all changes since the last version.
