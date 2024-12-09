# CS-GY 6613: Artificial Intelligence Project

## Team Information

Team GitHub IDs:
* Shashank Pandey: ([pandeysh-25](https://github.com/pandeysh-25)), NetID: sp8108
* Bhavik Patwa: ([Bhavik-Patwa](https://github.com/Bhavik-Patwa)), NetID: bnp7995

* HuggingFace ID: sp8108
* The fine-tuned ROS2 model is loaded at: https://huggingface.co/sp8108/gpt2-finetuned-ros2

## About the Repository

This repository contains the submission for the AI final project (Fall 2024). The repository structure is as follows:

Infrastructure:
* The 'ETL-milestone' notebook details the ETL process and loading of data into MongoDB.
* The 'featurization-milestone' notebook covers the featurization of our textual data, updating our MongoDB entries, and storing into Qdrant.
* The 'rag-milestone' notebook goes through the initial implementation of our RAG system, using our processed vector data.
* The 'finetuning-dataset-generation' notebook covers the process we followed to generate question-answer pairs, which would be used to fine-tune the baseline model. The instructions we obtain from this process are saved in 'instruction_dataset.json'

Results:
* The 'app.ipynb' notebook covers the Gradio interfacing, showing how we integrate all parts of our pipeline.
* Our report and results are also in the repository.
