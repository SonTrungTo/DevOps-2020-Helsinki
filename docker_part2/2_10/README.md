## Explanations

This exercise is the inverse thought process of [2.8](https://github.com/SonTrungTo/DevOps-2020-Helsinki/tree/master/docker_part2/2_8)

The key here is these lines of codes in the [backend](https://github.com/docker-hy/backend-example-docker/blob/master/server/index.js#L69-L73)

In 2.8, the request of `/api/ping` was actually sent to backend as `/ping` thanks to the configs made to the reverse proxy
by adding `/` to the `proxy_pass` url.

Conversely, in 2.10, the request of `/api/ping` is sent to backend as `/ping` because of the lack of forward slash `/` to
the `proxy_pass` url, consequently making the proxy made the request as `/ping`, and this is possible because of `/api*`
route in the backend.