default: help
.PHONY: default

help:
	@echo 'Usage:'
	@echo '	$$ make [action]'
	@echo
	@echo 'Example:'
	@echo '	$$ make'
	@echo '	$$ make help'
	@echo
	@echo '	$$ make fedora-prepare'
	@echo
	@echo '	$$ make manjaro-prepare'
	@echo
	@echo '	$$ make ubuntu-prepare'
	@echo
	@echo '	$$ make rc'
	@echo
	@echo '	$$ make view'
	@echo
	@echo '	$$ make install'
	@echo
	@echo '	$$ make test'
	@echo
	@echo '	$$ make sync'
	@echo

.PHONY: help


fedora-prepare:
	sudo dnf install php
.PHONY: fedora-prepare


manjaro-prepare:
	sudo pacman -Sy --needed php
.PHONY: manjaro-prepare


ubuntu-prepare:
	sudo apt-get install php-cli
.PHONY: ubuntu-prepare


rc:
	php config.conf > config
.PHONY: rc


view:
	cat config | less
.PHONY: view


install: rc
	install -Dm644 config ~/.config/i3/config
.PHONY: install


test:
	echo "Todo: test"
.PHONY: test


sync: rc
	install -Dm644 config ../../../../config
.PHONY: sync
