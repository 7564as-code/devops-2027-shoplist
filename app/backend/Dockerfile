FROM python:3.11-slim

COPY netfree.crt /usr/local/share/ca-certificates/netfree.crt
RUN cat /usr/local/share/ca-certificates/netfree.crt >> /etc/ssl/certs/ca-certificates.crt

ENV PIP_CERT=/etc/ssl/certs/ca-certificates.crt
ENV REQUESTS_CA_BUNDLE=/etc/ssl/certs/ca-certificates.crt
ENV SSL_CERT_FILE=/etc/ssl/certs/ca-certificates.crt

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY app.py .

EXPOSE 5000

CMD ["python", "app.py"]