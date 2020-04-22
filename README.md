# RoR Chat


### local dev.
3 containers -> redis, postgres, ror6 + unicorn

```
docker build -t ror6dev .
docker-compose run -p8080:8010 --user "$(id -u):$(id -g)" ror6 bash
  bundle install
  rails db:setup
  rails db:migrate
  bundle exec unicorn -c config/unicorn.rb

```
http://<IP>:8080