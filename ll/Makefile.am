
lib_LTLIBRARIES = libll.la

libll_la_SOURCES = \
			 ll.c \
			 ll.h

libll_la_LIBADD = ../log/liblog.la

bin_PROGRAMS = ll_test

ll_test_LDADD= ../wrap/libwrap.la libll.la -lpthread
ll_test_SOURCES = ll_test.c
