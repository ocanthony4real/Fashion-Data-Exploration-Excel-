# Fashion Dataset Exploration
This README.md file will serve as an article to documnent my process for this project *winks*

## Data Importation

The dataset was imported from Kaggle in CSV format. Thereafter, the dataset was then loaded into Excel and changed to xlsx format.
Observation
A thorough examination on the dataset revealed that the data needed some cleaning before it could be used to get useful information. Some of the observations made on the dataset include the non-linearity of the index column (i.e indexing resets to zero after every 26 columns), too many info on the ‘Deatils’ columns that could be split into multiple columns, redundancy of the word ‘size’ and ‘off’ in the Sizes and Discount columns respectively, amongst others. 

![EP1-1](https://user-images.githubusercontent.com/101093568/186724787-64948a92-0678-40a5-a74a-906825ab637c.png) 
(A view of the uncleaned data)

## Data Cleaning
To make the cleaning process easier, the dataset was first converted into a table called ‘FashionTable’. Below is a step-by-step process I followed in carrying out the data cleaning.

i)	New index: A consistent index was created and the former one deleted. This new index was created using the ROWS() function and was called ‘ID’.

ii)	Split Column: The ‘Deatils’ column was then split into two columns. The first column was corrected to ‘Details’, while the second the column was renamed ‘Color’. The colors were simply extracted from the Details columns of categories that has colors (which are footwears, nightwears, Indianwears, and Westernwears).

iii)	Trim cells (Category column): The Category column has the word “women” attached to every cell. This is redundant so I cleaned it off using the SUBSTITUTE() function. Then I inserted spaces in-between words to make them readable. 

iv)	Trim cells (Discount column): I removed the “off” attached to every cells in the column using the LEFT() function.

v)	Trim cells (Sizes column): I removed the word “sizes” from each cell as it’s redundant.

vi)	Format columns (MRP column): I formatted the MRP column to Rupees currency by first using the SUBSTITUTE(), CLEAN(), TRIM(), and VALUE() function. Thereafter, I clicked the Rp option in the Accounting dropdown list.

vii)	Format columns (all other columns): I changed the format of every other columns to their necessary formats.

viii)	Rename Columns: “Sizes” was renamed to “Sizes Available”, “Sellprice” renamed to “Selling Price”, “MRP” renamed to “Max. Retail Price”, “BrandName” renamed to “Brand Name”.

ix)	Filter columns: I removed rows that have their Brand Name as Nan (which was used to represent null values). Also, rows with errors in the Max. Retail Price and Color columns were removed. The affected columns were necessary for my analysis, therefore they ought to be complete if I must gain useful insight from the data.

x)	Remove columns: For this analysis, I realized that the Details and Sizes Available columns won’t be needed so I removed them.
Below is a screenshot of what the final table looks like:

 ![EP1-2](https://user-images.githubusercontent.com/101093568/186724996-48c17d12-bff1-4264-92ea-abbf59d0c470.png)
 
## Dashboard
For more flexibility, I first created a template of my dashboard using Power Point.
 Then I proceeded to drawing insights from my cleaned data. I plotted various charts with the data on the template. The final result is shown below:

![Dataset](https://user-images.githubusercontent.com/101093568/186725165-db7acb41-d7b5-4cc7-b24f-c2d86171f7a9.png)

  




	
