# Content-Based Recommender

This  project was created in my journey towards being a Data Scientist, in order to practice what I learn.

The objetive of the project is to create a hybrid book recommendation system that combines three types of recommenders:

- Simple recommender (top rated books)
- Collaborative filtering engine (readers like  you also enjoyed these books)
- Content-based recommender (other books like this)

## Datasets

To run the Jupyter Notebooks of this project first download, extract and place the CVS files of the following datasets in the corresponding folders.

| Folder | Dataset source |
|---|---|
| /dataset1 | <https://www.kaggle.com/arashnic/book-recommendation-dataset/version/1> |
| /dataset2 | <https://www.kaggle.com/sp1thas/book-depository-dataset> |

## System resources

I use a Docker container to run Jupyter Notebooks inside an Ubuntu linux machine.

The image is public, so you can use this command to launch the container (requires Docker Desktop on your machine).

    docker run -it -d -p 8888:8888 -v local_repo_path:path_inside_container --name mycontainer ptavaressilva/datascience:v1 /bin/bash

Once it is up, you can start Jupyter with the following command

    docker exec -it mycontainer jupyter notebook --no-browser --allow-root --ip 0.0.0.0

It then outputs the URL that you can use in your host's browser to connect to Jupyter.

Please note that this container should not be exposed to the network as it is intended for educational purposes.

The scope of this project does not include big data handling, therefore I reduced the dataset used for the content recommender, and it still required a hefty 24 GB of memory to calculate the TF-IDF matrix.
