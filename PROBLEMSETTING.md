# Gender Classification from Audio Signal using GNNs

## Team members:

**Abu Bakr Rahman Shaik** - 23-756-737 - abubakrrahman.shaik@uzh.ch 

**Azizbek Asadov** - 23-747-041 - azizbek.asadov@uzh.ch 

**Jaaylin Anthony Martin** - 24-741-530 - jaaylinanthony.martin@uzh.ch

## Overview

The main motivation of the project is to evaluate the performance of SOTA GNN architectures for classification of gender based on audio signals, this has significant applications in various fields such as security, healthcare, and human-computer interaction.
The paper (https://www.mdpi.com/1424-8220/24/7/2106) demonstrated that GNNs produce superior results for environmental sound signal classification. Inspired by the paper, this project aims to implement a similar setting to compare the performance of 2 leading GNN architectures for gender classification. 

## Problem Formulation

The problem formulation builds on the baseline paper, which employed 3 audio signal PTMs for feature extraction and 3 GNN architectures for classification. But due to the unavailability of code from the baseline paper for replication, this project will limit the scope by focusing on one PTM and two GNN architectures.

The project will have the following steps: 

**1. Audio signal Implementation**

		[i]  Selection and implementation of PTM: Choose one robust audio signal PTM for extracting meaningful features from the audio data. The baseline paper used VGGish, PANNs and YAMNet for feature extraction. 
		[ii] Feature Extraction: Utilize the selected PTM to convert audio signals into feature vectors that can be used for graph node representation.

**2. Graph Construction**

		Each extracted feature vector will represent a node in the graph.

**3. GNN Architectures Implementation**

		[i]  Architecture Selection: Choose two distinct GNN architectures. The baseline paper used GCN, GAT and GraphSAGE architectures for classification tasks.
		[ii] Implementation: Implement both GNNs to train on the graph data obtained from the chosen PTM features.

**4. Performance Evaluation**

		Use classification accuracy, precision, recall, and F1-score as performance metrics to compare the GNN architectures.



## Challenges

**Data Acquisition:** Unknown datasets from Kaggle; can't be sure if it is a diverse and representative dataset of audio signals for effective training.

**Graph Construction:** Defining an optimal method for graph construction that captures the relationships between audio features effectively. Lack of the baseline paper's code makes this part challenging. 


## Datasets 

https://www.kaggle.com/datasets/murtadhanajim/gender-recognition-by-voiceoriginal -  Raw Audio signals in 2 folders (5,768 F and 10,400 M)

https://www.kaggle.com/datasets/primaryobjects/voicegender - Data of 21 attributes of 3,168 audio signals and labels 

		


