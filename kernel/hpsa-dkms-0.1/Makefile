# net/can
# drives/net/can
export CONFIG_SCSI_HPSA          := m

SRC_DIRS :=  drivers/scsi
KVERSION := $(shell uname -r)

modules: $(SRC_DIRS)

$(SRC_DIRS):
	$(MAKE) -C /lib/modules/$(KVERSION)/build M="$(M)/$@" subdir-ccflags-y=-DCONFIG_CAN_CALC_BITTIMING

.PHONY: $(SRC_DIRS) modules
