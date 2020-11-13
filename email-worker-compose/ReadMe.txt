docker-compose up -d --scale worker=3

docker-compose logs -f -t

docker-compose exec db psql -U postgres -d email_sender -c "select * from emails"

docker-compose down -v