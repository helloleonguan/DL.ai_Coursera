# ML Strategy - 2

## Learning Objectives 
* Understand what multi-task learning and transfer learning are. 
* Recognize bias, variance and data-mismatch by looking at the performances of your algorithm on train/dev/test sets. 

### 1. Error Analysis 
* estimating the ceiling on different ideas
![](./img/wk02_ceiling.png)
![](./img/wk02_ceiling2.png) 
* cleaning up incorrectly labeled data
![](./img/wk02_incorrect_labeled.png)
_if it's systematic errors, then it will be an issue for the DL algorithm. e.g. consistently incorrectly label lions as cats._
* if the incorrectly labeled data are in dev set, add another colomn in the error analysis  
![](./img/wk02_incorrect_labeled2.png)
* advice on correcting incorrect samples
![](./img/wk02_advice_on_correcting.png)
* build your first system quickly, then iterate
![](./img/wk02_iterate.png)

### 2. Mismatched training and dev/test set
* Training and Testing on Different Distributions
![](./img/wk02_distribution.png)
![](./img/wk02_distribution2.png)
* Bias and Variance with mismatched data distributions


