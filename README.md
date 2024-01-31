FROM python:3.7
WORKDIR /app

RUN apt update
RUN apt install -y curl
# download certificate
RUN curl -sL https://netfree.link/dl/unix-ca.sh | sh
# pip config
RUN pip config set global.cert /usr/lib/ssl/certs/ca-certificates.crt

COPY . /app
RUN pip install -r requirements.txt
CMD ["python", "./convert_image_to_pdf.py"]