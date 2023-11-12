# For debug

[image.sc forum issue](https://forum.image.sc/t/failing-to-parse-hcs-image-set-using-namesandtypes-module/88622)

NamesAndTypes module failing for HCS project

*	Example workflow: [toyset_metadata.cppipe](toyset_metadata.cppipe)
	-	toyset: [data](data/)
*	group_by simulation in R: [parse_hcs.qmd](parse_hcs.qmd)
	-	expected output: [grouped_metadata.csv](grouped_metadata.csv)

We have data from high-content screen where we image each well on multiple 384-well plate as follows:

9 fields per well, each field has four z-stacks, each stack has two channels. Images were taken for 384-well plates, each at two time points (Measurement 1 and 2).

In a similar HCS project, I was able to successfully parse raw images using CellProfiler metadata and NamesAndTypes modules but for the current project, somehow I am unable to resolve duplicates in NamesAndTypes module. I tried several variants in “Match metadata” option but either I get image set matching error or no image set for a given matched metadata.

However, I am able to parse these images and find no duplicates if I do created grouped metadata table using pivot like function in R. I am trying to debug error on my end in cellprofiler pipeline given similar setup worked for other cellprofiler project.

Thanks,
Samir & Kentaro

