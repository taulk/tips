# Web.py deploy with nginx+gunicorn

[Ref](http://webpy.readthedocs.org/en/latest/deploying.html)

Edit the main.py
```
import web
...
app = web.application(urls, globals())

# get the wsgi app from web.py application object
wsgiapp = app.wsgifunc()
```

start gunicorn server

```
gunicorn -w 4 -b 127.0.0.1:4000 yourapp:wsgiapp
```

nginx config

```
server {
  listen 80;
  server_name example.org;
  access_log  /var/log/nginx/example.log;

  location / {
      proxy_pass http://127.0.0.1:4000;

      proxy_set_header Host $host;
      proxy_set_header X-Real-IP $remote_addr;
      proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
  }
}
```
