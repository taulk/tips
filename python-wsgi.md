# Python WSGI

[Ref](http://ksnowlv.github.io/blog/2014/08/10/python-wsgi-da-jian-web-server/)

## Add hello.py

```
def application(environ, start_response):
  start_response('200 OK', [('Content-Type', 'text/html')])
  return '<h1>Hello, %s!</h1>' % (environ['PATH_INFO'][1:] or 'web')
```

## Add http_server.py

```
from wsgiref.simple_server import make_server

from hello import application

httpd = make_server('', 8000, application)
print 'Serving HTTP on port 8000...'

httpd.serve_forever()
```

## Serve

```
python http_server.py
```
