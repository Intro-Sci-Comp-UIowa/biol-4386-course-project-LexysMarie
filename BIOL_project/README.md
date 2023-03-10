**NMNAT2 Abundance is Positively Correlated to the Level of Syanptic Protein**

1) Ali YO, Allen HM, Yu L, et al., NMNAT2:HSP90 complex mediates proteostasis in proteinopathies. *PLOS Biology*. June 2 2016; doi:0.1371/journal.pbio.1002472

**Introduction**
	Nicotinamide mononucleotide adenylyl transferase (NMNATs) are important for neuronal maintenance of *Drosophila* and humans. Overexpression of these proteins provides neuroprotection in many neurodegenerative models, especially in Wallerian degeneration. NMNATs are also known as nicotinamide adenine dinucleotide (NAD)-synthesizing enzymes. They enable proper flux of NAD, which is an important cofactor in many cellular processes. When inducing Wallerian degeneration, NAD levels are reduced while exogenous NAD application offers neuronal protection. However, if NMNAT enzymatic function is impaired in some way, neuronal protection is reduced. Recently, it's been discovered in *Drosophila* photoreceptor models that NMNAT enzymatic activity is not required to maintain neuronal integreity in these photoreceptors. This data suggests that NMNATs might be able to protect neurons by different mechanisms.
	NMNAT2 is an example of a NMNAT enzyme. Constant supply of NMNAT2 from Golgi-derived vesicles is important in maintaining axonal health. When NMNAT2 is absent, neurite outgrowth deficits or axonal degeneration can occur. NMNAT2 is highly expressed in the mammalian brain. Reduction of *nmnat2* mRNA levels have been observed in individuals with Parkinson, Huntington, and Alzheimer's disease (AD). This and other recent data suggest that NMNAT2 is important for neuronal maintenance. However, the mechanism underlying this maintenance remains unknown.
	In *Drosophila*, *Drosophila* NMNAT (*d*NMNAT) acts as a molecular chaperone. Molecular chaperones are a class of proteins that either interact with, stabilize, or assist proteins in maintaining protein homeostasis (proteostasis) and facilitating the clearance of pathological protein aggregates. Recent data has shown that chaperones are important in maintaining neuronal function.
	Proteinopathies, like AD and tauopathies, are characterized by stereotypic aggregated proteins. This pathology can also be associated with cognitive impairment. It has been hypothesized that enhancing chaperone activity can help to establish a cytoprotetective state. Cytoprotective states occur when cellular damage, caused by misfolding or aggregation associated proteinopathies, is protected against in the body. In AD, the role of chaperones has been studied in depth, especially in regard to tau aggregation and fibrillization. It has been observed that chaperones like HSP70 and HSP90 preferentially bind to hyperphosphorlyated human Tau (p-hTau) and paired helical filamentous tau. Overexpression of these two chaperones inhibit the early stages of amyloid aggregation in AD. This paper aimed to answer three questions: Does NMNAT2 act as a chaperone? Is chaperone activity required for NMNAT2 to reduce tauopathy and protect neurons against protein stress? And how does NMNAT2 exert its chaperone function? To answer these questions, this study examined the relationship between *nmnat2* mRNA levels and the cognitive capabilities and AD pathology of a large cohort of human subjects.
	In the figure that I'm recreating (figure 7D; see below), it was determined beforehand that synapses are usually the first structures lost in neurodegenerative disease. In fact, NMNAT2 has been detected in synaptic membranes and vesicles of cortical neurons. This data suggests that NMNAT2 plays a role in synaptic maintenance. To test this theory, presynaptic proteins (VGluT1, SNAP25, RIM1alpha, and SYPH) in both wild-type mice and mice without NMNAT2 were compared. Additionally, levels of the chaperone HSP90 and N-methyl-D-aspartate receptor 1 (NR1) in wild-type and NMNAT2 knockout mice were also compared. It was determined that presynaptic protein levels are positively correlated with NMNAT2 levels. However, there was no significant correlation between HSP90 and NR1 and NMNAT2. This data indicates that NMNAT2 plays a significant role in synaptic maintenance.
![Figure 7](Screen Shot 2023-02-14 at 3.56.00 PM.png)
Fig 7. NMNAT2 abundance is positively correlated to the levels of synaptic proteins. (A-B) Levels of synaptic proteins analyzed by western blotting in DIV10 WT, HET, and KO cortical neurons. n = 3 independent experiments for each genotypes. (C-D) Western analysis for the abundnce of synaptic proteins in the hippocampi of 8-mo-old NMNAT2 HET and WT (n = 6 per genotype). The regression lines show the relationships between NMNAT2 and SNAP25, SYPH, VGluT1, RIM1alpha, HSP90, NR1. Protein levels were normalized to GAPDH. Individual values for 7B and 7D are provided in S1 Data.

**Materials and Methods**
1) How was the experiment performed to produce the data?
	a. A Western blot analysis was performed. The data is based off that analysis. The figure that I want to reproduce (figure 7D) is a line graph that shows regression lines presenting the correlation between NMNAT2 and SNAP25, SYPH, RIM1alpha, HSP90, and NR1. Protein levels were normalized to GAPDH
2) Where and how will you obtain the data?
	a. The data is presented in an excel sheet in figure S1. There are links for figure S1 provided in the paper itself, which can be found in the Supporting Information section of the paper.
3) What are the main steps needed to recreate the figure?
	a. I plan on graphing the figure in R. The basic syntax to create a line graph in R is displayed below. I plan on using a variation of this syntax to create my figure. The basic script steps are also displayed below. Finally, as suggested, I'm going to generate a summary statistics table, with code shown below.
		i. plot (v,type,col,xlab,ylab)
		ii. Script Steps:
			1. Create the data for the chart
			2. Give the chart a file name
			3. Plot the bar chart
			4. Save the file
		iii. Summary Statistics:
			1. vtable::sumtable()
*Updates*
 - Added raw data to data file and in separate folder on github repository on Monday, February 20, 2023; 3:27 pm


## Homework 2

**Methods**

*Data*
Data source: Excel file
Data acquisition: Link found in original paper

*Methods*
*Scatterplot Formation*
1) Save data in R:
	a. save(data, file = "Figure7D.Rdata")

2) Create the data for the chart:
	a. input <- Fold Change to Plot[c,('wt','het'

3) Give the chart file a name:
	a. png(file = "Figure_7D.png")

4) Plot the bar chart:
	a. plot(x = input$wt,y = input$het,
		i. xlab = "Normalized NMNAT2 level",
		ii. ylab = "Normalized Fold Change",
		iii. xlim c(0,2.5),
		iv. ylim c(0,2.5),
		v. main = "NMNAT2 abundance is positively correlated to the levels of synaptic proteins"
	b.)

5) Save the file:
	a. dev.off()


*Scatterplot Matrix*
1) Give the chart file a name:
	a. png(file = "Figure_7D matrices.png")

2)Plot the matrices between 6 variables given 6 plots

3) One variable with 5 others and total 6 variables.
	a. pairs(~SNAP25+SYPH+HSP90+VGluT1+Rim1-alpha+NR1,data = Figure7D,
		i. main = "NMNAT2 abundance is positively correlated to the level of synaptic proteins")

4) Save the file: 
	a. dev.off 

*Summary Statistics Table*
1)Generate a summary statistic table:
	a. vtable::sumtable()

**References**
1) Ali YO, Allen HM, Yu L, et al., NMNAT2:HSP90 complex mediates proteostasis in proteinopathies. *PLOS Biology*. June 2 2016; doi:0.1371/journal.phbio.1002472
2) "R - Line Graphs." *TutorialsPoint*, TutorialsPoint, 28 July 2021, https://www.tutorialspoint.com/r/r_line_graphs_.htm.
3) "R - Scatterplots." *TutorialsPoint*, TutorialsPoint, 2023, https://www.tutorialspoint.com/r/r.scatterplots.htm
