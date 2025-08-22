

We of course want to avoid guessing wrong and also penalize it when it happens.  we defines misclassification as the probability of assigning an object to the **wrong class**. For the **binary case** (classes 1 and 2), the misclassification probabilities are:
- Misclassifying **class 1 as class 2**:
$$
P(\text{label 2} \mid I = 1) = \pi_1 \int_{A_2} f_1(x) \, dx
$$

- Misclassifying **class 2 as class 1**:
$$
P(\text{label 1} \mid I = 2) = \pi_2 \int_{A_1} f_2(x) \, dx
$$

- **Total misclassification probability**:
$$
P_{\text{misclass}} = \pi_1 \int_{A_2} f_1(x) \, dx + \pi_2 \int_{A_1} f_2(x) \, dx
$$


This total is minimized when the decision boundary is chosen such that:
$$
\pi_1 f_1(x) = \pi_2 f_2(x)
$$Meaning now we have s "wall" (boundary) in the decision region so we can chose one of the sides, either left from the wall or right from the wall, formally:$$
\text{choose class 1 over 2 when } \pi_1 f_1(x) > \pi_2 f_2(x)
$$
