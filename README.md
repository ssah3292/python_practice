# python_practice

<h1 align="center"> How to create conda docker env.</h1>

docker run -i -t -p 8888:8888 -v "%CD%":/opt/conda/envs --name conda-cont phenomback/conda-env
conda create -n mlenv python=3.10
activate env2

conda remove --name ENVIRONMENT --all

jupyter lab --ip='0.0.0.0' --port=8888 --no-browser --allow-root --notebook-dir=/home




pip install -U bandit black flake8 mypy pydocstyle pylint
pip install pyqtwebengine
pip install pyqt5
pip install -U bandit black flake8 mypy pydocstyle pylint


docker container commit dd30406df397 conda-env:latest

docker tag firstimage YOUR_DOCKERHUB_NAME/firstimage
docker tag conda-env phenomback/conda-env


docker push YOUR_DOCKERHUB_NAME/firstimage
docker push phenomback/conda-env

push to private docker
-----------------------
docker tag [OPTIONS] IMAGE[:TAG] [REGISTRYHOST/][USERNAME/]NAME[:TAG]
docker push NAME[:TAG]



