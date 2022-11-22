**MOC**:: [[3.2. DL MOC]]
**Tags**:: #ml #projectmanagement 

# Directory structure
|-- **LICENCE**
|-- **Makefile**: contains commands like "make data" or "make train"
|-- **README.md**
|-- **Data/**
	|-- **external/**: data from third party sources
	|-- **interim/**: Intermediate transformed data
	|-- **raw/**: original data dump
	|-- **processed/**: final dataset for modeling
|-- **Models/**: trained and serialized models (.pt models for PyTorch)
|-- **Notebooks/**: folder for jupyter notebooks
|-- **References/**: Data dictionnaries, manuals and all other explanatory materials
|-- **Reports/**
	|-- **Figures/**: generated figures used in reporting
|-- **requirements.txt**: file for reproducing environnement
|-- **setup.py**: make project pip installable
|-- **src/**: folder for source code
	|-- **__init__.py**: make src a python module
	|-- **data/**
		|-- **make_dataset.py**: generating raw dataset for the model
	|-- **features/**
		|-- **build_features.py**: : for building features for the model
	|-- **models/**
		|-- **train_model.py**: scripts which train models
		|-- **predict_model.py**: scripts which make predictions
	|-- **visualization/**: scripts for generate visualization