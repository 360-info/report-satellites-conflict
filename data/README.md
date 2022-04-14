# Data files in this analysis

## Downloaded files

UCS data is automatically downloaded by the analysis and is stored in `/data/.cache`.

## Files derived from `index.qmd`

[This analysis](../index.qmd) tidies [UIS student flow data](http://data.uis.unesco.org) and [OWID/UNDP human development data](https://ourworldindata.org/human-development-index) into several forms:

* [`sat-user-overlap-data.csv`](sat-user-overlap-data.csv): a data frame of the total number of satellites with a given owner-operator country and given user sector - one of "Civil", "Commercial", "Government" or "Military". Many satellites belong to more than one group, however, and such satellites are marked in the form "GroupA/GroupB". Figures for single-group sets are inclusive of the overlaps (eg. the figure for "Commercial" also includes the figure for "Commercial + Military"). Columns are:
  - `country_owner`: The country of the owner-operator organization
  - `sets`: The user group(s)
  - `size`: The number of satellites for this country and user group(s)
  - `overlapped`: TRUE if this category is a complete subset of another (eg. if all Civil satellites for this country also belong to another user group). Used to control labelling in the venn diagram.
