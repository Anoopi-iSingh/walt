## Frequently Asked Questions ##

1. When does WALT get much lower mapping rate (mapping effiency) compared to other bisulfite mappers?
	By default, WALT ignores reads shorter than 39. If you get lower mapping rate, please go to mapstats file and check the percentage of reads that are shorter than 39. If a large portion of reads are shorter than 39, I suggest you use WALT seed pattern 7.
	(1)	Open walt/src/walt/Makefile, modify “-D SEEDPATTERN3" to " -D SEEDPATTERN7"
	(2)	rebuild the program using make all, make install
	(3)	rebuild your index using the new makedb command
	(4)	mapping reads using the new walt command
	
	

