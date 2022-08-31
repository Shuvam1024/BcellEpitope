# BcellEpitope
I replicated and then further tuned the parameters of a Machine Learning model in a Kaggle Project on COVID-19/SARS B-cell Epitope Prediction

Description:  B-cells inducing antigen-specific immune responses in vivo produce large amounts of antigen-specific antibodies by recognizing the subregions (epitope regions) of antigen proteins. They can inhibit their functioning by binding antibodies to antigen proteins. Predicting epitope regions is beneficial for the design and development of vaccines aimed at inducing antigen-specific antibody production. However, prediction accuracy requires improvement.
 
The conventional epitope region prediction methods have focused only on the target sequence in the amino acid sequences of an entire antigen protein and have not thoroughly considered its sequence and features as a whole. The work here uses a deep learning method based on short-term memory with an attention mechanism to consider the characteristics of a whole antigen protein in addition to the target sequence. The proposed method achieves
better accuracy compared with the conventional method in the experimental prediction of epitope regions using the data from the immune epitope database.
 
A simple dataset for epitope prediction used in vaccine development:
Due to the spread of COVID-19, vaccine development is being demanded as soon as possible. The dataset and the sample code used in this project for B-cell epitope prediction are open-source. The data was obtained from IEDB and UniProt.  

The data: Information on whether or not an amino acid peptide exhibited antibody-inducing activity (marked by an activity label) could be obtained from IEDB, which was used in many previous studies. Accordingly, this information was used as the label data. We also obtained the epitope candidate amino acid sequences (peptides) and the activity label data from the B-cell epitope data provided in IEDB. The presented antibody proteins were restricted to IgG, which constituted the most recorded type in IEDB. For convenience, we excluded records representing different quantitative measures of antibody activity for the same peptide from experiments. The epitope data obtained from IEDB corresponded to the five types of activity: "Positive-High," "Positive-Intermediate," "Positive-Low," "Positive," and "Negative." However, due to the limited number of data elements marked with the "Positive-High," "Positive-Intermediate," and "Positive-Low" labels, we equally considered these labels as "Positive", thereby attributing the task to a binary estimation.

Content
This contains three data files:

input_bcell.csv : this is our main training data. The number of rows is 14387 for all combinations of 14362 peptides and 757 proteins.
input_sars.csv : this is also our main training data. The number of rows is 520.
input_covid.csv : this is our target data. there is no label data in columns.

All of three datasets consists of information of protein and peptide:

parent_protein_id : parent protein ID
protein_seq : parent protein sequence
start_position : start position of peptide
end_position : end position of peptide
peptide_seq : peptide sequence
chou_fasman : peptide feature, β turn
emini : peptide feature, relative surface accessibility
kolaskar_tongaonkar : peptide feature, antigenicity
parker : peptide feature, hydrophobicity
isoelectric_point : protein feature
aromacity: protein feature
hydrophobicity : protein feature
stability : protein feature
and bcell and sars dataset have antibody valence(target value):
target : antibody valence (target value)

Relevant Papers

Epitope Prediction of Antigen Protein using Attention-Based LSTM Network (2020, bioRxiv)
https://www.frontiersin.org/articles/10.3389/fimmu.2017.00278/full

Acknowledgments
Data is provided from The Immune Epitope Database(IEDB) and UniProt.

Inspiration
Automated methods for B-cell epitope prediction. Machine learning helps rapid vaccine development.

Disclaimer
We make no warranties regarding the correctness of the data, and disclaim liability for damages resulting from its use. We cannot provide unrestricted permission regarding the use of the data, as some data may be covered by patents or other rights.
