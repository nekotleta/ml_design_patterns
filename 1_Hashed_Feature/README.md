# Hashed feature
It solves 3 problems with categorical feature:
* incomplete vocabulary - the training data does not contain all the possible;
* model size due to cardinality - the trained model could require a lot of space because of high size of vectors;
* cold start - predicts on new categories, which it wasn't be at the train dataset.
