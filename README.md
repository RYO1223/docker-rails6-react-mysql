



docker-compose run back rails new . --api --force --no-deps --database=mysql --skip-test


docker-compose build


config/database.yml
  username: <%= ENV['DB_USER'] %>
  password: <%= ENV['DB_PASSWORD'] %>
  host: db


docker-compose up -d
docker-compose exec db mysql -uroot -p -e"GRANT ALL PRIVILEGES ON *.* TO 'myapp'@'%';FLUSH PRIVILEGES;"

docker-compose run web rails db:create

docker-compose run --rm node sh -c "npm install -g create-react-app && create-react-app react-sample"
