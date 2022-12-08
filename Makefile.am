ACLOCAL_AMFLAGS=-I m4
lib_LTLIBRARIES = libinterflop_checkdenormal.la

libinterflop_checkdenormal_la_SOURCES = \
    interflop_checkdenormal.cxx \
    @INTERFLOP_STDLIB_PATH@/include/interflop-stdlib/iostream/logger.c 

libinterflop_checkdenormal_la_CFLAGS = \
    -DBACKEND_HEADER="interflop_checkdenormal" \
    -I@INTERFLOP_STDLIB_PATH@/include/ \
    -fno-stack-protector
libinterflop_checkdenormal_la_CXXFLAGS = \
    -DBACKEND_HEADER="interflop_checkdenormal" \
    -I@INTERFLOP_STDLIB_PATH@/include/ \
    -fno-stack-protector

if WALL_CFLAGS
libinterflop_checkdenormal_la_CFLAGS += -Wall -Wextra -Wno-varargs -Og -g
endif
if LINK_INTERFLOP_STDLIB
libinterflop_checkdenormal_la_LIBADD = @INTERFLOP_STDLIB_PATH@/lib/libinterflop_stdlib.la
endif
libinterflop_checkdenormal_la_includedir = $(includedir)/
include_HEADERS = interflop_checkdenormal.h