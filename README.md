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
| Availability    | `fast`, `user`, `time`, `alltimes`, `available`      |
| Fault Tolerance | `able`, `fast`, `stream`, `system`, `shall`          |
| Maintainability | `user`, `take`, `must`, `new`, `update`              |
| Performance     | `process`, `website`, `time`, `response`, `fast`     |
| Scalability     | `fast`, `use`, `able`, `process`, `support`          |
| Security        | `fast`, `data`, `information`, `access`, `authorize` |
| Usability       | `able`, `access`, `alltimes`, `easy`, `use`          |

As expected, the most representative bigrams of this kind of sentences (due to it's predefined syntax) were the following ones: `system shall`, `must able`, `system must`, `shall able`, `user able`, `authorize user`, `user user`, `user shall`, `shall easy`, `use system`