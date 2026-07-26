# Global Economy Redesign

This project uses `renv` to record and restore the R packages required to
render `gdp_redesign.qmd`.

## Requirements

- R 4.6.x
- Quarto
- Internet access during the initial package restoration

## Restore the R environment

Extract or clone the complete project into a local folder. Open R in the
project root (the folder containing `renv.lock`) and run:

```r
install.packages("renv")
renv::restore()
```

When prompted, confirm that the packages should be installed. `renv` will
recreate the package versions recorded in `renv.lock`. This initial restoration
may take several minutes.

## Render the report

After `renv::restore()` completes, render from a terminal in the project root:

```bash
quarto render gdp_redesign.qmd
```

Alternatively, open `gdp_redesign.qmd` in RStudio and select **Render**.

The rendered dashboard is written to `gdp_redesign.html`, and the combined
figure is written to `gdp_redesign.png`.

## Troubleshooting

Check whether the restored environment matches the lockfile:

```r
renv::status()
```

If package restoration fails, verify that R 4.6.x and Quarto are installed and
that R can access `https://cloud.r-project.org`.
