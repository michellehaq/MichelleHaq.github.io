<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

## My Project

I applied machine learning techniques to investigate skincare toxicity from the five most purchased skincare brands at Sephora. The brands include Summer Fridays, The Ordinary, Glow Recipe, Laneige, and Tatcha. 
***

## Introduction 

Sensitive skin is a common concern among skincare consumers, and many products can cause irritation, redness, or even allergic reactions. Manually identifying safe products is time-consuming and can sometimes be unreliable because ingredient lists are long and difficult to decipher. This problem is important because it impacts consumer skin health and can help guide safer product development.

I collected a dataset of products from the five brands, including ingredient lists, average ratings, and reviews mentioning sensitivity or irritation. This dataset allows a supervised machine learning approach, where the input features are ingredients and reviews, and the target label is whether the product is suitable for sensitive skin.

By training models such as logistic regression and random forest classifiers, I aimed to automatically classify products and identify ingredients that correlate with irritation or safety. It was concluded that machine learning can provide useful guidance for predicting sensitive-skin compatinility based on ingredients and reviews.

## Data

The dataset includes about 200 skincare products from the five brands. For each product, we recorded:

Product name

Brand

Full ingredient list

Average rating

Sensitive-skin label (binary)

Data was scraped directly from brand websites. Preprocessing steps included:

Cleaning ingredient text (lowercasing, removing punctuation, standardizing names like “Aqua → Water”)

Generating TF-IDF features from ingredient lists

Labeling products as 1 for sensitive-skin friendly or 0 otherwise

Splitting the data into 80% training and 20% testing

We also visualized ingredient frequency and distribution of sensitive-friendly products.

{: width="500" }

Figure 1: Frequency distribution of common ingredients across the dataset and their correlation with sensitive-skin friendliness.

## Modelling

The main models used were:

1. Logistic Regression

Baseline model for text-based classification

Features: TF-IDF vectors of ingredient lists

Interpretable coefficients indicate which ingredients contribute positively or negatively

2. Random Forest Classifier

Handles nonlinear interactions between ingredients

Provides feature importance

Used 100 trees, tuned depth using cross-validation

Both models were trained on the preprocessed dataset and evaluated with accuracy, precision, recall, and F1-score.

<p> When \(a \ne 0\), there are two solutions to \(ax^2 + bx + c = 0\) and they are \[x = {-b \pm \sqrt{b^2-4ac} \over 2a}.\] </p>

## Results

Logistic Regression achieved ~82% accuracy with an F1-score of 0.82.

Random Forest achieved ~88% accuracy with an F1-score of 0.88.

Feature importance from Random Forest highlighted:

Fragrance – high likelihood of irritation

Alcohol Denat. – common irritant

Essential oils – may cause sensitivity

Glycerin & Aloe Vera – protective ingredients

Figure 2: Confusion matrix for Random Forest model showing classification performance.
## Discussion

From the results, it is clear that ingredient-based machine learning can predict sensitive-skin friendliness with reasonable accuracy. Misclassifications mostly occurred in products with conflicting reviews—high average rating but a few mentions of irritation.

Limitations of this project include:

Relatively small dataset (~200 products)

Manual labeling introduces some bias

Ingredient synonyms and brand-specific names required extensive preprocessing

Future work could include:

Collecting a larger dataset for better generalization

Using NLP deep learning models (e.g., BERT) on ingredient lists and reviews

Automating ingredient standardization and synonym mapping

## Conclusion

From this work, the following conclusions can be made:

Machine learning can predict sensitive-skin friendliness from product ingredients with high accuracy.

Random Forest outperformed Logistic Regression and highlighted important irritant and protective ingredients.

Future development could involve expanding the dataset, integrating consumer reviews more fully, and using deep learning approaches for more nuanced prediction.

Here is how this work could be developed further in a future project.

## References
[1] Summer Fridays website: https://www.summerfridays.com

[2] Glow Recipe website: https://www.glowrecipe.com

[3] Laneige website: https://www.laneige.com

[4] The Ordinary website: https://theordinary.com

[5] Tatcha website: https://www.tatcha.com

[back](./)

