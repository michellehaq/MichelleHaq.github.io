<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>


## My Project

I applied machine learning techniques to investigate skincare toxicity from the five most purchased skincare brands at Sephora. The brands include Summer Fridays, The Ordinary, Glow Recipe, Laneige, and Tatcha. 
***

## Introduction 

Sensitive skin is a common concern among skincare consumers, and many products can cause irritation, redness, or even allergic reactions. Manually identifying safe products is time-consuming and can sometimes be unreliable because ingredient lists are long and difficult to decipher. This problem is important because it impacts consumer skin health and can help guide safer product development.

I collected a dataset of products from the five brands, including ingredient lists, average ratings, and reviews mentioning sensitivity or irritation. This dataset allows a supervised machine learning approach, where the input features are ingredients and reviews, and the target label is whether the product is suitable for sensitive skin.

By training models such as logistic regression and random forest classifiers, I aimed to automatically classify products and identify ingredients that correlate with irritation or safety. It was concluded that machine learning can provide useful guidance for predicting sensitive-skin compatinility based on ingredients and reviews.

## Data

The dataset includes about 200 skincare products from the five brands. For each product,  recorded:

Product name

Brand

Full ingredient list

Average rating

Sensitive-skin label (binary)

Data was scraped directly from brand bsites. Preprocessing steps included:

Cleaning ingredient text (lorcasing, removing punctuation, standardizing names like “Aqua → Water”)

Generating TF-IDF features from ingredient lists

Labeling products as 1 for sensitive-skin friendly or 0 otherwise

Splitting the data into 80% training and 20% testing

I also visualized ingredient frequency and distribution of sensitive-friendly products, shown in **Figure 1**
<img width="341" height="165" alt="image" src="https://github.com/user-attachments/assets/3d619398-e331-4805-8e9f-9351cb6199b6" />


Figure 2 shows the top 15 ingredients that most strongly influence whether a product is predicted to be sensitive-skin friendly, according to the Random Forest model. Ingredients like “fragrance” and “alcohol denat” have high importance because their presence strongly predicts that a product may irritate sensitive skin, while soothing ingredients like “aloe vera” and “glycerin” contribute positively to friendly classifications. This figure helps explain the model’s predictions and supports the conclusion that certain ingredients are key determinants of skin sensitivity in skincare products.
<img width="340" height="210" alt="image" src="https://github.com/user-attachments/assets/537c9d86-274a-4839-b9ca-d889f1345df4" />


## Conclusion

From this work, the following conclusions can be made:

Machine learning can predict sensitive-skin friendliness from product ingredients with high accuracy.

Random Forest outperformed Logistic Regression and highlighted important irritant and protective ingredients.

Future development could involve expanding the dataset, integrating consumer reviews more fully, and using deep learning approaches for more detailed prediction.


## References
[1] Summer Fridays bsite: https://www.summerfridays.com

[2] Glow Recipe bsite: https://www.glowrecipe.com

[3] Laneige bsite: https://www.laneige.com

[4] The Ordinary bsite: https://theordinary.com

[5] Tatcha bsite: https://www.tatcha.com

[back](./)

