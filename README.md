# Text Representation

The process to vectorize the requirements in order to be used for classification is implemented as follows:
1. Unnecessary characters removal
2. Lower-casing
3. Punctuation signs removal
4. Lemmatization
5. Stop word removal
6. Label ecoding
7. TF-IDF Vectorization

Once the sentences were processed, a further analysis using the CHI squared algorithm for feature selection identified the following most correlated unigrams by Quality Attribute:

| Category        | Correlated unigrams                                  |
| --------------- | ---------------------------------------------------- |
| Availability    | `hours`, `year`, `time`, `alltimes`, `available`     |
| Fault Tolerance | `fast`, `view`, `stream`, `system`, `shall`          |
| Maintainability | `hours`, `change`, `must`, `new`, `update`           |
| Performance     | `process`, `take`, `website`, `response`, `fast`     |
| Scalability     | `use`, `fast`, `process`, `number`, `support`        |
| Security        | `fast`, `data`, `information`, `access`, `authorize` |
| Usability       | `able`, `first`, `easy`, `train`, `use`              |

As expected, the most representative bigrams of this kind of sentences (due to it's predefined syntax) were the following ones: `system shall`, `must able`, `user access`, `system must`, `shall available`, `shall able`, `authorize user`, `user able`, `user user`, `user shall`, `shall easy`, `use system`