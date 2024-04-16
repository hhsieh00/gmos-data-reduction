# gmos-data-reduction
Collection of Jupyter notebooks for reduction of Gemini GMOS data<br><br>

<tt>notebook_GMOS_a01_12amp_process_raw_twilight_flats.ipynb</tt>
- Performs initial data reduction (overscan correction, trimming, and bias subtraction) of raw twilight flatfield images downloaded from the Gemini archive<br><br>
- Requires raw twilight sky flat data and raw bias data downloaded from the Gemini archive

<tt>notebook_GMOS_a02_12amp_combine_twilight_flatfield_images.ipynb</tt>
- Performs median-combination of individual twilight flatfield images processed by <tt>notebook_GMOS_a01_12amp_process_raw_twilight_flats.ipynb</tt>
- Requires screening by user of output data files from <tt>notebook_GMOS_a01_12amp_process_raw_twilight_flats.ipynb</tt> to exclude data with insufficient or excessive mean counts<br><br>

<tt>notebook_GMOS_a03_12amp_process_science_data.ipynb</tt>
- Performs overscan correction, trimming, bias subtraction, flat-field correction, and cosmic ray removal on raw Gemini science data downloaded from the Gemini archive
- Uses raw bias data downloaded from the Gemini archive and processed flatfield files created by <tt>notebook_GMOS_a01_12amp_process_raw_twilight_flats.ipynb</tt> and <tt>notebook_GMOS_a02_12amp_combine_twilight_flatfield_images.ipynb</tt>.<br><br>

<tt>notebook_GMOS_a04_make_multiextension_files.ipynb</tt><br>
- Creates multi-extension FITS (MEF) files by combining individual extension files for bias, flatfield, and science images produced by <tt>notebook_GMOS_a01_12amp_process_raw_twilight_flats.ipynb</tt>, <tt>notebook_GMOS_a02_12amp_combine_twilight_flatfield_images.ipynb</tt>, and <tt>notebook_GMOS_a03_12amp_process_science_data.ipynb</tt> for a particular night of science observations.<br><br>
