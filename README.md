# README

## Traditional deployment

Database configuration using `rails-env`:

    # .env.development
    POSTGRES_USER=rails
    POSTGRES_PASSWORD=rails

Now init the DB:

    rake db:create
    bin/rails db:migrate RAILS_ENV=development
    bin/rails db:migrate

    rails s -b 0.0.0.0


Production:

    POSTGRES_USER=rails POSTGRES_PASSWORD=rails RAILS_ENV=production rake db:setup
    rake assets:precompile
    POSTGRES_USER=rails POSTGRES_PASSWORD=rails RAILS_ENV=production rails s -b 0.0.0.0

## ...