UK_ROOT ?= $(PWD)/workdir/unikraft
UK_BUILD ?= $(PWD)/workdir/build
UK_APP ?= $(PWD)
LIBS_BASE = $(PWD)/workdir/libs
UK_LIBS ?= $(LIBS_BASE)/musl:$(LIBS_BASE)/lwip:$(LIBS_BASE)/python3:$(LIBS_BASE)/compiler-rt

.PHONY: all

all:
	@$(MAKE) -C $(UK_ROOT) L=$(UK_LIBS) A=$(UK_APP) O=$(UK_BUILD)

$(MAKECMDGOALS):
	@$(MAKE) -C $(UK_ROOT) L=$(UK_LIBS) A=$(UK_APP) O=$(UK_BUILD) $(MAKECMDGOALS)
