CFLAGS = -Wall -g
OBJ_DIR = ../output            

SRCS = ../Demo/Demo_Sample.c
OBJS = $(SRCS:.c=.o)
TARGET = ../output/Demo_Sample
#LIBS = -lyour_library_name     #Link *.a

CHIP_MODEL = Hi3519DV500_010

ifeq ($(CHIP_MODEL), Hi3519DV500_010)
        CC = aarch64-v01c01-linux-gnu-gcc
	INCLUDES = -I../third_lib/Hi3519DV500_010/extdrv -I../third_lib/Hi3519DV500_010/include
	LDFLAGS = -L../third_lib/Hi3519DV500_010/lib
endif

ifeq ($(CHIP_MODEL), SS928V100_022)
	CC = aarch64-mix210-linux-gcc
	INCLUDES = -I../third_lib/SS928V100_022/extdrv -I../third_lib/SS928V100_022/include
	LDFLAGS = -L../third_lib/SS928V100_022/lib
endif



all: $(TARGET)

$(TARGET): $(OBJS)
	$(CC) $(CFLAGS) $(OBJS) $(LDFLAGS) $(LIBS) -o $(TARGET)

%.o: %.c
	$(CC) $(CFLAGS) $(INCLUDES) -c $< -o $@

clean:
	rm -f $(OBJS) $(TARGET)
