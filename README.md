# nginx with modsecurity + OWASP crs + rate limiting

Dockerized nginx + modsecurity with OWASP coreruleset and rate limiting enabled.

Uses [coreruleset/modsecurity-crs-docker](https://github.com/coreruleset/modsecurity-crs-docker) as base docker image.

- `default.conf` is mounted as a docker volume to `/etc/nginx/conf.d/default.conf`. (It is to be merged with existing nginx configuration)
- We can fine tune the rules and WAF protection settings via the variables in `.env`.
- We can disable certian rules or patterns from the WAF by editing the `REQUEST-x.conf` and `RESPONSE-x.conf` files.