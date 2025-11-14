# Makefile.am: Automake template for bash-dot-files.
#
# Process this file with automake to create Makefile.in
#
BUILD_DIR := $(dir $(realpath $(lastword $(MAKEFILE_LIST))))

bin_SCRIPTS = install-llama.cpp-rocm
EXTRA_DIST = build-llama.cpp-rocm.in \
	     install-asdf.in \
	     install-intel-oneapi-hpc.in \
	     install-llama.cpp-rocm.in \
	     install-nvidia-rocm.in

AM_DEFAULT_SOURCE_EXT = .in

.PHONY: all clean-local


all: llama.cpp-rocm

llama.cpp-rocm: build-llama.cpp-rocm
	$(BUILD_DIR)build-llama.cpp-rocm $(abs_srcdir)

install: install-exec-local

install-exec-local: install-llama.cpp-rocm
	$(BUILD_DIR)install-llama.cpp-rocm

clean:
	rm -rf llama.cpp

build-llama.cpp-rocm: build-llama.cpp-rocm.in

install-asdf: install-asdf.in

install-llama.cpp-rocm: install-llama.cpp-rocm.in

install-intel-oneapi-hpc: install-intel-oneapi-hpc.in

install-nvidia-rocm: install-nvidia-rocm.in
