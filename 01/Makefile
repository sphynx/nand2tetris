HS = HardwareSimulator.sh

CHIPS = $(wildcard *.hdl)
TESTS = $(patsubst %.hdl,%.tst,$(CHIPS))
OUTS = $(patsubst %.hdl,%.out,$(CHIPS))
ALL = $(patsubst %.hdl,%,$(CHIPS))

all: $(ALL)

%.out: %.tst
	$(HS) $<

.PHONY: clean

clean:
	$(RM) *.out

%:	%.tst
	$(HS) $<
