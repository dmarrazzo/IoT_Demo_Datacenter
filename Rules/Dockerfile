FROM    psteiner/base

MAINTAINER psteiner <psteiner@redhat.com>

USER root

ENV APPL rules-jar-with-dependencies.jar

# transfer install-script
ADD Docker_Files/scripts/run.sh $HOME/

# make 'psteiner' the owner
RUN chown -R psteiner:psteiner $HOME/run.sh 

# switch to psteiner
USER psteiner

WORKDIR $HOME/tmp

CMD $HOME/run.sh



# Build command -> docker build --rm -t workspace_iotdatacentermonitor .
# run command -> docker run -h iotcontrollerrouter -d workspacefuse_iotdatacentermonitor
# run and connect -> docker run -P -i -t -h iotdatacentermonitor workspacefuse_iotdatacentermonitor /bin/bash
