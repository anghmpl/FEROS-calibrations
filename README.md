###  Checks both flat-field and wavelength calibrations
#### - All output files (pdf's) have the date as an identifier; if you have multiple plots for one day, just add a counter. I am working on that, but for now, it would overwrite the pdf file
#### - The first part of the script would look through a list of files and select either flat-field, biases, or any type of calibrations and write them in a file
#### - For flat-field calibrations, a list with 12 flat-field images is plotted, with a line across specific coordinates ( y_coo= 2043, xstart=905) to check if the flat-field flux is OK, it indicates the exposure times and the file name
#### - For wavelength calibrations:
  *  4 files are plotted,  using 3 different lines for comparison, one in the blue range, one central and one from the red end. A line is put over both object fibre (left) and sky fibre (right), and the counts for all 4 data sets are plotted
  *  The lines may shift slightly; to see the maximum flux, check the exact position
  *  I will change it to the sum of the three maximum pixel values in the future

#### The last blocks are for testing things!!!
+ **$${\color{red}22.05.2026:}$$**
    * Corrected an error in the first 2 rows. I used more than just one row of pixels; now only 1 pixel is used for all 4 dates.
    * The sum of the three maximum pixel values is not done yet.


+ **$${\color{red}08.09.2026:}$$**
    * FF\_input.lst and WAVE\_select.lst are examples of the input files. The first one needs 12 images; the second one needs 4 images.
    * For wavelength calibrations, 4 lines are selected. Along a specified line, the flux values for 5 pixels [line-2:line+3] are obtained, and the 2 highest values are averaged. So, even if the line is not on the highest value, the 2 pixels with the highest flux are still selected.


<img width="4607" height="5589" alt="FEROS_calibs" src="https://github.com/user-attachments/assets/4b15144b-6412-4f8b-84a5-f15265fa1455" width="50%"/>

