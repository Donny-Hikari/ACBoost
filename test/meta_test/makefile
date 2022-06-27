
ifeq ($(ACBOOST_ROOT),)
	ACBOOST_ROOT=../..
endif

scriptsdir=$(ACBOOST_ROOT)/scripts
entry=build/main

test:
	@$(scriptsdir)/test

run:
	@./$(entry) < "cases/$(N).in"

diff:
	@bash $(scriptsdir)/compare $(N)

lastnewline:
	@bash $(scriptsdir)/lastnewline
