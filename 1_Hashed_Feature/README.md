# Hashed feature
It solves 3 problems with categorical feature:
* incomplete vocabulary - the training data does not contain all the possible;
* model size due to cardinality - the trained model could require a lot of space because of high size of vectors;
* cold start - predicts on new categories, which it wasn't be at the train dataset.

Trade-offs and Alternatives
* Bucket collisions.
* Skew - loss of accuracy.
* Aggregate features - replace categorical values with aggregate function, for example airporrt name - probability of on-time flights in the training dataset.
* Hyperparameters tuning - number of buckets in hash function should be hyperparameter to tune.
* Cryptographic hash - binary encoding + md5 hash will not suffer from spurious correlation problem beacuse the output of an MD5 hash is uniformly distributed, and so the resulting bits will be uniformly distributed.
