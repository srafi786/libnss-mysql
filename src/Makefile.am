##  Copyright (C) 2002 Ben Goodwin
##  This file is part of the nss-mysql library.
##
##  The nss-mysql library is free software; you can redistribute it and/or
##  modify it under the terms of the GNU General Public License as published
##  by the Free Software Foundation; either version 2 of the License, or
##  (at your option) any later version.
##
##  The nss-mysql library is distributed in the hope that it will be useful,
##  but WITHOUT ANY WARRANTY; without even the implied warranty of
##  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
##  GNU General Public License for more details.
##
##  You should have received a copy of the GNU General Public License
##  along with the nss-mysql library; if not, write to the Free Software
##  Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA  02111-1307  USA
##
## $Id$
# From Makefile.am $Revision$

library_sources         = version.c nss_config.c nss_main.c \
                          nss_support.c mysql.c lookup.c \
                          mysql-pwd.c mysql-spwd.c mysql-grp.c
library_ldflags         = -module -version-info @LIBVER@:0:0 \
                          -export-symbols $(srcdir)/@OS@.sym

lib_LTLIBRARIES         = libnss_mysql.la
libnss_mysql_la_CFLAGS  = @MYSQL_CFLAGS@
libnss_mysql_la_LDFLAGS = @MYSQL_LDFLAGS@ $(library_ldflags)
libnss_mysql_la_SOURCES = $(library_sources)

noinst_HEADERS = nss_mysql.h lookup.h
