FROM python:3.8
ENV ENV_VERS_OKD=4.8.0-0.okd-2021-10-01-221835
ENV TZ=Europe/Moscow
RUN  wget https://mirror.openshift.com/pub/openshift-v4/clients/oc/latest/linux/oc.tar.gz -O /tmp/oc.tar.gz &&\
    tar -zxvf /tmp/oc.tar.gz --exclude='*.md' -C /usr/bin/ &&\
    rm -rf /tmp/oc.tar.gz
ADD . /opt/app
WORKDIR /opt/app
RUN pip install -r requirements.txt
RUN  ./oc.sh
CMD [ "python", "main.py" ]
EXPOSE 80
