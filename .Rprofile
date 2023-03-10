
# Options -----------------------------------------------------------------

options(
  # If warn is one, warnings are printed as they occur
  warn = 1,
  # warn on partial matches
  warnPartialMatchAttr = TRUE,
  warnPartialMatchDollar = TRUE,
  useFancyQuotes = FALSE,
  usethis.full_name = "Adam Sadowski",
  # named list of default DESCRIPTION fields for new packages made
  # with usethis::create_package().
  usethis.description = list(
    "Authors@R" = utils::person(
      "Adam", "Sadowski",
      email = "asadowsk@uoguelph.ca",
      role = c("aut", "cre"),
      comment = c(ORCID = "JANE'S-ORCID-ID")
    ),
    Version = "0.0.0.9000"
  ),
  usethis.destdir = "C:/Users/asadowsk/OneDrive - University of Guelph/packages",
  usethis.overwrite = TRUE
)


# Non-Options -------------------------------------------------------------

## Auto-completion of package names in `require`, `library`
utils::rc.settings(ipck = TRUE)

## Prevent if(c(TRUE, FALSE)) TRUE
Sys.setenv("_R_CHECK_LENGTH_1_CONDITION_" = "true")

## For Devtools ----

if (interactive()) {
  suppressMessages(require(devtools))
}

## For Shiny Preview in Viewer Pane ----

if (
  # Make sure that {rstudioapi} is available
  requireNamespace("rstudioapi", quietly = TRUE) &&
  # Returns TRUE if RStudio is running
  rstudioapi::hasFun("viewer")
) {
  options(shiny.launch.browser = .rs.invokeShinyPaneViewer)
}
