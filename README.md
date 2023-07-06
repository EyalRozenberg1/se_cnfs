# SEMI-EQUIVARIANT CONDITIONAL NORMALIZING FLOWS

Official data of:

**Semi-Equivariant Conditional Normalizing Flows, With Applications to Target-Aware Molecule Generation**  
>Eyal Rozenberg, Daniel Freedman  
{eyalrozenberg,danielfreedman}@verily.com  

[LINK TO PAPER ON MLST (Machine Learning: Science and Technology)]

**Abstract**:  
Learning over the domain of 3D graphs has applications in a number of scientific and engineering disciplines, including molecular chemistry, high energy physics, and computer vision. We consider a specific problem in this domain, namely: given one such 3D graph, dubbed the base graph, our goal is to learn a conditional distribution over another such graph, dubbed the complement graph. Due to the three-dimensional nature of the graphs in question, there are certain natural invariances such a distribution should satisfy: it should be invariant to rigid body transformations that act jointly on the base graph and the complement graph, and it should also be invariant to permutations of the vertices of either graph. We propose a general method for learning the conditional probabilistic model, the central part of which is a continuous normalizing flow. We establish semi-equivariance conditions on the flow which guarantee the aforementioned invariance conditions on the conditional distribution. Additionally, we propose a graph neural network architecture which implements this flow, and which is designed to learn effectively despite the typical differences in size between the base graph and the complement graph. We demonstrate the utility of our technique in the molecular setting by training a conditional generative model which, given a receptor, can generate ligands which may successfully bind to that receptor. The resulting model, which has potential applications in drug design, displays high quality performance in the key ∆Binding metric.

### DATA:
To demonstrate the utility of our technique in the molecular setting we use CrossDocked2020 [Francoeur et al.,2020] dataset. This is a standardized dataset for training ML models with ligand poses cross-docked against non-cognate receptor structure, greatly expanding the number of poses available for training. The dataset is organized by clustering of similar binding pockets across the PDB; each cluster contains ligands cross-docked against all receptors in the pocket. Each receptor-ligand structure also contains information indicating the nature of the docked pair, such as root mean squared deviation (RMSD) to the reference crystal pose and Vina cross-docking score [Trott and Olson, 2010] as implemented in Smina [Koes et al., 2013]. 
* Instruction to download the raw data for the CrossDocked2020 set:  
https://github.com/gnina/models/tree/master/data/CrossDocked2020
* Download the tarballs (v1.1) from:  
http://bits.csb.pitt.edu/files/crossdock2020/v1.1/
* The refined datasets pointers:  
Training  
Validation  
Evaluation  
