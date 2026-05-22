###  Checks both flat filed and wavelength calibrations
#### - All output files (pdf's) have the date as identifier; if you have multiple plots for one day, just add a counter. I am working on that, but for now, it would overwrite the pdf file
#### - The first part of the script would look through a list of files and select either flat- fields, biases, or any type of calibrations and write them in a file
#### - for flat field calibrations, a list with 12 flat field images is plotted, with a line across specific coordinates ( y_coo= 2043, xstart=905) to check if the flat field flux is OK, it indicates the exposure times and the file name
#### - For wavelength calibrations:
  *  4 files are plotted,  using 3 different lines for comparison, one in the blue range, one central and one from the red end. A line is put over both object fibre (left) and sky fibre (right), and the counts for all 4 data sets are plotted
  *  The lies may shift slightly, to see the maximum flux, check the exact position
  *  I will change it to the sum of the three maximum pixel values in the future

#### The last blocks are for testing things!!!
+ **$${\color{red}22.05.2026:}$$**
    * corrected an error in the first 2 rows, I used more than just one row of pixels, now only 1 pixel is used for all 4 dates.
    * the sum of the three maximum pixel values is not done yet.
