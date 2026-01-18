Named Entity Recognition (NER) on News Articles using spaCy
Project Overview

This project implements a Named Entity Recognition (NER) pipeline on news articles using spaCy.
Since the dataset does not contain entity-level annotations (character offsets), a weakly supervised learning approach is used by bootstrapping entity labels from a pretrained spaCy model and fine-tuning it on news-domain text.

The system preprocesses news articles, trains a custom NER model, evaluates it using standard metrics, and applies it to annotate unseen news articles.

Key Features

Handles real-world datasets without entity spans

Uses weak supervision for NER training

Fully compatible with spaCy 3.x

End-to-end pipeline: preprocessing → training → evaluation → inference

Produces annotated news articles as output

Approach
Problem

The dataset provides document-level labels, but no entity offsets, which are required for supervised NER training.

Solution

Use a pretrained spaCy NER model (en_core_web_sm) to auto-generate entity spans

Treat generated entities as weak labels

Fine-tune a custom spaCy NER model on news articles

Evaluate and apply the trained model to new articles

This approach mirrors industry-standard weak supervision techniques.
