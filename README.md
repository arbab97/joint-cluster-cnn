
		Please run it on the high-RAM instance of Colab, or on a system with atleast 24GB system memory.
# JULE 
TensorFlow Implementation of https://arxiv.org/pdf/1604.03628 for bats calls clustering

### Setup and Model Train
* Use `joint_cluster_cnn.py` to configure the  learning rate, number of epochs, number of nearest clusters, lambda and input directory (line 19). 
* `test.py` contains the drive code to run the `join_cluster_cnn.py`. 
* After the setup, run model using the command: `export CUDA_VISIBLE_DEVICES=0 && source activate {environment name} && python test.py`

### Running via Notebook on Google Colab (`JULE.ipynb`)
A notebook has already been setup which will fetch the required data, install all the required packages, fetch the code, run the algorithm and output results in a `csv` format. The details are given below:
* Install miniconda to setup the environmen later.
* Clone the code from github repository. Or the code folder (provided) could also be uploaded manually in the notebook directory. 
* Connect to Google Drive and copy all the required data which needs to be clustered. You can also upload the data manually. Another way include using `gdown` with shared link of data. 
* Create new environment using `conda env create -f jule_tensorflow_3.yml`. Then install the compatible `tensorflow 1.3.0` package using `conda install -c anaconda tensorflow-gpu=1.3.0`. Alternatively, you can also use the provided `requirements_jule.yml` file to setup the new environment using : `conda env create -f 'requirements_[algo].yml'`.
* Create a new log file manually that'll be used by the model to save the log. 
Use `mkdir /content/joint-cluster-cnn/logfile` and then 
`touch /content/joint-cluster-cnn/logfile/logfile.log`
* Finally, run the model using the command given above. In notebook it is:  `export CUDA_VISIBLE_DEVICES=0 && source activate jule_tensorlfow_3 && python test.py`
* The output is provided in `csv` format in the file: `results_jule.csv`


### Citation
This Algorithms is taken from:
```bibtex
@inproceedings{yang2016joint,
  title={Joint unsupervised learning of deep representations and image clusters},
  author={Yang, Jianwei and Parikh, Devi and Batra, Dhruv},
  booktitle={Proceedings of the IEEE conference on computer vision and pattern recognition},
  pages={5147--5156},
  year={2016}
}
```
