 FROM ubuntu:22.04
 RUN apt-get update
 RUN apt-get install python3-pip -y
 RUN apt-get install docker.io -y
 RUN apt-get install git -y
 RUN apt-get install curl -y
 RUN apt-get install wget -y
 RUN wget https://github.com/mikefarah/yq/releases/latest/download/yq_linux_amd64 -O /usr/local/bin/yq && chmod +x /usr/local/bin/yq
 RUN rm -rf /etc/ssh && mkdir /etc/ssh
 EXPOSE 5000
 RUN rm -rf /usr/lib/python3.11/EXTERNALLY-MANAGED
 RUN pip install --no-cache-dir -r requirements.txt
 ENTRYPOINT ["flask", "run"]
 CMD ["--host=0.0.0.0"]