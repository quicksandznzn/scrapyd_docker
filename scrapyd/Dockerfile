FROM python:3.6-slim
ADD .. /src/scrapyd
WORKDIR /src/scrapyd
COPY scrapyd.conf /etc/scrapyd/
EXPOSE 6800
RUN apt-get update && apt-get install -y gcc
RUN pip --no-cache-dir --default-timeout=1000 install  -r requirements.txt -i https://pypi.douban.com/simple/
CMD scrapyd