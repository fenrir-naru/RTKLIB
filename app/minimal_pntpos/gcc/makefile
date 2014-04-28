# makefile for rtkrcv

PACKAGE = minimal_pntpos.exe

BIN_PATH = /usr/bin:/usr/local/bin
CXX = gcc
CPPFLAGS = -DWITHOUT_FILE -DWITHOUT_THREAD -DWITHOUT_SYSTIME -DTRACE
#-DENAGLO -DENAGAL -DENAQZS -DNFREQ=3
#-mfpu=neon -mfloat-abi=softfp -ffast-math #for beaglebone
CFLAGS = $(CPPFLAGS) #-Wall -O3 -ansi -pedantic
LFLAGS =  
ORIG_SRC_DIR = ../../../src/
INCLUDES = -I$(ORIG_SRC_DIR)
LIBS = -lm #-L
BUILD_DIR = build_GCC

SRCS_ORIG = rtkcmn.c ephemeris.c pntpos.c sbas.c ionex.c preceph.c
SRCS = ../minimal_pntpos.c $(patsubst %,$(ORIG_SRC_DIR)%,$(SRCS_ORIG))
OBJS = $(patsubst %.c,%.o,$(notdir $(SRCS)))

all : $(BUILD_DIR) $(PACKAGE)

# ヘッダーファイルの依存関係 @see http://lists.gnu.org/archive/html/automake/2002-01/msg00155.html
$(BUILD_DIR)/depend.inc: $(BUILD_DIR) makefile
	for i in $(SRCS); do \
		$(CXX) -E -MM $(INCLUDES) $(CPPFLAGS) $$i >> tempfile; \
		if ! [ $$? = 0 ]; then \
			rm -f tempfile; \
			exit 1; \
		fi; \
	done; \
	cat tempfile | sed -e 's/^+.*//g' -e 's/[^\.]*\.o/$(BUILD_DIR)\/&/g' > $@; \
	rm -f tempfile

-include $(BUILD_DIR)/depend.inc

$(BUILD_DIR)/%.o :
	$(CXX) -c $(CFLAGS) $(INCLUDES) -o $@ $(findstring $<,$^)

$(PACKAGE) : $(patsubst %,$(BUILD_DIR)/%,$(PACKAGE))

$(BUILD_DIR)/$(PACKAGE) : $(patsubst %,$(BUILD_DIR)/%,$(OBJS))
	$(CXX) $(LFLAGS) $(INCLUDES) -o $@ $^ $(LIBS);

$(BUILD_DIR) :
	mkdir $@

clean :
	rm -f $(BUILD_DIR)/*

run : all

.PHONY : clean all

