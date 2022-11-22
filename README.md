# food-ingredients-for-good

# Plan

1. Data discovery
    + Kaggle dataset
    + Recipe data
2. Data model
    + fact
    + dim
        + UOM
3. EDA
4. Classifying ingredients
    + Clustering
        + Numeric features
        + Unstructured features
    + Deep learning from unstructured text
5. Conversions
    + Adding this step for now
6. Recipe comparison
7. Data pipeline
    + preprocessing (cleanse and prepare data)
        + pre deployment
        + post deployment
    + predictions
    + consumption
8. Refactor code?


# virtual environment

`pip3 install virtualenv`
`virtualenv venv`
`source venv/bin/activate`

[virtual environment setup guide](https://sourabhbajaj.com/mac-setup/Python/virtualenv.html)

# EDA Questions

1. What foods can be substituted for meats and still have the same amount of protein?
2. How many groups of foods are there based on ingredients?
3. Can we classify foods simply based on their ingredients? Does it make intuitive sense?
4. What foods have the highest sugar, protein, fat, or calories?


# Clustering

Each observation in the dataset has a unique label (both a 'key', "NBD_No", and a text label for the ingredient, "Descrip"). My hypothesis is that similar foods have similar nutritional values, meaning we may be able to see distinct groupings of these foods based on their nutritional value.

I examine three (3) different clustering algorithms for this dataset:

1. [Kmeans](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html)  
2. [Agglomerative Clustering](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.AgglomerativeClustering.html)
3. [DBSCAN](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.DBSCAN.html)

**Result:** There is some utility in clustering observations by their nutritional value, because some clusters have very similar foods assigned to them. However, this is not a flawless approach, since clusters will also contain very different foods, making it difficult to say what the cluster represents (in terms of food). Additionally, a numeric approach using the silhouette score for clustering algorithms shows that the clusters still overlap and are not distinct from each other. 

**Next Steps:**  
+ Keep a baseline clustering method available and iterate to improve
+ Examine other ways to assign foods to a group or give them a label using their nutritional value.
    + Deep learning on a subset of manually labeled ingredients
        + Decide on a apriori labeling method for food ingredients

# Product 


# Directories

+ data

# References

https://www.kaggle.com/datasets/thedevastator/now-with-more-nutrients
