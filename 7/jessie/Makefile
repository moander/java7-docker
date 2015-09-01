NAME	:= moander/java7
TAGS	:= latest jessie jessie-7u79 7u79
DOCKER	:= docker
BTAG	:= $(firstword $(TAGS))

.PHONY: all build tag push

all: build tag push

build:
	$(DOCKER) build -t $(NAME):$(BTAG) .

tag:
	@set -x && $(foreach tag,$(TAGS), $(DOCKER) tag -f $(NAME):$(BTAG) $(NAME):$(tag);)

push: tag
	@set -x && $(foreach tag,$(TAGS), $(DOCKER) push $(NAME):$(tag);)
