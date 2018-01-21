# JAIST_AWS

(*Uncompleted document in some ones, so please wait a minute*)

Introduction to how to use AWS Ec2 instance through JAIST CLOUD

ISC provides kindly these with purpose to acceralate our research and to have us acquire sophisticated information processing skill on educational scenario. (We can use  freely but) Note that we should notice we have a duty to avoid **"over-use"** when we use it any time because resource cost...  (when you take a rest (e.g go to bed, have a food and so on...), computer also hope to do that :sleeping:)

We suggest definitive standard time for switch-off as 1 day, it means we switch off if we do not use over 1 day a last use (e.g. attend to conference, take a trip etc...)
 
------------------------
0. Intro

1. Env
2.
3. Setting basic environment

------------
 - ` sudo yum update `
 - CUDA sample test, comple [^1]
 - In a case you download cudnn in Windows, you need to change its identifier into arbitary one. [^2]

## Evironment and Spec.
- Amazon Linux AMI like Redhat distribution, p2 EC2
- CPU Xeon E5-2686v4 (Broadwell) *4
- GPU NVIDIA K80 *1
- mem 61?(GiB) (CPU), 12(GiB) (GPU)
- See more jp site here https://aws.amazon.com/jp/ec2/instance-types/ ,

## (Memo) For Our Favorite Dev. Setting
- For general document of how to use on JCS, we can view [here(en)](http://www.jaist.ac.jp/iscenter/en/jaist-cloud/cloud/guidebook/), [here(jp)](http://www.jaist.ac.jp/iscenter/fileadmin/Contents/Top-Page/Cloud/Cloud-Service/JAISTCloudService-ja.pdf)

- import .pem file (certificate)
- login
- mount in my dir
- *chmod filesystem(mounted directory)*, *chown?* (which proper to permission)
  - /etc/??? (vi edit ___ ) to fix mnt after switching-off
- cuda   /.bash_proofile ==> note that data position,,,, after that, relogin to active roader it
- ()cuDNN (note that data position,,,, scp)

- pyenv **in data** ~ miniconda ~ 
- conda **config to data** http://nekoyukimmm.hatenablog.com/entry/2016/03/27/173030
- tf (sample code to check work on gpu)
- ()jy port

### For MY Favorite
- CUDA (already installed 7.5)
- CuDNN(need to download in local and then pass through it to remote with matched version for 7.5) 6.0
  - `sudo su -`
  - We need to consider to install and expand cuDNN tgz in enough inode (valume) file.
  - 
- Conda
- Deep learning tools
  - Tensorflow, Chainer, Keras
  - Mxnet
  - Spyder (remote)
  - (Atom, hidrogen? conda, jupyter, IDE)
  - **Jupyter remote, lab, theme**
    - jupyter lab, and color (font "Recty Dimished"). (extension is under the development) (Nodejs kernel still not)
  
  
  
## Note (unsolved issues)
- We need to check about specific version in GPU, to use it.
  - ~mount extended HDD~
    - ***inode issue (how can we resolve it? uses xft? ext4(how can check), root?user? => can file mnt folder or expand inodes?)***
  - ~static IP~(fixed initially by defalt in Jaist setting)
  - In RHEL(or CentOS)-like AWS Linux, any equivalent for libcupti-dev library: https://stackoverflow.com/questions/45348033/tensorflow-installation-on-centos7-libcupti-dev-equivalent , rpm   ===> **Hint: libcupti	/usr/local/cuda-8.0/extras/CUPTI/lib64**

## Plan
- Making sample code, data analysis, deep learning (but mainly around my theme... see more memo)
- 
- Docker

## Refe(almost jp)
- qiita
  - tf p2 (CUDA, CuDNN-From-scp)(miniconda, jupyter)(security group for jupyter needed? env,path?) **https://qiita.com/hamaguchitm/items/269df3662a09f46277c7**
    - (this aws linux ami does not work?  DON'T USE anaCONDA) https://qiita.com/halhorn/items/361008b19b4fcfd618d6
  - tf
    - (CuDNN acceralate calcu, DETAIL FILE MNG) **https://qiita.com/h860a/items/294262d98e1223008252**
  - anaconda+jupyter(don't use sec gr?) simple https://qiita.com/Salinger/items/c7b87d7000e48be6ebe2
    - this use? sec gr https://jp.ubunifu.co/python/jupyterhub-pyenv-anaconda%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%EF%BC%88aws-ec2%EF%BC%89
  - mxnet 
  - web
    - https://qiita.com/Arashi/items/629aaed33401b8f2265c


[^1]: https://qiita.com/daikumatan/items/26039fc23edabf76a9c4
[^2]: https://missingmemory.net/archives/416



