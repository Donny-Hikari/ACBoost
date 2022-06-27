
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

create-test-projects:
	@ACBOOST_DIRPREFIX=test-projects . $(ACBOOST_ROOT)/acboost-create all_pass
	@ACBOOST_DIRPREFIX=test-projects . $(ACBOOST_ROOT)/acboost-create one_fail
	@cp src/all_pass.cpp test-projects/all_pass/src/all_pass.cpp
	@cp src/all_pass.cpp test-projects/one_fail/src/one_fail.cpp
	@touch test-projects/all_pass/cases/1.in
	@echo Pass >test-projects/all_pass/cases/1.out
	@touch test-projects/all_pass/cases/2.in
	@echo Pass >test-projects/all_pass/cases/2.out
	@touch test-projects/one_fail/cases/1.in
	@echo Pass >test-projects/one_fail/cases/1.out
	@touch test-projects/one_fail/cases/2.in
	@echo Fail >test-projects/one_fail/cases/2.out
