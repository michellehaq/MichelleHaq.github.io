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

We also visualized ingredient frequency and distribution of sensitive-friendly products, shown in **Figure 1**
<img width="341" height="165" alt="image" src="https://github.com/user-attachments/assets/3d619398-e331-4805-8e9f-9351cb6199b6" />


**{: width="500" }

## Conclusion

From this work, the following conclusions can be made:

Machine learning can predict sensitive-skin friendliness from product ingredients with high accuracy.

Random Forest outperformed Logistic Regression and highlighted important irritant and protective ingredients.

Future development could involve expanding the dataset, integrating consumer reviews more fully, and using deep learning approaches for more detailed prediction.


## References
[1] Summer Fridays website: https://www.summerfridays.com

[2] Glow Recipe website: https://www.glowrecipe.com

[3] Laneige website: https://www.laneige.com

[4] The Ordinary website: https://theordinary.com

[5] Tatcha website: https://www.tatcha.com

[back](./)

