# BcellEpitope
I reproduced and then further extended the Machine Learning model in a Kaggle Project on B-cell Epitope Prediction for COVID-19/SARS vaccine development.
Relevant Papers:
https://www.frontiersin.org/articles/10.3389/fimmu.2017.00278/full
https://www.biorxiv.org/content/10.1101/2020.07.27.224121v1.full.pdf

Data is from The Immune Epitope Database(IEDB).

This work outlines a method for B-cell epitope prediction using an attention-based long short-term memory network (LSTM), a deep learning approach, by incorporating target amino acid sequence as well as the long-range features of a whole protein. To address the problem of data sparseness, the method is extended to enable the simultaneous consideration of the structural and chemical features of an entire antigen protein in a deep-learning network. Length of candidate epitope peptide: 8-14 amino acids.
The structural and chemical features of the peptides considered in this study are the following: β-turn, relative surface accessibility, antigenicity, and hydrophilicity.  A total of eight of the structural and chemical features are integrated into the network of the proposed method. Then, the attention mechanism is applied to estimate which amino acids are particularly noteworthy for the purposes of epitope estimation. The proposed method achieves better accuracy compared with the conventional method in the experimental prediction of epitope regions using the data from the immune epitope database.


Content
		This contains three data files:
		

		input_bcell.csv : this is our main training data. The number of rows is 14387 for all combinations of 14362 peptides and 757 proteins.
		input_sars.csv : this is also our main training data. The number of rows is 520.
		input_covid.csv : this is our target data. there is no label data in columns.
		

		All of three datasets consists of information of protein and peptide:
		

		parent_protein_id : parent protein ID
		protein_seq       : parent protein sequence
		start_position    : start position of peptide
		end_position      : end position of peptide
		peptide_seq       : peptide sequence
		chou_fasman       : peptide feature, β turn
		emini             : peptide feature, relative surface accessibility
		kolaskar_tongaonkar : peptide feature, antigenicity
		parker            : peptide feature, hydrophobicity
		isoelectric_point : protein feature
		aromacity         : protein feature
		hydrophobicity    : protein feature
		stability         : protein feature
		and bcell and sars dataset have antibody valence(target value):
		target : antibody valence (target value)
    
    


