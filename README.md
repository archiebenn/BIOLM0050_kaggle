# Kaggle Challenge - where do proteins localise?  
Understanding where proteins localise is essential for uncovering their biological function and role in disease.  

### Challenge details and description  
This competition (https://www.kaggle.com/competitions/bbinf-26-subcell) challenges participlants to build a machine learning model that predicts the subcellular localisation of metazoan proteins based on their features:

- Proteins can be in more than one location (mutlti label type problem)
- Some of the proteins are natural, some are natural sequences, and some are engineered proteins
- Inbalanced data - some compartments have many examples (like cytoplasm), while others have less (like peroxisome)
- Protein localisation depends on many subtle factors: AA sequence motifs, signal peptides, post-translational modifications, and 3D structure. Capturing all from sequence alone is difficult

### Dataset Description
Data provided in `.csv` format. The following files are provided:  
- `train.csv` - training set
- `test.csv` - test set  
- `sample_submission.csv` - example of a submission in the correct format  
- `metaData.csv` - supplementary information about the data  

### Submission and Evaluation  
For each protein in the test set, a line with the protein ID followed by 1 or 0 depending on if the corresponding localisation is predicted or not. Example submission file:  

```
Id,cytoplasm,nucleus,extracellular,cell_surface,mitochondrion,endom
5,0,0,0,0,0,0
9,1,0,0,0,0,0
14,0,0,0,0,0,1
15,0,0,0,0,0,0
17,1,0,0,0,0,0
18,1,1,0,0,0,0
```

The submitted model is evaluated based on an F1-score (macro averaged)
