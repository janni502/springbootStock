# springbootStock
Assignment

## Usage

Set up the database and user access:
    - create database db_example
    - create user 'springuser'@'%' identified by 'ThePassword'
    - grant all on db_example.* to 'springuser'@'%';

    - mvn clean package
    - mvn clean install
    - docker-compose up -d

    - curl -F "file=@dow_jones_index.data" -H "X-Client_Id: abc123" http://127.0.0.1:8080/api/stock-data/bulk-insert 
    - curl -H "X-Client_Id: abc123" http://127.0.0.1:8080/api/stock-data/AA
    - curl -H "Content-Type: application/json" -H "X-Client_Id: abc123" -X POST -d @dow_jones_missing.json http://127.0.0.1:8080/api/stock-data/
