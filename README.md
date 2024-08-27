# SoybeanInverse

Start Date: 2/02/2023 <br />
Last Edit: 5/16/2023

In these script, I will be using visualizing the SoyNAM soybean dataset 
with the uniform manifold approximation and project (UMAP) algorithm. Pseudocode is also included.

Then, without UMAP dimensionality reduction, a random forest (RF) will be trained to 
predict a set of phenotypes from the genotype data available. A genetic 
algorithm (GA) will then be used to try to produce novel phenotypes by using the
trained RF as a forward simulator. The GA's solutions will be genotype with the
same format as the SoyNAM set, and will progress until a genotype that provides
the desired phenotype is discovered. The solution space of this problem is
massive, and will likely require an explorative, incremental approach similar
to the "Design, Build, Test, Learn" (DBTL) paradigm.

# Table of Contents

Part 1: Definitions and Visualization <br />
a) Import and Preprocessing <br />
b) UMAP Optimization by GA; Visualization of Phenotypes <br />
c) Random Forest Validation; K-Fold Cross Validation <br />
_______________________________________________
Part 2: Problem Statement <br />
a) Maximum SNP Tolerance Definition; Find Genotypes with Neighbors <br />
b) Can GA/RF find a removed point which is known to have nearest neighbors? <br />
_______________________________________________
Part 3: Visualization and "Sanity Check" of Pipeline <br />
a) Metrics by Bin: Generated Individual close to Genotypes of similar phenotype? <br />
b) UMAP Visualization of Generated Individuals against full population's phenotypes. <br />
c) UMAP Visualization of Generated Individuals against target neighbor cluster. <br />
_______________________________________________
Part 4: Incremental Optimization Proof of Concept <br />
a) GA Restricted to just individuals in a cluster. Can we accurately make an incremental change? <br />
b) In the largest cluster (19 individuals), how many of them can be recreated (reasonable time limit)? <br />
_______________________________________________
Part 5: Incremental Optimization Case Study <br />
a) Choose phenotype(s) to optimize. <br />
b) Loop incremental optimization, adding new individuals to the pipeline along the way. <br />
c) Visualize progression of individuals toward the phenotype goal. <br />
