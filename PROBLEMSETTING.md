# Gender Classification from Audio Signals using GNNs

## Team members

**Abu Bakr Rahman Shaik** - 23-756-737 - <abubakrrahman.shaik@uzh.ch>

**Azizbek Asadov** - 23-747-041 - <azizbek.asadov@uzh.ch>

**Jaaylin Anthony Martin** - 24-741-530 - <jaaylinanthony.martin@uzh.ch>

## Overview

The main motivation of the project is to evaluate the performance of GNN (Graph Neural Network) architectures for classification of gender based on audio signals. This has significant applications in various fields such as security, healthcare, and human-computer interaction.
The paper (<https://www.mdpi.com/1424-8220/24/7/2106>) demonstrated that GNNs produce superior results for environmental sound signal classification. Inspired by the paper, this project aims to implement a similar setting to compare the performance of GCN (Graph Convolutional Network) and GAT (Graph Attention Network) adapted for gender classification.

## Problem Formulation

The problem formulation builds on the baseline paper, which employed 3 audio signal PTMs (Pretrained Transformer-based Model) for feature extraction and 3 GNN architectures for classification. But due to the unavailability of code from the baseline paper for replication, this project will limit the scope by focusing on only one PTM and two GNN architectures.

Given this, the project will begin with us selecting a good PTM to use for getting the features of audio signals. The baseline paper used VGGish, PANNs and YAMNet for feature extraction so selection from one of these is ideal. Our data consists of .wav files of a single person speaking and labelled as being male or female. Using our chosen PTM we extract the features from each of these audio samples which will allow us to compare the meaningful data about each person's voice. These features will be represented as a node in our constructed graph. For comparison, we must connect each sample/node to their k most similar samples through the features of the nodes with the closest values, making each signal hopefully being clustered near others of the same gender.

To ensure this along with low prediction loss, we will utilize GCN and GAT due to them being the leading architectures that give great results, are well defined, and widely used. We will split our constructed graph nodes into a training, validation, and test set and feed the models training nodes along with their adjacency matrices for a simple single output of male or female classification. We will then tune the hyperparameters to find the best results on validation and see what is most important for each architecture in finding the predictions. Our evaluation on the test set will then include F1 score and AUROC(Area Under the Receiver Operating Characteristic curve). The F1 score is for balancing precision and recall which avoids having a high accuracy simply for always predicting the more likely gender, which in our case is mostly male samples. It ensures that fairness between predicting female is also accounted for and not just ignored due to being able to naively predict male because precision avoids false positives (predicting female when its male) and recall avoids false negatives (predicting male when its female). AUROC is also very important because it evaluates how well the model actually distinguishes between male and female predictions without pertaining to the imbalance in the data, just overall correct predictions. For our use case we will mainly focus on F1 score due to the imbalance, but will also evaluate AUROC to see the difference.

## Challenges

**Data Acquisition:** Unknown datasets from Kaggle; can't be sure if it is a diverse and representative dataset of audio signals for effective training.

**Graph Construction:** Defining an optimal method for graph construction that captures the relationships between audio features effectively. Lack of the baseline paper's code makes this part challenging.

## Datasets

<https://www.kaggle.com/datasets/murtadhanajim/gender-recognition-by-voiceoriginal> -  Raw Audio signals in 2 folders (5,768 F and 10,400 M)

<https://www.kaggle.com/datasets/primaryobjects/voicegender> - Data of 21 attributes of 3,168 audio signals and labels
