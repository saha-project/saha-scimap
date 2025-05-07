# SAHA SCIMAP

This repository contains the protein annotation scripts for the SAHA project.

## SCIMAPPrep.ipynb

Doesn't do much to be honest.

## RunSciMap.py

This python script runs the SCIMAP package to conduct gating and hierarchically assign cell types.

Before running the script, change line 41
```python
newAD = sm.pp.rescale(newAD,imageid='SAHA_name', method='by_image')
```

And line 48
```python
newAD.obs.groupby('SAHA_name').phenotype.value_counts()
```

Replace 'SAHA_name' with the obs column you use to separate the batches.

Run the script like so:
```bash
python RunSciMap.py adata.h5ad workflow_broad.csv adataSM.h5ad
```

## DifExpr.ipynb

This script examines how many cells are assigned differently between MaxFuse and SCIMAP and examines for cells in on annotation how they are assigned in another annotation.

## SCIMAPCompare.ipynb

This script examines visually how cell typing differences betwen MaxFuse and SCIMAP.

![a89edb97-2fc2-4f2f-87d5-5da1953826c4](https://github.com/user-attachments/assets/974c9943-44d1-4408-bfa9-1ac4555b0a09)
![187096a9-b467-4c93-9116-d452d8bfbb1a](https://github.com/user-attachments/assets/f432196f-9d54-4269-8f2d-04e1daf216a1)

## PrettyPictures.ipynb

This script generates the spatial mapping of cell typing derived from SCIMAP.

![e016052f-7059-43e3-95cf-f0489e29d68f](https://github.com/user-attachments/assets/79201b89-280f-47e9-8e4a-2eeaffbe4a80)

## UMAP_TSNE.ipynb

This script generates the UMAP, TSNE, and the cell proportion plots.

![umap_scimap](https://github.com/user-attachments/assets/38f017b6-9f8e-4810-a593-9b26decf84a3)
![077499d6-0a28-4e8f-a68b-f23521caaa99](https://github.com/user-attachments/assets/0eef83c6-64ff-4b0a-ba56-5b63bc25e280)
![843fdfe3-bb59-4c96-b326-382f350b4277](https://github.com/user-attachments/assets/ea5f79f0-ab89-4441-9bc0-7db5d03d56db)


