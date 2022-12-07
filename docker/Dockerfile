FROM registry.redhat.io/devspaces/udi-rhel8:3.2-26.1666711967

RUN cd /tmp && wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh && \
   chmod +x /tmp/Miniconda3-latest-Linux-x86_64.sh && \
   /tmp/Miniconda3-latest-Linux-x86_64.sh -b -p $HOME/miniconda && \
   $HOME/miniconda/bin/conda init

RUN /home/user/miniconda/bin/conda install --name base pylint -y

RUN chgrp -R 0 /home && \
    chmod -R g=u /etc/passwd /etc/group /home
    