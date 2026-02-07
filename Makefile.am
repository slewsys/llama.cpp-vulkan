# Makefile.am: Automake template for bash-dot-files.
#
# Process this file with automake to create Makefile.in
#
BUILD_DIR := $(dir $(realpath $(lastword $(MAKEFILE_LIST))))

bin_SCRIPTS = install-llama.cpp-vulkan
EXTRA_DIST = build-llama.cpp-vulkan.in \
	     install-asdf.in \
	     install-llama.cpp-vulkan.in \
	     install-vulkan-sdk.in

AM_DEFAULT_SOURCE_EXT = .in

.PHONY: all clean-local


all: llama.cpp-vulkan

llama.cpp-vulkan: build-llama.cpp-vulkan install-vulkan-sdk
	$(BUILD_DIR)install-vulkan-sdk
	$(BUILD_DIR)build-llama.cpp-vulkan $(abs_srcdir)

install: install-exec-local

install-exec-local: install-llama.cpp-vulkan
	$(BUILD_DIR)install-llama.cpp-vulkan

clean:
	rm -rf src

build-llama.cpp-vulkan: $(top_srcdir)/build-llama.cpp-vulkan.in

install-asdf: $(top_srcdir)/install-asdf.in

install-llama.cpp-vulkan: $(top_srcdir)/install-llama.cpp-vulkan.in

install-vulkan-sdk: $(top_srcdir)/install-vulkan-sdk.in
