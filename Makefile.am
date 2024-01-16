AM_CFLAGS = -Wundef \
            -I${top_srcdir}/include \
            -I${top_srcdir}/sysdeps/include

ACLOCAL_AMFLAGS = -I m4

# create libufdt_sysdeps.a and libufdt.a
lib_LIBRARIES := \
    libufdt_sysdeps.a \
    libufdt.a

libufdt_sysdeps_a_SOURCES := \
    ${top_srcdir}/sysdeps/libufdt_sysdeps_posix.c

libufdt_sysdeps_a_LDFLAGS = -Wall -Werror

libufdt_a_SOURCES :=  \
    ufdt_overlay.c \
    ufdt_convert.c \
    ufdt_node.c \
    ufdt_node_pool.c \
    ufdt_prop_dict.c

libufdt_a_LDFLAGS = -Wall -Werror -lfdt

bin_PROGRAMS = mkdtimg

mkdtimg_SOURCES := \
    ${top_srcdir}/utils/src/mkdtimg.c \
    ${top_srcdir}/utils/src/mkdtimg_cfg_create.c \
    ${top_srcdir}/utils/src/mkdtimg_core.c \
    ${top_srcdir}/utils/src/mkdtimg_create.c \
    ${top_srcdir}/utils/src/mkdtimg_dump.c \
    ${top_srcdir}/utils/src/dt_table.c

mkdtimg_LDFLAGS = -Wall -Werror -lfdt

mkdtimg_LDADD = ${top_builddir}/libufdt_sysdeps.a

