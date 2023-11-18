# Exploring the Efficacy of Simple Models and Feature Engineering Techniques in Text Classification: A Comparative Analysis

Paper: [Exploring the Efficacy of Simple Models and Feature Engineering Techniques in Text Classification.pdf](https://github.com/DanielDaCosta/Text-Classification-Exploration/blob/main/Exploring%20the%20Efficacy%20of%20Simple%20Models%20and%20Feature%20Engineering%20Techniques%20in%20Text%20Classification.pdf)

# Abstract
Text classification is one of the core tasks of Natural Language Processing. Despite being such a complicated task, reasonable results can be obtained by using simple models such as Logistic Regression and Naive Bayes. Beyond the choice of model, the method of feature en- gineering employed also holds an important role in predicting accurate labels. In this paper, we implement these models from scratch using their default configurations and perform a comparative analysis with alternative feature engineering techniques such as Bag-of-Words, TF-IDF (Term Frequency - Inverse Document Frequency), and Word Embedding.

# Introduction
The primary goal of this paper is to provide a comprehensive exploration of the methodologies and strategies involved in constructing Logistic Regression and Naive Bayes models from scratch. When building these models, it is important to focus not only on correctly implementing them but also on the discerning selection of feature engineering techniques that yield optimal results across all four datasets. To achieve this goal, not only are the models effectively developed, but also analyze feature engineering methods.

# Usage
## Train
- 4dim
```
python train.py -m naivebayes -i datasets/4dim.train.txt -o nb.4dim.model

python train.py -m logreg -i datasets/4dim.train.txt -o logreg.4dim.model

python train.py -m logreg_word2vec -i datasets/4dim.train.txt -o logreg_word2vec.4dim.model -e word2vec_embedding.wordvectors

python train.py -m naivebayes_tfidf -i datasets/4dim.train.txt -o naivebayes_tfidf.4dim.model
```
- odiya
```
python train.py -m naivebayes -i datasets/odiya.train.txt -o nb.odiya.model

python train.py -m logreg -i datasets/odiya.train.txt -o logreg.odiya.model

python train.py -m logreg_word2vec -i datasets/odiya.train.txt -o logreg_word2vec.odiya.model -e word2vec_embedding.wordvectors

python train.py -m naivebayes_tfidf -i datasets/odiya.train.txt -o naivebayes_tfidf.odiya.model
```
- products
```
python train.py -m naivebayes -i datasets/products.train.txt -o nb.products.model

python train.py -m logreg -i datasets/products.train.txt -o logreg.products.model

python train.py -m logreg_word2vec -i datasets/products.train.txt -o logreg_word2vec.products.model -e word2vec_embedding.wordvectors

python train.py -m naivebayes_tfidf -i datasets/products.train.txt -o naivebayes_tfidf.products.model
```
- questions
```
python train.py -m naivebayes -i datasets/questions.train.txt -o nb.questions.model

python train.py -m logreg -i datasets/questions.train.txt -o logreg.questions.model

python train.py -m logreg_word2vec -i datasets/questions.train.txt -o logreg_word2vec.questions.model -e word2vec_embedding.wordvectors

python train.py -m naivebayes_tfidf -i datasets/questions.train.txt -o naivebayes_tfidf.questions.model
```
## Classify
- 4dim
```
python classify.py -m nb.4dim.model -i datasets/4dim.val.test.txt -o datasets/4dim.val.pred.txt

python classify.py -m logreg.4dim.model -i datasets/4dim.val.test.txt -o datasets/4dim.val.pred.txt

python classify.py -m logreg_word2vec.4dim.model -i datasets/4dim.val.test.txt -o datasets/4dim.val.pred.txt

python classify.py -m naivebayes_tfidf.odiya.model -i datasets/4dim.val.test.txt -o datasets/4dim.val.pred.txt

```
- odiya
```
python classify.py -m nb.odiya.model -i datasets/odiya.val.test.txt -o datasets/odiya.val.pred.txt

python classify.py -m logreg.odiya.model -i datasets/odiya.val.test.txt -o datasets/odiya.val.pred.txt

python classify.py -m logreg_word2vec.odiya.model -i datasets/odiya.val.test.txt -o datasets/odiya.val.pred.txt

python classify.py -m naivebayes_tfidf.odiya.model -i datasets/odiya.val.test.txt -o datasets/odiya.val.pred.txt
```
- questions
```
python classify.py -m nb.questions.model -i datasets/questions.val.test.txt -o datasets/questions.val.pred.txt

python classify.py -m logreg.odiya.model -i datasets/odiya.val.test.txt -o datasets/odiya.val.pred.txt

python classify.py -m logreg_word2vec.odiya.model -i datasets/odiya.val.test.txt -o datasets/odiya.val.pred.txt

python classify.py -m naivebayes_tfidf.odiya.model -i datasets/odiya.val.test.txt -o datasets/odiya.val.pred.txt
```

- products
```
python classify.py -m nb.products.model -i datasets/products/val.test.txt -o datasets/products.val.pred.txt

python classify.py -m logreg.products.model -i datasets/products/val.test.txt -o datasets/products/val.pred.txt

python classify.py -m logreg_word2vec.products.model -i datasets/products/val.test.txt -o datasets/products/val.pred.txt

python classify.py -m naivebayes_tfidf.products.model -i datasets/products/val.test.txt -o datasets/products/val.pred.txt
```
