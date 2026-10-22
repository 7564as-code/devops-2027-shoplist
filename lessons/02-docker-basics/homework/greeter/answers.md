1.docker build -t greeter:v1 .
2.docker run -d --name greeter -p 9000:8000 greeter:v1
3.docker run -d --name greeter -p 9000:8000 -e GREETING=Shalom greeter:v1
4.shalom, Rivka
5. FROM, WORKDIR, ENV, COPY requirements.txt . ו-RUN pip install - cached
COPY . . ו-EXPOSE ו-CMD - ירוץ שוב
