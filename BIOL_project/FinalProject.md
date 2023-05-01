# NMNAT2 Abundance is Positively Correlated to the Level of Synaptic Protein

1. Ali YO, Allen HM, Yu L, et al., NMNAT2:HSP90 complex mediates proteostasis in proteinopathies. *PLOS Biology.* June 2 2016; doi:0.1371/journal.pbio.1002472


## Introduction
Nicotinamide mononucleotide adenylyl transferase (NMNATs) are important for neuronal maintenance of *Drosophila* and humans. Overexpression of these proteins provides neuroprotection in many neurodegenerative models, especially in Wallerian degeneration. NMNATs are also known as nicotinamide adenine dinucleotide (NAD)-synthesizing enzymes. They enable proper flux of NAD, which is an important cofactor in many cellular processes. When inducing Wallerian degeneration, NAD levels are reduced while exogenous NAD application offers neuronal protection. However, if NMNT enzymatic function is impaired in some way, neuronal protection is reduced. Recently, it's been discovered in *Drosophila* photoreceptor models that NMNAT enzymatic activity is not required to maintain neuronal integrity in these photoreceptors. This data suggests that NMNATs might be able to protect neurons by different mechanisms.

NMNAT2 is an example of a NMNAT enzyme. Constant supply of NMNAT2 from Golgi-derived vesicles is important in maintaining axonal health. When NMNAT2 is absent, neurite outgrowth deficits or axonal degeneration can occur. NMNAT2 is highly expressed in the mammalian brain. Reduction of *nmnat2* mRNA levels have been observed in individuals with Parkinson, Huntington, and Alzheimer's disease (AD). This and other recent data suggest that NMNAT2 is important for neuronal maintenance. However, the mechanisms underlying this maintenance remains unknown.

In *Drosophila*, *Drosophila* NMNAT (*d*NMNAT) acts as a molecular chaperone. Molecular chaperones are a class of proteins that either interact with, stabilize, or assist proteins in maintaining protein homeostasis (proteostasis) and facilitating the clearance of pathological protein aggregates. Recent data has shown that chaperones are important in maintaining neuronal function.

Proteinopathies, like AD and tauopathies, are characterized by stereotypic aggregated proteins. This pathology can also be associated with cognitive impairment. It has been hypothesized that enhancing chaperone activity can help to establish a cytoprotective state. Cytoprotective states occur when cellular damage, caused by misfolding or aggregation associated proteinopathies, is protected against the body. In AD, the role of chaperones has been studied in depth, especially in regard to tau aggregation and fibrillizaiton. It has been observed that chaperones like HSP70 and HSP90 preferentially bind to hyperphosphorylated human Tau (p-hTaus) and paired helical filamentous tau. Overexpression of these two chaperones inhibit the early stages of amyloid aggregation in AD. This paper aimed to answer three questions: Does NMNAT2 act as a chaperone? Is chaperone activity required for NMNAT2 to reduce tauopathy and protect neurons against protein stress? And how does NMNAT2 exert its chaperone function? To answer these questions, this study examined the relationship between *nmnat2* mRNA levels and the cognitive capabilities and AD pathology of a large cohort of human subjects.

The figure that I'm recreating was based on the results of a Western Blot analysis (figure 7C; see below). In the figure that I'm recreating (figure 7D; see below), it was determined beforehand that synapses are usually theh first structures lost in neurodegenerative disease. In fact, NMNAT2 has been detected in synaptic membranes and vesicles of cortical neurons. This data suggests that NMNAT plays a role in synaptic maintenance. To test this theory, presynaptic proteins (VGluT1, SNAP25, RIM1alpha, and SYPH) in both wild-type mice and mice without NMNAT2 were compared. Additionally, levels of the chaperone HSP90 and N-methyl-D-aspartate receptor 1 (NR1) in wild-type and NMNAT2 knockout mice were also compared. It was determined that presynaptic protein levels are positively correlated with NMNAT2 levels. However, there was no significant correlation between HSP90 and NR1 and NMNAT2. This data indicates that NMNAT2 plays a significant role in synaptic maintenance.

![Figure 7C](https://github.com/Intro-Sci-Comp-UIowa/biol-4386-course-project-LexysMarie/blob/main/BIOL_project/Pictures/Screen%20Shot%202023-04-06%20at%2012.11.48%20PM.png)

![Figure 7D](https://github.com/Intro-Sci-Comp-UIowa/biol-4386-course-project-LexysMarie/blob/main/BIOL_project/Pictures/Screen%20Shot%202023-01-29%20at%202.13.03%20PM.png)

Figure 7. (C-D) Western analysis for the abundance of synaptic proteins in the hippocampi of 8-mo-old NMNAT2 HET and WT (n = 6 per genotype). The regression lines show the relationships between NMNAT2 and SNAP25, SYPH, VGluT1, RIM1alpha, HSP90, NR1. Protein levels were normalized to GAPDH.


## Materials and Methods
1. How was the experient performed to produce the data?

a. A Western Blot analysis was performed. The data is based off that analysis. The figure that I want to reprodue (figure 7D) is a line graph that shows regression lines presenting the correlation between NMNAT2 and SNAP25, SYPH, RIM1alpha, HSP90, and NR1. Protein levels were normalized to GAPDH.


2. Where and how will you obtain the data?

a. The data is presented in an excel sheet in figure S1. There are links for figure S1 provided in the paper itself, which can be found in the Supporting Information section of the paper.


3. What are the main steps needed to recreate the figure?

a. I graphed the figure using ggplot2 in R. The code that I used is displayed below. I will also be generating a summary statistics table, with code shown below as well.


*Methods*
*Note* A detailed analysis of my code can be found in the "scripts" folder of my GitHub repository. Here, I am just outlining the steps that are necessary to create my figure.


1. Load the ggplot2 package

2. Create a data frame

3. Save as a CSV file

4. Import your data

5. Load tidyr

6. Create grouped data

7. Load ggplot2

8. Create a ggplot object

9. Convert "name" to variable

10. Add a scatterplot layer

11. Add lines of best fit to each of the panels

12. Create a paneled scatterplot

13. Add color to the "HET" and "WT" variables

14. Customize the plot with titles and labels

15. Generate a summary statistics table


## Results and Discussion
![Recreated Figure 7](https://github.com/Intro-Sci-Comp-UIowa/biol-4386-course-project-LexysMarie/blob/main/BIOL_project/Intro%20to%20Scientific%20Computing%20Final%20Project.png)

Recreated Figure 7: The regression lines show the correlation between NMNAT2 and other synaptic proteins. Synaptic proteins analyzed include SYPH, SNAP25, VGluT1, RIMalpha, HSP90, and NR1. Protein levels were normalized to GAPDH.

This figure is based on results found in a Western Blot analysis (figure 7C; see above). Overall, the figure showed that the abundance of presynaptic proteins like SYPH, VGluT1, and RIM1alpha are positively correlated with NMNAT2 levels. Additionally, neurofilament levels and MAP2 are correlated with NMNAT2 levels. However, HSP90 and NR1 levels are not significantly related to NMNAT2. This data indicated that NMNAT2 is important for synaptic maintenance. 

Overall, there aren't any differences between my figure and the original one, even though one was produced in Excel and the other was produced in R using ggplot2. This is because the figure is very simple. It's just a scatterplot showing regression lines that is universally easy to generate.


## Reflection and Conclusion
This figure, while still easy to produce, was much more difficult to produce in R than in Excel in my opinion. This could make reproducibility difficult for other users, especially if they are starting from scratch, like I did. This figure is not very robust either. It would be hard to show these results in a bar graph, or a histogram for example. Even a line graph would be difficult. A line graph would show the individual points shown in the scatter plot, but a line of best fit would be difficult to generate. 
