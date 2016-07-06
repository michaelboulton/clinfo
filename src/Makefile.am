AUTOMAKE_OPTIONS = foreign

CFLAGS=-std=c99 -g -Wall -Wextra -pedantic
LDLIBS=-lOpenCL

include_HEADERS = error.h ext.h memory.h strbuf.h

bin_PROGRAMS = clinfo
clinfo_SOURCES = clinfo.c

AM_LDFLAGS = -ldl
