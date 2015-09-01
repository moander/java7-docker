TYPES := $(shell echo */)

.PHONY: all build tag push

all: build tag push

build tag push:
	@set -x && $(foreach type,$(TYPES), $(MAKE) -C $(type) $(MFLAGS) $@;)
