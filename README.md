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
2. Create Folder (ex: my-project) to Share with Docker Container
3. Download Latest Docker Image
	
	`docker pull chchannn/ml-starter`
	
4. Start Docker Container With Shared Notebook Folder, please change your folder path accordingly:

	`docker run -i -t -p 8888:8888 -v /your/my-project/path/:/notebooks/ chchannn/ml-starter`
	
	On Windows it looks like `docker run -i -t -p 8888:8888 -v /c/my-project/:/notebooks/ chchannn/ml-starter`
	
	On macOS it looks like `docker run -i -t -p 8888:8888 -v ~/my-project/:/notebooks/ chchannn/ml-starter`
	
5. Visit  `localhost:8888` to Login and use Jupyter Server
	
6. Default Jupyter Password is **ml-starter**

7. Optional - Change default memory
	
	`docker-machine stop`

	`VBoxManage modifyvm default --cpus 2`

	`VBoxManage modifyvm default --memory 4096`

	`docker-machine start`

