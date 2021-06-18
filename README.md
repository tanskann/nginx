# nginx

From time to time, I need a dummy container that would respond to HTTP requests. This container answers to that need. It serves `/` and `/api/v1/ping` endpoints and listens to port `8080`. Further modifications are possible by modifying the `default.conf` and rebuilding the container.

## Why not have PORT as env variable?

Simplicity. I just need this to run without any fancy scripts or variables, I don't want to configure it when it's running. Keep it simple!

## How does this work

`docker build . -t your-registry/your-container:your-tag && docker push your-registry/your-container:your-tag`
