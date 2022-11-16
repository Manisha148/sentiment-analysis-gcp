# syntax=docker/dockerfile:1

FROM python:3.8-slim-buster


WORKDIR /app

COPY . /app

RUN pip install notebook

RUN pip install bash_kernel && python -m bash_kernel.install

ENV DEFAULT_KERNEL_NAME "bash"

RUN pip install -r requirements.txt

EXPOSE 5000

CMD ["python3","app.py"]


