CFLAGS = -Wall -Werror -Wextra -g

build: clean
	${CC} ${CFLAGS} -shared -o build/hash_table.so -fPIC src/hash_table.c src/xmalloc.c src/prime.c

build-test: clean
	${CC} ${CFLAGS} -o build/test_hash_table src/hash_table.c tests/test_hash_table.c src/xmalloc.c src/prime.c
	${CC} ${CFLAGS} -o build/test_primes tests/test_primes.c src/prime.c

clean:
	rm -rf build/
	mkdir -p build/

test: build-test 
	./build/test_hash_table
	./build/test_primes
