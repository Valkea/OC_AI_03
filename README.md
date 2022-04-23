# Prepare data for a public health agency ("Préparez des données pour un organisme de santé publique")

[This project is part of the AI Engineer cursus on OpenClassrooms]

We are provided with a dataset from [openfoodfacts.org](https://world.openfoodfacts.org/data) which lists 2.251.894 products collected by volunteers.

There are 186 columns used to describe each product:

0 code                                               	1 url                                                
2 creator                                            	3 created_t                                          
4 created_datetime                                   	5 last_modified_t                                    
6 last_modified_datetime                             	7 product_name                                       
8 abbreviated_product_name                           	9 generic_name                                       
10 quantity                                           	11 packaging                                          
12 packaging_tags                                     	13 packaging_en                                       
14 packaging_text                                     	15 brands                                             
16 brands_tags                                        	17 categories                                         
18 categories_tags                                    	19 categories_en                                      
20 origins                                            	21 origins_tags                                       
22 origins_en                                         	23 manufacturing_places                               
24 manufacturing_places_tags                          	25 labels                                             
26 labels_tags                                        	27 labels_en                                          
28 emb_codes                                          	29 emb_codes_tags                                     
30 first_packaging_code_geo                           	31 cities                                             
32 cities_tags                                        	33 purchase_places                                    
34 stores                                             	35 countries                                          
36 countries_tags                                     	37 countries_en                                       
38 ingredients_text                                   	39 ingredients_tags                                   
40 allergens                                          	41 allergens_en                                       
42 traces                                             	43 traces_tags                                        
44 traces_en                                          	45 serving_size                                       
46 serving_quantity                                   	47 no_nutriments                                      
48 additives_n                                        	49 additives                                          
50 additives_tags                                     	51 additives_en                                       
52 nutriscore_score                                   	53 nutriscore_grade                                   
54 nova_group                                         	55 pnns_groups_1                                      
56 pnns_groups_2                                      	57 food_groups                                        
58 food_groups_tags                                   	59 food_groups_en                                     
60 states                                             	61 states_tags                                        
62 states_en                                          	63 brand_owner                                        
64 ecoscore_score                                     	65 ecoscore_grade                                     
66 main_category                                      	67 main_category_en                                   
68 image_url                                          	69 image_small_url                                    
70 image_ingredients_url                              	71 image_ingredients_small_url                        
72 image_nutrition_url                                	73 image_nutrition_small_url                          
74 energy-kj_100g                                     	75 energy-kcal_100g                                   
76 energy_100g                                        	77 energy-from-fat_100g                               
78 fat_100g                                           	79 saturated-fat_100g                                 
80 -butyric-acid_100g                                 	81 -caproic-acid_100g                                 
82 -caprylic-acid_100g                                	83 -capric-acid_100g                                  
84 -lauric-acid_100g                                  	85 -myristic-acid_100g                                
86 -palmitic-acid_100g                                	87 -stearic-acid_100g                                 
88 -arachidic-acid_100g                               	89 -behenic-acid_100g                                 
90 -lignoceric-acid_100g                              	91 -cerotic-acid_100g                                 
92 -montanic-acid_100g                                	93 -melissic-acid_100g                                
94 monounsaturated-fat_100g                           	95 polyunsaturated-fat_100g                           
96 omega-3-fat_100g                                   	97 -alpha-linolenic-acid_100g                         
98 -eicosapentaenoic-acid_100g                        	99 -docosahexaenoic-acid_100g                         
100 omega-6-fat_100g                                   	101 -linoleic-acid_100g                                
102 -arachidonic-acid_100g                             	103 -gamma-linolenic-acid_100g                         
104 -dihomo-gamma-linolenic-acid_100g                  	105 omega-9-fat_100g                                   
106 -oleic-acid_100g                                   	107 -elaidic-acid_100g                                 
108 -gondoic-acid_100g                                 	109 -mead-acid_100g                                    
110 -erucic-acid_100g                                  	111 -nervonic-acid_100g                                
112 trans-fat_100g                                     	113 cholesterol_100g                                   
114 carbohydrates_100g                                 	115 sugars_100g                                        
116 -sucrose_100g                                      	117 -glucose_100g                                      
118 -fructose_100g                                     	119 -lactose_100g                                      
120 -maltose_100g                                      	121 -maltodextrins_100g                                
122 starch_100g                                        	123 polyols_100g                                       
124 fiber_100g                                         	125 soluble-fiber_100g                                 
126 insoluble-fiber_100g                               	127 proteins_100g                                      
128 casein_100g                                        	129 serum-proteins_100g                                
130 nucleotides_100g                                   	131 salt_100g                                          
132 sodium_100g                                        	133 alcohol_100g                                       
134 vitamin-a_100g                                     	135 beta-carotene_100g                                 
136 vitamin-d_100g                                     	137 vitamin-e_100g                                     
138 vitamin-k_100g                                     	139 vitamin-c_100g                                     
140 vitamin-b1_100g                                    	141 vitamin-b2_100g                                    
142 vitamin-pp_100g                                    	143 vitamin-b6_100g                                    
144 vitamin-b9_100g                                    	145 folates_100g                                       
146 vitamin-b12_100g                                   	147 biotin_100g                                        
148 pantothenic-acid_100g                              	149 silica_100g                                        
150 bicarbonate_100g                                   	151 potassium_100g                                     
152 chloride_100g                                      	153 calcium_100g                                       
154 phosphorus_100g                                    	155 iron_100g                                          
156 magnesium_100g                                     	157 zinc_100g                                          
158 copper_100g                                        	159 manganese_100g                                     
160 fluoride_100g                                      	161 selenium_100g                                      
162 chromium_100g                                      	163 molybdenum_100g                                    
164 iodine_100g                                        	165 caffeine_100g                                      
166 taurine_100g                                       	167 ph_100g                                            
168 fruits-vegetables-nuts_100g                        	169 fruits-vegetables-nuts-dried_100g                  
170 fruits-vegetables-nuts-estimate_100g               	171 fruits-vegetables-nuts-estimate-from-ingredients_10
172 collagen-meat-protein-ratio_100g                   	173 cocoa_100g                                         
174 chlorophyl_100g                                    	175 carbon-footprint_100g                              
176 carbon-footprint-from-meat-or-fish_100g            	177 nutrition-score-fr_100g                            
178 nutrition-score-uk_100g                            	179 glycemic-index_100g                                
180 water-hardness_100g                                	181 choline_100g                                       
182 phylloquinone_100g                                 	183 beta-glucan_100g                                   
184 inositol_100g                                      	185 carnitine_100g                                     

- *Nutritional informations*: most of them are nutritional columns such as calcium, iron, fat, salt, vitamin-a, etc.
- *Meta informations*: several columns are used to identify the products, such as the product name, the code (barre-code), the open food fact url, etc.
- *Origins*: some others gives informations about the manufacturers, the sellers, the production place, the brand etc.
- *Categories*: several columns also give informations about the products types.
- *Scores*: finally the dataset also provides several scores such as the Nova_groups, the Ecoscore, the Nutriscore or Nutrigrade...

> The goal is to analyse this dataset in order to find some interesting application to build with it.

## Running the notebook online

The main notebook is quite heavy and it may not correctly display on Github.
However it can be displayed at the following address: [https://nbviewer.org/github/Valkea/OC_AI_03/blob/main/Cleaning_Nutrigrade.ipynb](https://nbviewer.org/github/Valkea/OC_AI_03/blob/main/Cleaning_Nutrigrade.ipynb)

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

#### Run the jupyter notebook

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

