**The data**
The data contains 24 short stories (.txt) from the Gutenberg Project in 6 languages: Italian, Finnish, English, Hungarian, French, and German. There are 4 stories in each language. One data file is one short story. 

This dataset was created to explore differences in short stories in different languages and from different cultures in Europe. This dataset can help explore questions for example about differences in language, but also differences across decades. It could also potentially be expanded to include for example gender comparisons or stories from outside of Europe. 

Selection criteria:
The stories had to be written in one of the 6 chosen languages to be able to make a comparison between stories written in Europe. The were chosen based on their popularity (likes, favorites) on the Internet Archive, as more popular stories likely represented the most popular writing style(s). As a result, what is missing are less popular stories that perhaps could introduce more diversity in the dataset. On top of that, I did not specifically look for stories written by women or to create a dataset that was balanced for gender. Further, sticking to a minimum of 4 stories per language means I had to exclude other languages, which again leads to a less diverse dataset.  

Data collection:
The data was collected and downloaded from the Internet Archive via their Project Gutenberg section on their webpage. The data was collected on 2026-11-16.

Preprocessing:
The data was processed to have a year of earliest possible publication and a year of latest possible publication. For stories that only contained one year, these years are the same. No further cleaning of the data was done to allow the data to be manipulated by anyone who wishes to use it in their own independent way. 

**Structure**
The folder contains the data (.txt files) for each short story, a README.md with information about the dataset, a requirements.txt with information about the required programmes and packacges, metadata.csv which contains metadata about each short story, a python notebook 'check_dataset.ipynb' to check the contents and quality of the metadata, a python notebook 'prepare_dataset.ipynb' with the preprocessing code, and finally a .gitignore. 

The codebook for the metadata.csv:

**Variable, Description, Type, Allowed values / missing value**
id, unique id for each story, string, 'gut_'+ 5 digits; cannot be empty
file, the relative path for each story, string, 'data/gut_' + 5 digits +'.txt'; cannot be empty
title, the title of the story, string, 1+ words including special characters; empty if unknown
author, the name of the author of the story as given on Project Gutenberg, string, 1+ words including special characters, Anonymous; empty if unknown
language, the language of the story, categorical, ISO 639-1 two-letter codes, e.g., en, it, de; empty if unknown
year_earliest, year of first publication, integer, 1700–1950; empty if unknown
year_latest, year of latest publication, integer, 1700–1950; empty if unknown
source, source of short story, string, 'https://www.gutenberg.org/ebooks/' + 5 digits; empty if unknown
licence, the license of the short story, string, licence codes and descriptions, e.g., CC0, Public domain; empty if unknown

**Uses and Limitations**

The dataset can be used explore questions about differences in short stories and language use across languages within Europe. The data covers a time period between roughly the 1850s and the 1920s. The limitations are that this dataset does not record information about the gender of the authors which means the dataset currently is not suitable for any research into gender differences. Furthermore, choosing more popular stories means that there is potentially a lack of diversity in the types of authors included and in the language used. 6 languages are included (Italian, Finnish, English, Hungarian, French, German), which means that a lot of languages within Europe are left out and thus the comparison is limited. 

**License**

The short stories are placed in the public domain using a CC0 License in the USA. Project Gutenberg is trademarked for commercial use, meaning the data can be freely used and distributed as long as this is not for commercial purposes. The data does not contain personal information. It is possible to distribute and share the data under the public domain status as long as is being complied by the Project Gutenberg license or this licence is removed. 


This dataset is shared under a CC0 licence. Attribution is not required. A citation suggestion is "Project Gutenberg Short Stories" (2026) by spinnetje8. 






