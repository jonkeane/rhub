## Test environments


## R CMD check results


## Release summary

### New features

* New `local_check_linux()` function to run an R-hub check on the local
  host's Docker. New `local_check_linux_images()` function to list R-hub
  Docker images.

* New `check_on_solaris()` shortcut to check on Solaris X86, without
  building the PDF manual or the vignettes.

* New `get_check()` function that works with check ids, or a check group id.

* `list_package_checks()` and `list_my_checks()` now output a `tibble`, that is nicely formatted when printed to the screen.

* The output of `get_check()`, `check()`, `check_on_`, `check_for_cran()`,
  etc. functions gained
    * an `urls()` method returning a `data.frame` with URLs to the html and
    text logs, as well as the artifacts, of the check(s);
    * a `browse()` method replacing the `web()` method for opening the
  URLs corresponding to a `rhub_check` object.

* New `cran_summary()` method to print a summary for a group or set of
  checks.

### Bug fixes

* In printing methods the submitted time is now always correct thanks to
  explicitly specifying units for `as.numeric.difftime` (@jimhester, #94
  and @schloerke, #135).
