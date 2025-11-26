FROM python:3.8-slim-bullseye

RUN apt-get update && apt-get install -y wget unzip ca-certificates \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app
COPY api /app

RUN pip3 install --no-cache-dir -r requirements.txt

RUN python3 -m nltk.downloader punkt punkt_tab averaged_perceptron_tagger brown

EXPOSE 5000
ENTRYPOINT ["python3"]
CMD ["logic_server.py"]
