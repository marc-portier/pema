Bootstrap: docker
####From: hariszaf/pema:27_08_19_javas
From: hariszaf/pema:v2

%post
export WORKDIR="/home"
echo "export WORKDIR=$WORKDIR" >> $SINGULARITY_ENVIRONMENT
mkdir -p $WORKDIR

#echo "export PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/home/tools/BDS/.bds" >> $SINGULARITY_ENVIRONMENT 

echo "export PATH=/usr/lib/jvm/java-8-openjdk-amd64/bin:/usr/lib/jvm/java-11-openjdk-amd64/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/home/tools/BDS/.bds" >> $SINGULARITY_ENVIRONMENT 

echo "export PATH=$PATH:/bin/gzip" >> ~/.bashrc 


%runscript
/home/tools/BDS/.bds/bds /home/PEMA_v1.bds
