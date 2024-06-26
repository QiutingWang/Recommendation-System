# Recommendation-System
## Goal: 
Through `f(U,I,C) function` predicts the favorable rates and generate ranking recommendation list of items(`I`) give to user(`U`) under some context(`C`).

## Metholodolgy Graph
```mermaid
graph LR
  A[Recommendation System]-->B(Collaborative Filtering)-->D(Memory Based)
  A-->C(Content Based Method)
  B-->E(Model Based)
  D-->F(User-User)
  D-->G(Item-Item)
  E-->H(Matrix Factorization)
  C-->I(Item-centred Classification Problem)
  C-->J(User-centred Regression Problem)
```

### Collaborative Filtering Method
   - Intuition: based solely on past interactions records between users and items to make new recommendations, stored in "`user-item interaction matrix`"
   -  Use past information to *detect similar users or items* and make predictions based on these estimated proximities.
   - Categories:
     - **Memory Based**: Directly work with recorded interactions.No models. Based on nearest neighbors.
       - User-User: Use KNN calculate the similarity between different users
       - Item-Item: Use KNN calculate the similarity between items will be recommended and users' prefered item.
     - **Model Based**: New representative users and items are build based on a generative model.
   - Advantages: Requires no information about users or items, just needs interactions.
   - Drawbacks: Suffer more cold start problem than Content-Based Method.
   
### Content Based Method
  - Intuition: Based on features explaining user-item interaction, regarded as classification(T/F,item-centred) or regression(rating,etc.,user-centred) problem. For example, LS-PLM, Factorization Machine.
  - Mix Up: Two features factors (information about both user-centered and item-centered) can be used in a **neutral network architecture**. For example, GBDT+LR
    
## Paper
- [Collaborative Filtering Recommender Systems](https://files.grouplens.org/papers/FnT%20CF%20Recsys%20Survey.pdf)
- [Item-Based Collaborative Filtering Recommendation Algorithms](https://www.ra.ethz.ch/cdstore/www10/papers/pdf/p519.pdf)
- [DeepFM:A Factorization-Machine based Neural Network for CTR Prediction](https://arxiv.org/pdf/1703.04247)
- [Wide & Deep Learning for Recommender Systems](https://arxiv.org/pdf/1606.07792)
- [A Survey on Postive and Unlabelled Learning](https://www.eecis.udel.edu/~vijay/fall13/snlp/lit-survey/PositiveLearning.pdf)
- [PEBL: Positive Example Based Learning for Web Page
Classification Using SVM](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=0d2d9049679c18d90a836d7d05bcf93d4ffe9842)
