all: dummy_plugin.so

dummy_plugin.so: dummy_plugin.c
	gcc -g -Werror -D _GNU_SOURCE -Wall -shared -nostartfiles dummy_plugin.c -o dummy_plugin.so -iquote ../../../criu/include -iquote ../../criu/include -fPIC

clean:
	rm dummy_plugin.so

install:
	mkdir -p /var/lib/criu && cp dummy_plugin.so /var/lib/criu/

uninstall:
	rm /var/lib/criu/dummy_plugin.so

