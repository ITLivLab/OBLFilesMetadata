# OBLFilesMetadata
This repo contains metadata that was extracted from OBL Files that the CIA released. The files can be found here: https://www.cia.gov/library/abbottabad-compound/index.html and https://archive.org/details/AbbottabadCompoundMaterials

# Why?
Data was extracted because curiosity...
Also I wanted to dump the data into ElasticSearch and see if there is anything interesting.

# How?
Apache Tika was utilized to extract the metadata. https://tika.apache.org/1.16/gettingstarted.html
Apache Tika can be ran in server mode or you can also use command line app as well. I used the following command: `java -jar tika-app-1.16.jar -j $filename > $filename.MYJSON`
There were some failures while doing this. Tika couldn't extract metadata from some of the files and for some other files, I had to kill the tika process.