# JAIST_AWS
introduction to how to use AWS through JAIST CLOUD

0.

1. 
 - ` sudo yum update `
 - CUDA sample test, comple [^1]
 - In a case you download cudnn() in Windows, you need to change its identify into arbitary one. [^2]

## Evironment and Spec.
- Amazon Linux AMI like Redhat distribution
- CPU Xeon E5-2686v4 (Broadwell) 1
- GPU p2
- mem 
- See more https://aws.amazon.com/jp/ec2/instance-types/


## (MEMO) For Our Favorite Dev. Setting


### For MY Favorite
- CUDA (already installed 7.5?)
- CuDNN(need to install in local and then pass through it to remote with matched version for 7.5)
  - `sudo su -`
  - We need to consider to install and expand cuDNN tgz in enough inode ().
  - 
- Conda
- Deep learning tool
  - Tensorflow, Chainer, Keras
  - Mxnet
  
  
  
## Note
- We need to check about specific version in GPU, to use it.
  - mount extended HDD
  - static IP

## Refe(jp)
- qiita
  - tf p2 (CUDA, CuDNN-From-scp)(miniconda, jupyter)(security group for jupyter needed? env,path?) https://qiita.com/hamaguchitm/items/269df3662a09f46277c7
    - (this aws linux ami does not work?  DON'T USE anaCONDA) https://qiita.com/halhorn/items/361008b19b4fcfd618d6
  - tf
    - (CuDNN acceralate calcu, DETAIL FILE MNG) https://qiita.com/h860a/items/294262d98e1223008252
  - anaconda+jupyter(don't use sec gr?) simple https://qiita.com/Salinger/items/c7b87d7000e48be6ebe2
    - this use? sec gr https://jp.ubunifu.co/python/jupyterhub-pyenv-anaconda%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%EF%BC%88aws-ec2%EF%BC%89
  - mxnet 
  - web
    - https://qiita.com/Arashi/items/629aaed33401b8f2265c


[^1]: https://qiita.com/daikumatan/items/26039fc23edabf76a9c4
[^2]: https://missingmemory.net/archives/416
