**

# NaturalHeritage Taxon checker

The aim of this tool is to complete and annotate tab-delimited files with taxonomic information (scientific names) against several web services

 1. GBIF
 2. GBIF (vernacular names)
 3. WoRMS
 4. IUCN
 5. Fishbase
 6. DaRWIN (RBINS-RMCA database)

Resulting data are the original file with extra fields verifying the author, taxonomic hierarchy, synonymy relationships.
GBIF API is able to detect possible misspellings. The data are also annotated with a color code

**Technical requirements**

 1. PHP (7.4)
 2. Apache
 3. PostgreSQL (replacement with MySQL/MariaDB should be easy via PDO)
 4. gnparser (https://github.com/gnames/gnparser/blob/master/README.md) application in GO to parse scientific name (e.g separate binomial form from authors)
 
PHP libraries:
 1. php-pgsql (and/or PDO)
 2. php-curl
 3. php-soap (for WoRMS)

GNParser has to be installed as command line on the server locally (as command-line app, ot as a service):
https://github.com/gnames/gnparser/blob/master/README.md
