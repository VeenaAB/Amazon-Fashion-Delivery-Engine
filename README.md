# Amazon-Fashion-Discovery-Engine
Build a recommendation engine which suggests similar products (apparel) to the given product (apparel) in any e-commerce websites.
## Statement

Personalized product recommendations are the alternative way of navigating through the online shop. More people find products they need. Even if they didn’t think of them.

Build a recommendation engine which suggests  similar products to the given product  in any e-commerce websites ex. Amazon.com, myntra.com etc.

## Objective 

The recommendation engine, uses information about 1,80,000 products and  each product will have multiple features named

1. Title of the product  
2. Brand of the product
3. Color of the product
4. Type of the product
5. Image of the apparel , etc...

# Procedure
- Download dataset from Kaggle
- Data Cleaning
  - Remove null values using isnull() of numpy 
  - Remove stopwords using nltk.stopwards from the discription and/or title
  - Text preprocessing
    - Stem the words in each column
    - remove duplicate products after stemming
- Create word to vector for each product
- Corrolation matrices
  - Text based product similarity
    - Bag of Words (BoW) on product titles (titles containing similar words)
  - TF-IDF (Term Freq - Inverse Document Freq) based product similarity:
    - how important word(s) is in a product title/discription and use it to find products having same word(s) in title/discription
  - Text Semantics based product similarity
    - Find products with similar discription
  - Visualization Based product similarity
    - Find similar product based on apparence using heat map and use it to find corrolation
- Recommendation Engine
  - Feed word to vector calculated above to keras CNN
  - Train model for similarity based on distance of vectors (similar if vectors are near)
  - For an input, calculate the vector
  - Suggest nearest K vectors to the given vector

### Data Source : amazon.com
