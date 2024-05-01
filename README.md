# SMILES Molecule Generator and Analyzer

This repository contains a Jupyter notebook that integrates various tools to generate and analyze SMILES (Simplified Molecular Input Line Entry System) molecules. The notebook allows users to input SMILES strings, generate new molecular structures using REINVENT, and calculate various chemical properties using RDKit. The molecules are then ranked based on their drug-likeness and other ADMET properties.

## Features

- **Molecule Generation**: Input SMILES and generate new molecules using the REINVENT framework.
- **Property Calculation**: Calculate molecular properties such as molecular weight, logP, and topological polar surface area using RDKit.
- **Dynamic Visualization**: Interactive widgets allow users to view and select different molecular properties dynamically.
- **Ranking System**: Molecules are ranked based on calculated properties to identify promising drug candidates.
- **3D Visualization**: Molecules can be selected for 3D visualization and inspection.

## Setup and Installation

1. **Clone the repository**:
```
git clone https://github.com/christos-efthymiou/Small-Molecule-Optimization.git
```
2. **Create a Conda environment** (recommended):
```
conda create -n reinvent python=3.10
conda activate reinvent
```
3. **Install required packages**:
Change directory into the REINVENT4 folder and install the dependencies from the lockfile (this command works for Windows 11):
```
pip install -r requirements-linux-64.lock
```
4. **Install the reinvent tool**: 
```
pip install --no-deps . 
```
5. **Check installation**: 
Test to make sure the tool was installed properly: 
```
reinvent --help
```
5. **Edit vocabulary.py file**: 
For Windows 11, you will need to edit the vocabulary.py file in the anaconda environment at this location (change the name to yours) "C:\Users\name\anaconda3\envs\reinvent4\lib\site-packages\reinvent\models\mol2mol\models\vocabulary.py". Open the file and replace the contents with the following: 
```
from reinvent.models.transformer.core.vocabulary import Vocabulary

__all__ = [Vocabulary]
```
6. **Install ipywidgets**: 
With the environment activated, install ipywidgets so the notebook functions properly with the following command: 
```
pip install ipywidgets
```
7. **Run the jupyter notebook**: 
In the terminal, use the following command to open the jupyter interface and then you can double click to open the notebook:
```
jupyter notebook
```

## Usage

- **Generating Molecules**: Enter a SMILES string and click the "Generate Molecules" button.
- **View Properties**: The calculated properties will be displayed in a dynamic table. Select the properties you wish to view using the provided widget.
- **Download Data**: The data will automatically be saved as a CSV file in the current directory.

## Contributing

Contributions to this project are welcome! Please fork the repository and submit a pull request with your features or fixes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
