# Text Representation

The process to vectorize the requirements in order to be used for classification is implemented as follows:

1. Unnecessary characters removal
2. Lower-casing
3. Punctuation signs removal
4. Lemmatization
5. Stop word removal
6. Label ecoding
7. TF-IDF Vectorization

Once the sentences were processed, a further analysis using the CHI squared algorithm for feature selection identified the following most correlated unigrams and bigramas per Quality Attribute:

| Quality Attribute   | Unigrams                                                   | Bigrams                          |
| ------------------- | ---------------------------------------------------------- | -------------------------------- |
| **AVAILABILITY**    | `failure`, `achieve`, `hours`, `availability`, `available` | `system must`, `shall available` |
| **FAULT TOLERANCE** | `eg`, `control`, `result`, `failure`, `operate`            | `within system`, `system shall`  |
| **MAINTAINABILITY** | `maintain`, `design`, `new`, `update`, `maintenance`       | `use system`, `user able`        |
| **PERFORMANCE**     | `status`, `result`, `less`, `response`, `fast`             | `less fast`, `response time`     |
| **SCALABILITY**     | `manner`, `capable`, `support`, `handle`, `number`         | `shall support`, `shall capable` |
| **SECURITY**        | `authorize`, `password`, `security`, `encrypt`, `access`   | `user system`, `authorize user`  |
| **USABILITY**       | `use`, `content`, `navigation`, `easy`, `page`             | `shall easy`, `use system`       |

Finally, the features were split and exported with a 17:3 ratio for training and test sets, the pickles `X_train`, `X_test`, `y_train` and `y_test` are expected to be implemented on the [Automated Model Configuration repository](https://github.com/quality-attributes/irace-configuration). The same split ratio and random state are going to be used for the deep learning classifiers as well.