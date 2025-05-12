# Medical-Prediction-with-Explainable-AI-using-Partial-Dependence-Plot-PDP-
To build a medical prediction system ( heart disease) using machine learning models integrated with Explainable AI (XAI) techniques specifically Partial Dependence Plots (PDPs
What PDPs Show
PDPs depict the marginal effect of one (or two) input features on a model’s predicted probability, averaging out the influence of all other features. This answers “If this feature changes while everything else stays the same on average, how does the prediction shift?”

Why They Matter in Medicine
For clinicians, a PDP can translate a complex model into an intuitive curve—e.g., “Above 150 mg/dL cholesterol the risk rises sharply.” Such visual evidence builds trust and can guide threshold-based interventions.

Single- vs. Two-Way PDPs

1-D PDPs: One feature on the x-axis, predicted risk on the y-axis.

2-D (Interaction) PDPs: Heat map or contour plot for two features (e.g., age × resting BP) to surface interaction effects.


Feature Selection Tips

Start with clinically meaningful variables (age, chol, thalach, cp, trestbps, thal).

Prefer features with low collinearity; strongly correlated inputs can muddy PDP interpretations.


Model Requirements
PDPs work for any fitted model that implements predict or predict_proba. Tree-based ensembles (Random Forest, XGBoost) are ideal because they naturally handle non-linearities captured by PDPs.
