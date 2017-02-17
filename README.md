# Machine Learning With Docker

A docker image with serveral machine learning tools installed. Based on tensorflow/tensorflow

## Includes
* Python
* Tensorflow
* Scikit Learn
* Pandas
* Numpy
* PIP
* PYMSQL

## Setup
1. Install [Docker](http://www.docker.com)
2. Create folder (ex: my-project) to share with docker container
3. Download latest docker image
	
	`docker pull chchannn/ml-starter`
	
4. Start docker container with shared notebook folder, please change your folder path accordingly:

	`docker run -i -t -p 8888:8888 -v /your/my-project/path/:/notebooks/ chchannn/ml-starter`
	
	On Windows it looks like `docker run -i -t -p 8888:8888 -v /c/my-project/:/notebooks/ chchannn/ml-starter`
	
	On macOS it looks like `docker run -i -t -p 8888:8888 -v ~/my-project/:/notebooks/ chchannn/ml-starter`
	
5. Visit  `localhost:8888` to login and use Jupyter server
	
6. Default Jupyter password is **ml-starter**

7. Optional - Change default memory
	
	`docker-machine stop`

	`VBoxManage modifyvm default --cpus 2`

	`VBoxManage modifyvm default --memory 4096`

	`docker-machine start`

