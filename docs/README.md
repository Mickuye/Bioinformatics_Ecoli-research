# Comprehensive Genome Analysis of Escherichia coli Strains
**ABSTRACT**

This study presents a comparative genomic analysis of multiple Escherichia coli strains, focusing on chromosomal sequence properties, antimicrobial resistance, phylogenetic relationships, and subsystem distribution. Using publicly available genome sequences and established bioinformatics pipelines, we performed a systematic workflow consisting of quality control, assembly, annotation, resistance profiling, phylogenetic reconstruction, and subsystem analysis. The modular structure of this project ensures transparency, reproducibility, and accessibility for both researchers and students in bacterial genomics.

# Materials and Methods
**GENOME ANNOTATION**

To identify genes linked to chromosomal properties, antimicrobial resistance, and mobile genetic elements, we annotated assembled contigs using the PATRIC (v3.46.3) pipeline, targeting bacterial genomes. Each contig was assigned a unique genome identifier, enabling accurate classification and downstream comparisons.

**Outputs:** [Annotation Reports](https://github.com/Mickuye/Bioinformatics_Ecoli-research/tree/8dd400a6fd8a42b2e5c29d7996ea7734b56bb1e2/analyses/annotation)

**COMPARATIVE ANTIMICROBIAL RESISTANCE ANALYSIS** 

The resistome profiles of the E. coli genomes (strains MOD1–EC4326 and SCHI0016.S.230) were analyzed using BLASTP, k-mer–based detection, and the BV-BRC BLAST pipeline. Antibiotic Resistance Genes (ARGs) were systematically classified into mechanistic categories, clarifying each strain’s resistance potential.

**Outputs:** Resistance Profiles

**Results**

**_Chromosomal Sequence Properties_**
The chromosomal properties of the two E. coli genomes are summarized in Table 1. E-1 had the largest genome length and highest coding sequence (CDS) count, while E-2 exhibited a higher N50 and slightly higher GC content.

**Outputs:** Quality Control Reports

**_Table 1. Chromosomal Genome Properties_**

<img width="1200" height="70" alt="image" src="https://github.com/user-attachments/assets/eba17884-2785-4052-84c8-78f1cdeef9d7" />


# Quality Control & Assembly
-	E-1 (SRR3951549): 243 contigs, N50 = 146,357, GC = 50.28%
-	E-2 (SRR11094155): 45 contigs, N50 = 359,891, GC = 50.70%
Assemblies were produced using Unicycler v0.4.8, refined with Samtools v1.13, and validated with QUAST v5.2.0.

# Phylogenetic Analysis
A phylogenetic tree was constructed to examine the evolutionary relationship of the studied strains with additional E. coli references.
-	Tree format: Newick file
-	Visualization: Phylogenetic Tree (PDF/PNG)

**Findings:**
-	E-1 clustered with known multidrug-resistant clades, consistent with its resistome profile.
-	E-2 branched closer to metabolically versatile, less resistant strains.
-	The branching pattern confirmed congruence between resistance traits and evolutionary clustering.

# Subsystem Distribution

Subsystem profiling highlighted differences in metabolic pathways, resistance features, and mobile genetic elements.
-	Data tables: Subsystems (CSV/XLSX)
-	Visualization: Heatmap
  
# Findings (Heatmap):

-	Strain E-1: Enriched in subsystems associated with antimicrobial resistance (efflux pumps, β-lactamases) and mobile genetic elements.
-	Strain E-2: Fewer resistance subsystems but stronger representation in metabolic processes (carbohydrate utilization, membrane transport).
  
# Interpretation:
E-1 shows greater adaptation to antibiotic stress, likely reflecting evolutionary pressure from antimicrobial exposure. In contrast, E-2 prioritizes metabolic versatility over resistance, suggesting divergent survival strategies.

# Scripts
All scripts are provided in the scripts/ folder.
-	**subsystem_heatmap.R:** generates the subsystem heatmap from processed data.

# Conclusion

This project demonstrates a complete comparative genomic analysis pipeline for E. coli, from raw data to interpretation. Strain E-1 exhibited genomic signatures of multidrug resistance, supported by phylogenetic clustering and subsystem enrichment. Strain E-2 showed a reduced resistance profile but enhanced metabolic capacity. Together, these findings illustrate how E. coli strains balance resistance acquisition and metabolic adaptability, offering insights into bacterial evolution under selective pressures.


