## Run python Conda project using Docker

```
docker run -i -t -p 8888:8888 -v C:\WORK\workspace\python\python_practice:/opt/conda/envs --name conda-cont phenomback/conda-env:latest


// not tested. If it is not working check the <docker run -i -t -p 8888:8888 continuumio/anaconda3 /bin/bash -c "/opt/conda/bin/conda install jupyter -y --quiet && mkdir /opt/notebooks && /opt/conda/bin/jupyter notebook --notebook-dir=/opt/notebooks --ip='*' --port=8888 --no-browser --allow-root">
To run Jupyter: jupyter lab --ip='0.0.0.0' --port=8888 --no-browser --allow-root --notebook-dir=/home

conda create -n mlenv python=3.10 
conda activate mlenv

pip install pyqtwebengine 
pip install pyqt5
pip install -U bandit black flake8 mypy pydocstyle pylint
```


```
pip install -r ./requirements.txt
```
### publish the docker image

```bash
docker tag firstimage YOUR_DOCKERHUB_NAME/firstimage docker tag conda-env phenomback/conda-env

docker push YOUR_DOCKERHUB_NAME/firstimage docker push phenomback/conda-env

```

### push to private Docker hub Repo
```bash
docker tag [OPTIONS] IMAGE[:TAG] [REGISTRYHOST/][USERNAME/]NAME[:TAG] docker push NAME[:TAG]
```


## Python Notes
