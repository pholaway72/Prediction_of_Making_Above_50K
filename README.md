# Does A Person Make >$50,000?

The goal of this project was to do two things.

1. The prediction task is to determine whether a person makes over 50K a year. (See `Problem1.ipynb`)
2. Perform a segmentation study. (See `Problem2.ipynb`)

To accomplish the first task, a logistic-regression model was trained using data from `au_train.csv`. The data set contains information the following information.

- `age`: The person's age
- `workclass`: What type of industry the person works in
- `fnlwgt`: The weight assigned by the US Census Bureau
- `education`: How far in school the person has gone
- `education-num`: A numeric level for each level in `education` with the lowest level being assigned the lowest number (`Preschool` = 1)
- `marital-status`: The marriage status of the person; for example, `Husband` or `Wife`
- `occupation`: What job that person has
- `race`: A person's race as reported to the US Census Bureau
- `sex`: A persons' sex as reported to the US Census Bureau
- `capital-gain`: A person's capital gains
- `capital-loss`: A person's capital loss
- `hours-per-week`: How many hours in a week a person works
- `native-country`: Where the person was originally from
- `class`: Either `<=50K` or `>50K`; so if the person made over $50,000

Not all variables above were used in the final logistic regression model. The final model trained achieved an accuracy score of 81.28% with an AUC = 0.67. The final model is listed below.

$\boxed{\text{logit(Class)}=-8.3157+0.043\text{ age}+0.0003\text{ capital-gain}+0.3228\text{ education-num}+0.0007\text{ capital-loss}+0.0407\text{ hours-per-week}}$

To accomplish the second task, proportional breakdowns were done to for `sex` and `race` by looking at the proportion of those in each group who made `<=50K` versus those who made `>50K`. To explain these breakdowns, futher breakdowns were done for both `sex` and `race` looking at `education`, `occupation`, and `hours-per-week`.
