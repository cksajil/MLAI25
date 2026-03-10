# Explainable AI (XAI) and Responsible AI
## Key topics
- Explainable AI (XAI)
- Model Interpretability
- SHAP
- LIME
- Feature Importance
- Partial Dependence Plots
- AI Bias
- Responsible AI
- Ethics in AI

Explainable AI (XAI) refers to methods that make machine learning models transparent and interpretable to humans.
- XAI answers questions like:
- Why did the model make this prediction?
- Which features influenced the decision?
- Can we trust the model?

| Model             | Interpretability |
| ----------------- | ---------------- |
| Linear Regression | High             |
| Decision Trees    | Medium           |
| Random Forest     | Low              |
| Neural Networks   | Very Low         |

## Feature Importance
Feature importance tells us:
- Which features influence predictions most
- Which features may be irrelevant
```python
from sklearn.datasets import load_breast_cancer
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier

data = load_breast_cancer()

X = pd.DataFrame(data.data, columns=data.feature_names)
y = data.target

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

model = RandomForestClassifier()
model.fit(X_train, y_train)
```

```python
import matplotlib.pyplot as plt
import numpy as np

importances = model.feature_importances_

indices = np.argsort(importances)[::-1]

plt.figure(figsize=(10,6))
plt.title("Feature Importance")

plt.bar(range(10), importances[indices][:10])

plt.xticks(range(10),
           X.columns[indices][:10],
           rotation=90)

plt.show()
```

## Partial Dependence Plots
Partial dependence plots show how predictions change with feature values.
```python
from sklearn.inspection import PartialDependenceDisplay

PartialDependenceDisplay.from_estimator(
    model,
    X_train,
    ["mean radius"]
)

plt.show()
```
### Activity

- Generate PDP plots for:
- mean radius
- mean texture
- mean perimeter

## Types of Interpretability
- Global Interpretability (Explains how the model works overall)
- Local Interpretability (Explains one specific prediction. e.g.Why was this patient predicted as cancer positive?)

## Explainability Methods

### SHAP (SHapley Additive exPlanations)
```python
# pip install shap
import shap
explainer = shap.TreeExplainer(model)
shap_values = explainer.shap_values(X_test)
shap.summary_plot(shap_values, X_test)
```
This shows:
- Feature importance
- Feature influence direction
- Red features → increase prediction
- Blue features → decrease prediction

### LIME (Local Interpretable Model-Agnostic Explanations)
```python
# pip install lime
from lime.lime_tabular import LimeTabularExplainer

explainer = LimeTabularExplainer(
    training_data=X_train.values,
    feature_names=X.columns,
    class_names=['benign','malignant'],
    mode='classification')

exp = explainer.explain_instance(
    X_test.iloc[0].values,
    model.predict_proba)
exp.show_in_notebook()
```

### Comparing LIME and SHAP

| Feature             | SHAP        | LIME                  |
| ------------------- | ----------- | --------------------- |
| Theoretical basis   | Game theory | Local surrogate model |
| Consistency         | High        | Moderate              |
| Speed               | Slower      | Faster                |
| Global explanations | Yes         | Limited               |

## AI Bias and Fairness
Bias occurs when an AI system produces systematically unfair results. Example: Hiring algorithm preferring male candidates.

Sources of Bias
1. Data Bias: Training data reflects historical discrimination.
2. Sampling Bias: Dataset does not represent population.
3. Measurement Bias: Incorrect feature measurement.
4. Algorithmic Bias: Model design introduces unfairness.

## Responsible AI Development

Principles of Responsible AI:

1. Transparency: AI decisions should be explainable.
2. Fairness: Avoid discrimination.
3. Accountability: Developers responsible for outcomes.
4. Privacy: Protect user data.
5. Safety: AI should not harm humans.

### Responsible AI Checklist
Before deploying a model:
- Is it interpretable?
- Is bias evaluated?
- Are predictions explainable?
- Is the data ethically collected?