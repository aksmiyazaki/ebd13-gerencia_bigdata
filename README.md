# EBD13 - Data Management and Cloud Computing

Anotações sobre coisas relacionadas ao deploy do Hadoop.

##Comandos

Conectar a amazon:

ssh -i aksmiyazaki-home-keypair.pem admin@ec2-18-228-155-18.sa-east-1.compute.amazonaws.com

SPARK_LOCAL_IP=127.0.0.1 \
SPARK_MASTER_HOST=172.31.12.136 \
$HOME/spark-2.1.0-bin-hadoop2.7/sbin/start-master.sh


## Notes

sha1:ce571e696b25:c6d7626c29432d5c5d5e38f0c335d4470c14f37e

export ANACONDA_ROOT=~/anaconda2
export PYSPARK_DRIVER_PYTHON=$ANACONDA_ROOT/bin/ipython
export PYSPARK_PYTHON=$ANACONDA_ROOT/bin/python

SPARK_HOME='/home/admin/spark-2.1.0-bin-hadoop2.7'
PATH=$SPARK_HOME:$PATH
PYTHONPATH=$SPARK_HOME/python:$PYTHONPATH