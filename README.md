# Prepare data for a public health agency ("Préparez des données pour un organisme de santé publique")

[This project is part of the AI Engineer cursus on OpenClassrooms]

We are provided with a dataset from [openfoodfacts.org](https://world.openfoodfacts.org/data) which lists 2.251.894 products collected by volunteers.

There are 186 columns used to describe each product:

- *Nutritional informations*: most of them are nutritional columns such as calcium, iron, fat, salt, vitamin-a, etc.
- *Meta informations*: several columns are used to identify the products, such as the product name, the code (barre-code), the open food fact url, etc.
- *Origins*: some others gives informations about the manufacturers, the sellers, the production place, the brand etc.
- *Categories*: several columns also give informations about the products types.
- *Quantities*: multiple columns give informations about the serving quantity or the quantity in the package.
- *Scores*: finally the dataset also provides several scores such as the Nova_groups, the Ecoscore, the Nutriscore or Nutrigrade...

> The goal is to analyse this dataset in order to find some interesting application to build with it.

## Running the notebook online

The main notebook is quite heavy and it may not correctly display on Github.
However it can be displayed at the following address: [https://nbviewer.org/github/Valkea/OC_AI_03/blob/main/Cleaning_02_Nutrigrade.ipynb](https://nbviewer.org/github/Valkea/OC_AI_03/blob/main/Cleaning_02_Nutrigrade.ipynb)

## Running the notebook locally

In order to use this project locally, you will need to have Python and Jupyter notebook installed.
Once done, we can set the environment by using the following commands:

### First, 
let's duplicate the project github repository

```bash
>>> git clone https://github.com/Valkea/OC_AI_03
>>> cd OC_AI_03
```

### Secondly,
let's download the dataset from [Open Food Facts](https://static.openfoodfacts.org/data/en.openfoodfacts.org.products.csv)

```bash
>>> wget https://static.openfoodfacts.org/data/en.openfoodfacts.org.products.csv -P data
```

### Thirdly,
let's create a virtual environment and install the required Python libraries

(Linux or Mac)
```bash
>>> python3 -m venv venvP3
>>> source venvP3/bin/activate
>>> pip install -r requirements.txt
```

(Windows):
```bash
>>> py -m venv venvP3
>>> .\venvP3\Scripts\activate
>>> py -m pip install -r requirements.txt
```

### Finally,
let's configure and run the virtual environment for Jypiter notebook


#### Install jupyter kernel for the virtual environment using the following command:

```bash
>>> pip install ipykernel
>>> python -m ipykernel install --user --name=venvP3
```

#### Run the jupyter notebooks

in order to see the script used to reduce the number of columns from 186 to 36, run the following:
```bash
>>> jupyter notebook Cleaning_01_Preselection.ipynb

```

and to run the main EDA, use the following command:
```bash
>>> jupyter notebook notebook.ipynb
```

#### Select the installed kernel
Click on the kernel and click change kernel you will be able to see the kernel you just created.
![alt text](medias/venv_selection.png)

#### Uninstalling the venv kernel
Once done with the project, the kernel can be listed and removed using the following commands:

```bash
>>> jupyter kernelspec list
>>> jupyter kernelspec uninstall venvP3
```

