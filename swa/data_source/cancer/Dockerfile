
from python:3.7.8-buster
MAINTAINER kyoungwon

RUN apt-get update
RUN apt-get -y install libgl1-mesa-glx
RUN python -m pip install --upgrade pip
RUN pip install pika
RUN pip install numpy
RUN pip install opencv-python
COPY ./AI_Prediction_Service /workspace/AI_Prediction_Service
COPY ./start.sh /data/start.sh 
VOLUME ["/DATA"]
WORKDIR /workspace/AI_Prediction_Service

#CMD /data/start.sh 192.168.0.116 5672 1 50
#CMD /data/start.sh 192.168.0.120 5672 1 50
CMD /data/start.sh 10.106.43.10 5672 1 50
