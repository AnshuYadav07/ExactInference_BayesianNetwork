# ExactInference_BayesianNetwork


FIRST EXAMPLE SCENARIO:
This code builds a Bayesian Network to predict the probability of a disease based on symptoms (fever, cough, fatigue). It leverages exact inference using Variable Elimination to compute the probability of a hidden state (having a disease) given observable data (symptoms). This kind of model is useful for medical diagnosis or any scenario where we need to infer hidden causes based on observed evidence.


WHAT IT IS DOING:

	•	Modeling a health problem: It constructs a probabilistic model where having a disease is a hidden variable, and symptoms like fever, cough, and fatigue are observable.
	•	Predicting disease probability: Based on the symptoms provided, the model computes the likelihood of a person having the disease.
	•	Exact inference: Uses an algorithm called Variable Elimination to calculate exact probabilities.



WHY IT IS REQUIRED:

	•	Bayesian networks are essential for decision-making under uncertainty, particularly when we need to reason about probabilities given incomplete information.
	•	Exact inference ensures we get precise probability values rather than estimates, which is critical in domains like healthcare.


SECOND EXAMPLE SCENARIO

1.	Graph Structure (Bayesian Network):
	•	It creates a Bayesian Network where the nodes represent three observable variables:
	•	R: Whether it’s raining (Rain or No Rain)
	•	U: Whether the person carries an umbrella (Umbrella or No Umbrella)
	•	C: Whether the person catches a cold (Cold or No Cold)
	•	The directed edges in the graph represent dependencies:
	•	Rain affects whether a person carries an umbrella (R → U)
	•	Rain also directly affects whether a person catches a cold (R → C)
	•	Whether the person has an umbrella affects their chances of catching a cold (U → C)
	2.	Conditional Probability Distributions (CPDs):
	•	The probability of rain (R) is represented as a prior probability: there’s a 30% chance of rain and 70% chance of no rain.
	•	The probability of carrying an umbrella (U) depends on whether it’s raining. For instance, if it’s raining, there’s an 80% chance the person carries an umbrella.
	•	The probability of catching a cold (C) depends on both rain and the presence of an umbrella. For example, if it’s raining and the person has no umbrella, there’s a higher chance they catch a cold.
	3.	Inference:
	•	The inference step computes the probability of catching a cold given some evidence. For example, if we observe that it’s raining and the person doesn’t carry an umbrella, we can compute how likely they are to catch a cold.
	•	The Variable Elimination algorithm is used for exact inference. It eliminates irrelevant variables to compute the marginal probability for the variable of interest (C).
	4.	Evidence:
	•	Evidence is provided in the form of known information (e.g., it’s raining and the person doesn’t have an umbrella). This evidence is used to condition the probabilities and infer the likelihood of catching a cold (C).

Why it is Required:

	•	Probabilistic Reasoning: This model helps us reason under uncertainty. Instead of making deterministic predictions, the model handles uncertain situations (e.g., varying probabilities of rain and cold).
	•	Exact Inference: Bayesian Networks allow us to compute exact probabilities based on conditional dependencies between variables. In this case, the goal is to compute the likelihood of catching a cold based on observable factors (rain, umbrella).
	•	Decision Making: Such a model could be useful in decision-making systems where we need to predict outcomes based on incomplete or uncertain information. For example, based on weather conditions and personal habits, this model can predict health risks like catching a cold, which could inform decisions (e.g., whether to carry an umbrella).
	•	Handling Multiple Dependencies: Bayesian Networks are great for capturing complex dependencies between variables. Here, both rain and the use of an umbrella influence the likelihood of catching a cold, and the model accounts for these relationships explicitly.
