# RAG Systems for Robotics Development

### Contributor Information

* Shashank Pandey: ([pandeysh-25](https://github.com/pandeysh-25)), NetID: sp8108
* Bhavik Patwa: ([Bhavik-Patwa](https://github.com/Bhavik-Patwa)), NetID: bnp7995

* The fine-tuned GPT2 model is loaded at: https://huggingface.co/sp8108/gpt2-finetuned-ros2

### About the Repository

This repository contains the structured pipeline for developing a RAG (Retrieval-Augumented Generation) system, designed for robotics development - focusing on subdomains including ROS2 (robotics), and Nav2 (navigation), among others. The repository structure is as follows:

#### Pipeline:

Our pipeline has four parts:
* <b>ETL (Extract-Transform-Load)</b>: Here, we extracted data from various sources (including GitHub documentation, and YouTube videos) for each subdomain. We then perform standard text processing tasks before storing our data in MongoDB. This process is outlined in the 'ETL-milestone' notebook.
* <b>Featurization</b>: In this stage, we featurize our text (building on the basic transformations we had done earlier), and store our data in the Qdrant vector search engine. This is covered in the 'featurization-milestone' notebook.
* <b>RAG implementation</b>: We implement our basic RAG system, using our processed vector data to identify relevant context from our database for the query, before feeding it to a standard GPT-2 model. The 'rag-milestone' notebook contains this initial implementation. We later fine-tune our language model, and use it to generate responses.
* <b>Deployment</b>: We use Gradio to generate a simple Python app for deploying our model. We include a few sample queries in a drop-down menu that can be prompted to demonstrate the performance of our model.

#### Generating data for fine-tuning:
The 'finetuning-dataset-generation' notebook covers the process we followed to generate question-answer pairs, which would be used to fine-tune the baseline model. The Q/A pairs we obtain from this process are saved in 'instruction_dataset.json'

### Visualization

The overarching flow of the project can be seen in these images. The left image covers how our data collection process worked, while the right image details the components and flow of our RAG system.


<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/user-attachments/assets/37a26081-5e3c-4a2c-8a73-1890148ba134" alt="The ETL process" width="400" height="400"> &nbsp;&nbsp;&nbsp;&nbsp;
    <img src="https://github.com/user-attachments/assets/a0a06e9c-3df2-49d5-90b6-1bf5f30e3784" alt="The rest of our pipeline" width="400" height="400">
</div>

#

> Images courtesy of Pantelis Monogioudis, Ph.D. (adjunct professor at New York University)
