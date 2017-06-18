# Using EM for inducing verb  and noun classes in an unsupervised manner

Using Estimation Maximization to induce verb and noun classes based on extracted verb-noun-pairs, following Rooth et al. (1999)

## Contributors

- [pagelj](https://github.com/pagelj)
- [thefth](https://github.com/thefth)

## Variables

| Variable Name | Content |
|:-----|:-----|
|p\_c| Probability for each class|
|p\_v\_c| Probability for a verb being in a class|
|p\_n\_c| Probability for a noun being in a class|
|pairs\_classes| Joint probability for a verb and noun being in a class|
|v\_c| Hard verb classes|
|n\_c| Hard noun classes|
|verb\_noun\_rank| Ranked nouns for a intransitive verb|
|verb\_noun\_value| Accumulated probability for all nouns belonging to an intransitive verb|

## Data

- *gold_deps.txt*: Reduced data
- *all_pairs*: All pairs, not preprocessed
- *new_pairs*: All pairs, preprocessed

### Abbreviations

| Abbr. | Explanation |
|:-----:|:-----|
| s | intransitive verb |
| so | transitive verb |
| nsubj | nominal subject |
| csubj | clausal subject |
| nsubjpass | nominal subject in passive construction |
| dobj | direct object |
| iobj | indirect object |

### Verb-Noun pairs e.g.

| Verb | Co-occurring noun |
|:-----|:-----|
| testify\_s\_nsubj| list|
|make\_so\_nsubj| teacher|
|lead\_s\_csubj| deciding|
|give\_so\_csubj| adding|
|leave\_s\_nsubjpass| vegetable|
|make\_so\_nsubjpass| project|
|reach\_so\_dobj| leader|
|become\_so\_iobj| member|

## Example class

**Class 5: Change on a Scale - Numbers**

| Verbs | Prob | Nouns | Prob |
|:-----|:-----:|:-----|:-----:|
| pay\_so\_dobj |  0.0674 | price | 0.0389 |
| rise\_s\_nsubj | 0.0623 | number | 0.0304 |
| fell\_s\_nsubj | 0.0459 | attention | 0.0300 |
| draw\_so\_dobj | 0.0349 | profit | 0.0257 |
| fall\_s\_nsubj | 0.0203 | rate | 0.0257 |
| rise\_so\_nsubj | 0.0193 | share | 0.0226 |
| bring\_so\_dobj | 0.0191 | cost | 0.0210 |
| increase\_so\_dobj | 0.0185 | sale |  0.0169 |
| cut\_so\_dobj | 0.0179 | earnings | 0.0152 |
| increase\_s\_nsubj | 0.0168 | level |  0.0107 |

## Example intr. verb noun ranks

**begin\_s\_nsubj**

| Noun |  Score |
|:-----|-----:|
| work | 11.3236 |
| process | 8.4428 |
| which | 6.3095 |
| trial | 6.2411 |
| discussion | 5.9485 |
| phase | 5.8081 |
| career | 5.6166 |
| shipment | 5.5813 |
| series | 5.4629 |
| programme | 5.2699 |

## ToDo

- Achieving tracable computation of transitive verbs with ranked nouns

# References

Mats Rooth, Stefan Riezler, Detlef Prescher, Glenn
  Carroll, and Franz Beil. 1999. Inducing a semantically
  annotated lexicon via EM-based clustering. In
  Proceedings of the 37th Annual Meeting of the Association
  for Computational Linguistics on Computational
  Linguistics. Association for Computational
  Linguistics, Stroudsburg, PA, USA, ACL ’99, pages
  104–111. http://www.aclweb.org/anthology/P99-1014.
