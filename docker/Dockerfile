FROM python:3.7

RUN mkdir -p /usr/src/certificates
RUN git clone https://github.com/humburg/carpentries-certificates.git /usr/src/certificates

WORKDIR /usr/src/certificates
RUN git checkout docker
RUN pip install --no-cache-dir -r requirements.txt

ENTRYPOINT [ "python", "./bin/certificates.py" ]
CMD ["--help"]