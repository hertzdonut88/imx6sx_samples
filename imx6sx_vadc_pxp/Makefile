CC ?=$(CROSS_COMPILE)gcc
CFLAGS ?= -O2 -Wall -Wstrict-prototypes -Wno-trigraphs -fno-strict-aliasing -fno-common

INCLUDES +=  

LFLAGS +=  
LIBS = -lpxp -lpthread 

SOURCES=imx6sx_vadc_pxp.c
OBJECTS=$(SOURCES:.c=.o)
EXECUTABLE=imx6sx_vdac_pxp

all: $(SOURCES) $(EXECUTABLE)
    
$(EXECUTABLE): $(OBJECTS) 
	$(CC) $(OBJECTS) -o $@ $(LDFLAGS) $(LIBS) 

.c:
	$(CC) $(CFLAGS) $(INCLUDES) $< -o $@ 

clean:
	$(RM) *.o *~ $(EXECUTABLE)
