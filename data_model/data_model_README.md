# data_model_README.md


|Source|Name|Description|
|------|----|-----------|
|Kaggle|cleaned_ingredients.csv|Downloadable file from Kaggle with source data for cleaned ingredients and their nutritional value|



## L0

This is a replica of the source data.

`cleaned_ingredients`

|column_name | data_type | nullable| default_value | description |
|------------|-----------|---------|---------------|-------------|
| NDB_No | varchar(10) | No | "N/A" | | A unique ID for ingredient |
|Descrip | varchar(200) | No | 
|Energy_kcal | decimal | Yes | | |
|Protein_g | decimal | Yes | | |
|Saturated_fats_g | decimal | Yes | | |
|Fat_g | decimal | Yes | | |
|Carb_g | decimal | Yes | | |
|Fiber_g | decimal | Yes | | |
|Sugar_g | decimal | Yes | | |
|Calcium_mg | decimal | Yes | | |
|Iron_mg | decimal | Yes | | |
|Magnesium_mg | decimal | Yes | | |
|Phosphorus_mg | decimal | Yes | | |
|Potassium_mg | decimal | Yes | | |
|Sodium_mg | decimal | Yes | | |
|Zinc_mg | decimal | Yes | | |
|Copper_mcg | decimal | Yes | | |
|Manganese_mg | decimal | Yes | | |
|Selenium_mcg | decimal | Yes | | |
|VitC_mg | decimal | Yes | | |
|Thiamin_mg | decimal | Yes | | |
|Riboflavin_mg | decimal | Yes | | |
|Niacin_mg  | decimal | Yes | | |
|VitB6_mg | decimal | Yes | | |
|Folate_mcg | decimal | Yes | | |
|VitB12_mcg | decimal | Yes | | |
|VitA_mcg |  decimal | Yes | | |
|VitE_mg  |   decimal | Yes | | |
|VitD2_mcg |   decimal | Yes | | |


`conversion`

|column_name | data_type | nullable| default_value | description |
|------------|-----------|---------|---------------|-------------|
|ingredient | varchar(50) | No | N/A | The name of the ingredient, when applicable. |
| type | varchar(50) | No | N/A | The type of conversion (weight or volume). |
| uom | varchar(50) | No | N/A | The unit of measure for the ingredient to be converted> |
| uom_conversion | varchar(50) | No | N/A | The unit of measure to convert the ingredient into. | 
| conversion_factor | decimal | No | -1 | The factor to multiply the ingredient by to get the new unit of measure |