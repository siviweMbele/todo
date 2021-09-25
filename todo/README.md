# Build
mvn clean package && docker build -t co.za.entelect/todo .

# RUN

docker rm -f todo || true && docker run -d -p 8080:8080 -p 4848:4848 --name todo co.za.entelect/todo 