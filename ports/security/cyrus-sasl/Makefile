#
#  iOS Ports
#  Copyright (C) 2010 Bindle Binaries
#
#  @BINDLE_BINARIES_LICENSE_START@
#
#  Redistribution and use in source and binary forms, with or without
#  modification, are permitted provided that the following conditions are met:
#      * Redistributions of source code must retain the above copyright
#        notice, this list of conditions and the following disclaimer.
#      * Redistributions in binary form must reproduce the above copyright
#        notice, this list of conditions and the following disclaimer in the
#        documentation and/or other materials provided with the distribution.
#      * Neither the name of Bindle Binaries nor the names of its contributors
#        may be used to endorse or promote products derived from this software
#        without specific prior written permission.
# 
#  THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
#  AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
#  IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
#  ARE DISCLAIMED. IN NO EVENT SHALL BINDLE BINARIES BE LIABLE FOR ANY
#  DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
#  (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
#  SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
#  CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
#  LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY
#  OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
#  SUCH DAMAGE.
#
#  @BINDLE_BINARIES_LICENSE_END@
#
#  Makefile -- automate downloading OpenLDAP
#

# Package Information
PACKAGE_NAME				= cyrus-sasl
PACKAGE_VERSION				= 2.1.23
PACKAGE_DIR				= $(PACKAGE_NAME)-$(PACKAGE_VERSION)
PACKAGE_FILEEXE				= tar.gz
PACKAGE_FILE				= $(PACKAGE_DIR).$(PACKAGE_FILEEXE)
PACKAGE_MD5				= $(PACKAGE_FILE).md5
PACKAGE_URL				= http://ftp.andrew.cmu.edu/pub/cyrus-mail/$(PACKAGE_FILE)

include ../../../build-aux/Makefile-package

extra-prep:
	cp build-aux/config.h cyrus-sasl/
	mkdir -p include
	cp cyrus-sasl/include/hmac-md5.h  include/
	cp cyrus-sasl/include/md5.h       include/
	cp cyrus-sasl/include/md5global.h include/
	cp cyrus-sasl/include/sasl.h      include/
	cp cyrus-sasl/include/saslplug.h  include/
	cp cyrus-sasl/include/saslutil.h  include/
	cp cyrus-sasl/include/prop.h      include/

clean-local:
	/bin/rm -Rf include

distclean-local:
	/bin/rm -Rf build

# end of Makefile