# JULE for Bats' Calls Clustering

[JULE](https://arxiv.org/pdf/1604.03628) (Joint Unsupervised Learning of Deep Representations and Image Clusters) in TensorFlow.

## File Structure
Main class:
	joint_cluster_cnn.py
	
Driver file:
	test.py

## Instructions 
The input directory, learning rate, number of epochs, number of nearest clusters, lambda could be changed in joint_cluster_cnn.py.

After adjusting the hyper-parameters, environment, and input directory path, run the following:

```
!export CUDA_VISIBLE_DEVICES=0 && source activate {environment name} && python test.py
```

Please run it on the high-RAM instance of Colab, or on a system with atleast 24GB system memory.
