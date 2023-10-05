 FROM debian:12.1
 #<design-your-own>
 RUN apt update
 RUN apt install python3-pip -y
 WORKDIR /app
 COPY . .
 RUN rm -rf /usr/lib/python3.11/EXTERNALLY-MANAGED
 RUN pip install --no-cache-dir -r requirements.txt
 EXPOSE 5000
 ENTRYPOINT ["flask", "run"]
 CMD ["--host=0.0.0.0"]
