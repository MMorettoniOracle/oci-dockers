# Set the base image to Oracle Linux 7 - Slim
FROM oraclelinux:7.9
FROM python:3

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
COPY . .

CMD [ "python", "./oci/Python/demo.py" ]

#DEBUG
RUN echo $(ansible-galaxy collection install oracle.oci)
RUN echo $(ansible --version)
RUN echo $(ansible-playbook oci/ansible/sample.yaml)

