CC  =  gcc
CFLAGS += -g -Wall -Wextra -w

NGX_ROOT = /home/suraj/Desktop/suraj/src/nginx-1.7

TARGETS = ngx_array_t_test
TARGET_C_FILE = $(TARGETS).c
CLEANUP = rm -f $(TARGETS) *.o

all: $(TARGETS)

clean:
	$(CLEANUP)


CORE_INCS = -I. \
-I../nginx_src/src/core \
-I../nginx_src/src/event \
-I../nginx_src/src/event/modules \
-I../nginx_src/src/os/unix \
-I../nginx_src/objs \


NGX_PALLOC =../nginx_src/objs/src/core/ngx_palloc.o
NGX_ARRAY=../nginx_src/objs/src/core/ngx_array.o
NGX_STRING =../nginx_src/objs/src/core/ngx_string.o
NGX_ALLOC =../nginx_src/objs/src/os/unix/ngx_alloc.o

$(TARGETS): $(TARGET_C_FILE)  $(OBJPATH)
	$(CC) $(CFLAGS) $(CORE_INCS) $(NGX_PALLOC) $(NGX_STRING) $(NGX_ALLOC) $(NGX_ARRAY) $^ -o $@ 
