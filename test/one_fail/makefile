
ifeq ($(ACBOOST_ROOT),)
	ACBOOST_ROOT=../..
endif

scriptsdir=$(ACBOOST_ROOT)/scripts
entry=build/main

test: build
	@bash $(scriptsdir)/test

build: src/*.cpp
	g++ -o $(entry) src/*.cpp --std=c++11

run: build
	@./$(entry) < "cases/$(N).in"

diff:
	@bash $(scriptsdir)/compare $(N)

lastnewline:
	@bash $(scriptsdir)/lastnewline

clean:
	@rm $(entry)
