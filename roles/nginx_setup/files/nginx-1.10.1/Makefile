
default:	build

clean:
	rm -rf Makefile objs

build:
	$(MAKE) -f objs/Makefile

install:
	$(MAKE) -f objs/Makefile install

modules:
	$(MAKE) -f objs/Makefile modules

upgrade:
	/usr/sbin/nginx -t

	kill -USR2 `cat /opt/cachingServer/--pid-path=/tmp/nginx.pid`
	sleep 1
	test -f /opt/cachingServer/--pid-path=/tmp/nginx.pid.oldbin

	kill -QUIT `cat /opt/cachingServer/--pid-path=/tmp/nginx.pid.oldbin`
