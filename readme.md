GettingAndCleaningData
======================

This repository is the course project of the *Getting and Cleaning Data* Coursera course.


You have to run the [run_analysis.R][analysis]-file.
This subsequently loads the used data sets which are in
[getdata_projectfiles_UCI HAR Dataset.zip][zip] without extracting.

After running the code two tidy data sets (as described in the instructions) are saved:

1. [tidy_dataset1.txt][tidy1]: consists of a `10299x81` with `;`-seperation, `.`-decimals, header and no row.names
2. [tidy_dataset2.txt][tidy2]: consists of a `180x81` with `;`-seperation, `.`-decimals, header and no row.names

You can load the data via the codes:
```
tidy1 <- read.table("tidy_dataset1.txt", sep=";", dec=".", header=TRUE)
tidy2 <- read.table("tidy_dataset2.txt", sep=";", dec=".", header=TRUE)
```

[CodeBook.md][code] describes what is done in [run_analysis.R][analysis].


have fun!


[analysis]: https://github.com/Schlusie/GettingAndCleaningData/blob/master/run_analysis.R
[zip]: https://github.com/Schlusie/GettingAndCleaningData/blob/master/getdata_projectfiles_UCI%20HAR%20Dataset.zip
[tidy1]: https://github.com/Schlusie/GettingAndCleaningData/blob/master/tidy_dataset1.txt
[tidy2]: https://github.com/Schlusie/GettingAndCleaningData/blob/master/tidy_dataset2.txt
[code]: https://github.com/Schlusie/GettingAndCleaningData/blob/master/CodeBook.md
