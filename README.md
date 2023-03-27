# Demonstration for [cloudflare/workers-sdk#2950](https://github.com/cloudflare/workers-sdk/issues/2950)

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/grimsteel/cf-pages-routes-proxy-not-respected)

1. Run `npm run dev` to start serving the pages application using the proxy server

2. Go to any URL on the server, and notice that the middleware function was invoked, even though _routes.json only includes /api*

3. Stop the server and run `npm run dev:no-proxy`

4. Go to / on the server and notice that the middleware function is not invoked. Go to any URL under /api and notice that it is invoked. This is the expected behavior