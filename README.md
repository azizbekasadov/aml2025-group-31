# aml2025-group-15
Gender Classification from Audio Signals using GNNs

# Project Overview

This project explores the application of Graph Neural Networks (GNNs) for gender classification based on audio signals. Inspired by the research paper Sensors 2024, we aim to evaluate the performance of two state-of-the-art GNN architectures on this task.

Approach

	1.	Feature Extraction: Use a pre-trained model (PTM) such as VGGish, PANNs, or YAMNet to extract meaningful features from raw audio signals.
 
	2.	Graph Construction: Represent extracted audio features as nodes in a graph.
 
	3.	GNN Model Implementation: Implement two GNN architectures (e.g., GCN, GAT, or GraphSAGE) for classification.
 
	4.	Performance Evaluation: Compare models using accuracy, precision, recall, and F1-score.

Challenges

	•	Data Acquisition: Ensuring a diverse and balanced dataset for training.
 
	•	Graph Construction: Developing an effective method to represent audio features as a graph, without access to the baseline paper’s code.

Datasets Used

	•	Gender Recognition by Voice – Raw audio signals (5,768 female, 10,400 male).
 
	•	Voice Gender Dataset – 21 feature attributes extracted from 3,168 audio samples.

Contributors

	•	Abu Bakr Rahman Shaik - 23-756-737 - abubakrrahman.shaik@uzh.ch
 
	•	Azizbek Asadov - 23-747-041 - azizbek.asadov@uzh.ch
 
	•	Jaaylin Anthony Martin - 24-741-530 - jaaylinanthony.martin@uzh.ch
