FROM python:3

# mlperf-loggin will be mounted
# submission directory will be mounted

COPY requirements.txt /requirements.txt

RUN apt update && apt-get install -y apt-utils apt-transport-https ca-certificates gnupg2 git && pip install --upgrade pip && pip install pep8 autopep8 pylint pylint-django[with_django] rope && pip install -r /requirements.txt

RUN useradd -r -m -u 28595 -g 30 aprodromou

USER aprodromou
USER 28595:30

CMD [ "bash" ]
