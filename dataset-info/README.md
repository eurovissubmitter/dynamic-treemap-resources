# Dataset analysis
Each notebook file in this folder explores a different dataset from the `dataset` folder. 
It is possible to see its contents on the browser simply by opening it. 

To batch run the analysis: 
```
for dataset in $(find dataset/* -maxdepth 0 -type d); do papermill dataset-info/1DatasetBase.ipynb dataset-info/$(basename $dataset).ipynb -p input_dir $dataset; done
```
Adding new analysis and plots can be done by editing `DatasetBase.ipynb` and rerunning the command above.
