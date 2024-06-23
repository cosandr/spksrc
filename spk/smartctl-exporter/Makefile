SPK_NAME = smartctl-exporter
SPK_VERS = 0.12.0
SPK_REV = 1
SPK_ICON = src/smartctl-exporter.png

DEPENDS = cross/smartmontools cross/$(SPK_NAME)

UNSUPPORTED_ARCHS = $(PPC_ARCHS)

MAINTAINER = cosandr
DESCRIPTION = Export smartctl statistics to prometheus.
STARTABLE = yes
DISPLAY_NAME = Smartctl Exporter
CHANGELOG = "1. Initial release."

HOMEPAGE = https://github.com/prometheus-community/smartctl_exporter
LICENSE  = Apache License 2.0

ADMIN_PORT = 9633
FWPORTS = src/smartctl-exporter.sc

SERVICE_SETUP = src/service-setup.sh

POST_STRIP_TARGET = smartctl-exporter_extra_install

include ../../mk/spksrc.spk.mk

.PHONY: smartctl-exporter_extra_install
smartctl-exporter_extra_install:
	@install -m 755 src/smartctl-ata $(STAGING_DIR)/bin/
	@install -m 755 -d $(STAGING_DIR)/var
	@install -m 644 src/parameters.txt $(STAGING_DIR)/var/
