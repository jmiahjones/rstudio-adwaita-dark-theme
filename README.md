
# RStudio Adwaita Dark Theme <!-- <img src="figures/logo.png" align="right" width="120" /> -->

<!-- badges: start -->

<!-- badges: end -->

## Overview

Custom editor themes for Rstudio + a script to Adwaita-fy any rstheme file.

## Installation

To install the custom stylesheet for rstudio, run the INSTALL script to move the `qss/rstudio-gnome-dark.qss` file to `/usr/lib/rstudio/resources/stylesheets/`, or simply complete
this yourself.

To install the custom editor themes, go in RStudio Global Options \>
Appearance and click on <kbd>Add…</kbd> and add any of the themes in `rsthemes/`.

Alternatively, run the snippet in the RStudio console to install and
apply e.g. Adwaita Darkula:

``` r
rstudioapi::addTheme("https://raw.githubusercontent.com/jmiahjones/rstudio-adwaita-dark-theme/master/rsthemes/AdwaitaDarkula.rstheme", apply=TRUE, force=TRUE)
```

The previous work was all done by aldomann. By that example, I have created a script to *Darkify* any theme according to Adwaita. Run the
Darkify script by using
``` bash
Darkify /usr/lib/rstudio/resources/themes/monokai.rstheme ~/adwaita-monokai.rstheme
```

Then, go to the newly created adwaita-monokai theme and:
1. Change the name of the theme to ensure it is set apart from the default theme: e.g.
    ``` bash
    /* rs-theme-name: Adwaita Monokai */
    ```

2. Switch the dark theme flag to enable the stylesheet.
    ``` bash
    /* rs-theme-is-dark: TRUE */
    ```

Now point RStudio to the theme as described above!
