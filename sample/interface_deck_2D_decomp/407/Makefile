# Makefile for building final exe and cleaning directory

# name of platform to build for
PLAT = op
#PLAT = emt64

# path to installed compiler wrapper
#VPIC = /home/wohlbier/VPIC/407/vpic-407-src/build_intel_debug/build.${PLAT}
VPIC = /home/wohlbier/VPIC/407/vpic-407-src/build_intel_release_sse/build.${PLAT}
#VPIC = /home/wohlbier/VPIC/407/vpic-407-src/build_gcc_debug/build.${PLAT}
#VPIC = /home/wohlbier/VPIC/407/vpic-407-src/build_gcc_release_sse/build.${PLAT}

# name of input deck file
DECK = v407_interface_deck_2D_decomp.cc
# stripped deck
DECK_STRIP = `echo $(DECK) | sed 's,\.cxx,,g;s,\.cc,,g;s,\.cpp,,g'`

# compile final exe
all:
	$(VPIC) $(DECK)

# clean everything
clean:
	-$(RM) $(DECK_STRIP).$(PLAT)
	-$(RM) -rf ehydro
	-$(RM) -rf fft
	-$(RM) -rf field
	-$(RM) -rf global.vpc
	-$(RM) -rf I1hydro
	-$(RM) -rf I2hydro
	-$(RM) -rf particle
	-$(RM) -rf restart*
	-$(RM) -rf rundata
	-$(RM) -rf velocity
	-$(RM) *~
