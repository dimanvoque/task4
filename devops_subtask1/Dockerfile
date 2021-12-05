FROM ubuntu:latest

RUN apt-get update -y && DEBIAN_FRONTEND=noninteractive apt-get install -y python3-pip python3-dev build-essential cmake && \
    pip3 install flask && \
    apt-get clean && apt-get autoremove && \
    useradd -s /bin/bash -m techproguser && mkdir /app && chown techproguser:techproguser /app

USER techproguser

COPY . /app
WORKDIR /app

RUN cmake . && make

CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0"]