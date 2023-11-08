### authorlistR

# Renumber and Sort Affiliations in Author Lists

<!-- badges: start -->

<!-- badges: end -->

You prepare a manuscript with many co-authors, but as so often have then change the order of authors, add or remove affiliations... spending a lot of time and making errors to manually edit the author affiliation numbers... again and again!

Solution: currently just a simple script, but copy/paste your author and affialiation lists to the text files in this project, run the R code, and copy/paste back the formatted, renumbered and reorderd author and affiliation lists to your manuscript!

### Prerequisites

Following CRAN packages must be installed in your system

``` r
install.packages(c("tidyverse", "here", "r2rtf"))
```

### Usage

1)   Copy/paste to `author_names.txt` the list of author names in the desired order, succeeded with affiliations numbers. Authors should be separated by comma followed by a `space` or by a `;`. Multiple affiliations must be separated by `,`.

    ```         
    Clark1,2, H. Adams3, C. Baker8, E. Davis4,11, T. Evans5, O. Frank6, Y. Ghosh10,K. Hills11, 
    A. Irwin9, J. Jones7, K. Klein1,12
    ```

2)   Copy/paste to `author_affiliations.txt` the list of affiliations, preceded with the number that is used in the authorvlist (see 1) to associate the authors with corresponding affiliations. Each affiliations needs to be on a separated line.

    ```         
    1Starlight University
    2Quantum Institute of Technology
    3Horizon University
    ```

3) Run through the chunks of the notebook `authorlistR.qmd` in the folder `R`

4) Formatted output (.rtf files) of the updated author and affiliation lists can be found in the folder `output`, which can be opened in Word and other text editors. Examples:

> C.C. Clark<sup>1,2</sup>, H. Adams <sup>3</sup>, E. Davis<sup>4,5</sup>, BB. Baker<sup>1,5,6</sup>, Y. Ghosh<sup>7,8</sup>, T Evans<sup>9</sup>, F. Frank<sup>10</sup>, K. Hills<sup>5</sup>, A. Irwin<sup>2</sup>, J. Jones<sup>11</sup>, K. Klein<sup>1,3,6,12</sup>

> <sup>1</sup>Starlight University
>
> <sup>2</sup>Quantum Institute of Technology
>
> <sup>3</sup>Horizon University

## Contact

Bo Burla, Singapore Lipidomics Incubator, National University of Singapore (lsibjb \@ nus.edu.sg)

## Notes

This code does not check the data you provide and may crash or output wrong data if formatting is not as expected. The author of this script will not accept any responsibility for rejected manuscripts:)

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
