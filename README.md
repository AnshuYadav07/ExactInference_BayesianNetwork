# ExactInference_BayesianNetwork

This code builds a Bayesian Network to predict the probability of a disease based on symptoms (fever, cough, fatigue). It leverages exact inference using Variable Elimination to compute the probability of a hidden state (having a disease) given observable data (symptoms). This kind of model is useful for medical diagnosis or any scenario where we need to infer hidden causes based on observed evidence.




WHAT IT IS DOING:

	•	Modeling a health problem: It constructs a probabilistic model where having a disease is a hidden variable, and symptoms like fever, cough, and fatigue are observable.
	•	Predicting disease probability: Based on the symptoms provided, the model computes the likelihood of a person having the disease.
	•	Exact inference: Uses an algorithm called Variable Elimination to calculate exact probabilities.



WHY IT IS REQUIRED:

	•	Bayesian networks are essential for decision-making under uncertainty, particularly when we need to reason about probabilities given incomplete information.
	•	Exact inference ensures we get precise probability values rather than estimates, which is critical in domains like healthcare.
