
<!-- NEWS.md is generated from NEWS.Rmd. Please edit that file -->

## FielDHub 1.2.0

### Shiny App

-   Added a `help` menu option in the app that connect you directly to
    the documentation available in our GitHub repository.

-   Added **vignettes and help documentation** for all standard
    functions and modules available for all designs in the app.

-   Added capability for making multiple randomizations across different
    **locations** to the unreplicated, partially replicated, lattice,
    RCBD, factorial, split-plot, split-split-plot, strip-plot, IBD, and
    RCD designs.

-   Added capability to produce **heatmap visualizations** of simulated
    data for all experimental designs.

-   Added action buttons to **copy and save field maps and field book
    outputs to Excel.**

-   Added **factorization options that aid users in the creation of
    randomizations and mapping layouts** for the unreplicated and
    partially replicated designs. Previous version required users to do
    the \* mathematical calculation a priori.

-   Added **filters and search** boxes for the field book tables.

-   Updated UI/UX design for home page.

-   Grouped single diagonal arrangement, multiple diagonal arrangement,
    optimized arrangement and augmented RCB designs under one single
    module.

-   Added action run button to all experimental designs to prevent
    reactivity issues with the application.

-   Improved and standardized user experience features and readability
    access.

-   Improved error logging messages. Added features to inform end-users
    on the utilization of correct input data file formats and associated
    metadata/columns, checking for duplicate values in input files, as
    well as data type verification.

-   Added the plot() method to the FielDHub package to display the field
    layout of the field book for all designs.

-   Added **additional field layout visualization/map options** to all
    experimental designs. Previous version only had mapping options for
    unreplicated and p-rep designs.

-   Added a drop-down menu to display a **multiple layout mapping option
    shown by entry number and by plot** for all experimental designs.
    This means, that now you can visualize each randomization layout
    option for each of the locations you input.

-   Added an option for repeating whole entries/experiments in the
    unreplicated diagonal arrangement design with multiple experiments
    (previously called decision blocks).

-   Added a check box feature in the Augmented RCB design to allow for
    the creation of nurseries with the option of randomizing
    experimental entries or not. If user decides to leave this option
    unchecked, only the checks will be randomized, and the experimental
    entries will be shown in consecutive order.

-   Added a check box option to the RCB design to allow for a continuous
    plot numbering independently of the rep or block number. Previous
    version coded the replication into the plot number (i.e., 101 =rep1,
    201=rep2, etc.).

-   Fixed a restriction in the RCBD mapping layout to allow for the use
    of more than 25 entries. PS: There are better designs when the
    number of entries is higher than 25 (for more info go to: [FIELD
    PLOT DESIGN I](https://www.ndsu.edu/faculty/horsley/)).

### Standalone Functions in `FielDHub` Package

-   `partially_replicated()` now generates randomization across multiple
    locations/sites.

-   `diagonal_arrangement()` now generates randomization across multiple
    locations/sites.

-   `optimized_arrangement()` now generates randomization across
    multiple locations/sites.

-   `partially_replicated()` now allows that all entries/treatments have
    replicates. Before, it required at least some unreplicated entries.

-   Functions `optimized_arrangement()`, `diagonal_arrangement()` and
    `partially_replicated()` now return feedback if the input dimensions
    `nrows` and `ncols` are incorrect.

-   `RCBD()` now includes an argument (`continuous`) to manage the way
    it sets up the plotting number.

-   `RCBD_augmented()` now allows customization of the field dimensions
    by inputting the number of rows and columns through `nrows` and
    `ncols` arguments.

-   `RCBD_augmented()` now returns feedback if the input dimensions
    `nrows` and `ncols` do not match the data entered.

-   `RCBD_augmented()` when `random = FALSE` now allows only randomizing
    the checks/controls if the user wants.

-   Fixed a bug in `full_factorial()` for the CRD factorial design that
    prevented the option of including all possible factorial
    combinations.

-   Added a method `print()` of class `fieldLayout`. See
    [print()](https://didiermurillof.github.io/FielDHub/reference/print.fieldLayout.html).

-   Added a method `plot()` of class `FieldHub` that returns an object
    of class `fieldLayout`. See
    [plot()](https://didiermurillof.github.io/FielDHub/reference/plot.FielDHub.html).
    The method `plot()` can plot a field layout for any of the designs
    output. It is possible to pass arguments such as the location,
    layout order and others. For more detail see [plot(), print() and
    summary() methods in
    FielDHub](https://didiermurillof.github.io/FielDHub/articles/methods.html).

-   Fixed a bug in `diagonal_arrangement()` when `kindExpt = DBUDC`. The
    problem affected the random distribution of the checks for the case
    of unbalanced control plot numbers for each experiment.

-   Fixed a bug in `diagonal_arrangement()` when `kindExpt = DBUDC`. The
    problem affected merging data between the user data and
    randomization data when users wanted replicated entries across
    experiments.

## FielDHub 0.1.0

CRAN release.
