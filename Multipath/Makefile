# Compiler
CC = gcc


# Source files
SRC = multipath_test.c  /home/jarvis/Desktop/picoquic/loglib/autoqlog.c 

# Output binary
PROJECT = multipath_testing

# Include paths (for header files)
INCLUDE_PATHS = -I. \
                -I/home/jarvis/Desktop/picotls/include \
				-I/home/jarvis/Desktop/picoquic/picoquictest \
				-I/home/jarvis/Desktop/picoquic/picoquic \
				-I/home/jarvis/Desktop/picoquic/loglib 

# Library paths (where the linker looks for libraries)
LIB_PATHS = -L/home/jarvis/Desktop/picoquic/_deps/picotls-build \
			-L/home/jarvis/Desktop/picoquic \
			-L/lib/x86_64-linux-gnu \
            -L/usr/lib

# Libraries to link against
LIBRARIES = -lpicoquic-core \
            -lpicoquic-log \
            -lpicotls-core \
            -lpicotls-fusion \
            -lpicotls-minicrypto \
            -lpicotls-openssl \
            -lssl \
            -lcrypto \
			-lpthread \
			-lX11

CFLAGS = -g -Og -O2 $(INCLUDE_PATHS)

# Linker flags
LDFLAGS = $(LIB_PATHS) $(LIBRARIES)


$(PROJECT) : $(SRC)
	$(CC) $(CFLAGS) $(SRC) $(LDFLAGS) -o $(PROJECT) 

# Clean up the built binary
clean:
	rm -f $(PROJECT)