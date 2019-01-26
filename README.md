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

export SPARK_HOME='/home/admin/spark-2.1.0-bin-hadoop2.7'
export PATH=$SPARK_HOME:$PATH
export PYTHONPATH=$SPARK_HOME/python:$PYTHONPATH

## GCloud Steps
http://inep.gov.br/microdados

https://cloud.google.com/dataproc/docs/tutorials/jupyter-notebook?hl=pt-br
2


wget http://download.inep.gov.br/microdados/microdados_enem2016.zip
Jupyter
- add gs://dataproc-initialization-actions/jupyter/jupyter.sh as initialization action
- create ssh conn
    gcloud compute ssh "cluster-tf-m" \
  --project project-id \
  --zone=cluster-zone \
  -- -D 10000 -N

gcloud compute ssh "cluster-tf-m" \
  --project neon-idiom-212518 \
  --zone=southamerica-east1-c \
  -- -D 10000 -N

- access through tunnel

/usr/bin/google-chrome-stable \
    "http://cluster-tf-m:8123" \
    --proxy-server="socks5://localhost:10000" \
    --host-resolver-rules="MAP * 0.0.0.0 , EXCLUDE localhost" \
    --user-data-dir=/tmp/


-? Added aksmiyazaki to sudoers
- sudo chown -R $USER /opt/conda
- conda install pandas
- conda install seaborn

master 2 vcpu, 50 disco ssd
slaves 6 com 1vcpuj, 100gb disco padrão


- 1 master com 2vCPU, 7,5GB de Memória e 200GB de disco, 2 workers com mesma config.


