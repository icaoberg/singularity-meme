Bootstrap: docker
From: debian:buster

IncludeCmd: yes

%labels
    AUTHOR icaoberg
    EMAIL icaoberg@alumni.cmu.edu
    WEBSITE http://www.andrew.cmu.edu/~icaoberg
    VERSION 5.1.0

%post
    apt-get update && apt-get install -y \
       wget \
       libopenmpi-dev \
       openmpi-bin \
       ghostscript \
       libgs-dev \
       libgd-dev \
       libexpat1-dev \
       zlib1g-dev \
       libxml2-dev \
       autoconf automake libtool \
       libhtml-template-compiled-perl \
       libxml-opml-simplegen-perl \
       libxml-libxml-debugging-perl \
       sudo \
       openssh-server
    wget -nc http://meme-suite.org/meme-software/5.1.0/meme-5.1.0.tar.gz
    tar -xvf meme-5.1.0.tar.gz && rm -fv meme-5.1.0.tar.gz
    PERL_MM_USE_DEFAULT=1 perl -MCPAN -e 'install Log::Log4perl'
    PERL_MM_USE_DEFAULT=1 perl -MCPAN -e 'install Math::CDF'
    PERL_MM_USE_DEFAULT=1 perl -MCPAN -e 'install CGI'
    PERL_MM_USE_DEFAULT=1 perl -MCPAN -e 'install HTML::PullParser'
    PERL_MM_USE_DEFAULT=1 perl -MCPAN -e 'install HTML::Template'
    PERL_MM_USE_DEFAULT=1 perl -MCPAN -e 'install XML::Simple'
    PERL_MM_USE_DEFAULT=1 perl -MCPAN -e 'install XML::Parser::Expat'
    PERL_MM_USE_DEFAULT=1 perl -MCPAN -e 'install XML::LibXML'
    PERL_MM_USE_DEFAULT=1 perl -MCPAN -e 'install XML::LibXML::Simple'
    PERL_MM_USE_DEFAULT=1 perl -MCPAN -e 'install XML::Compile'
    PERL_MM_USE_DEFAULT=1 perl -MCPAN -e 'install XML::Compile::SOAP11'
    PERL_MM_USE_DEFAULT=1 perl -MCPAN -e 'install XML::Compile::WSDL11'
    PERL_MM_USE_DEFAULT=1 perl -MCPAN -e 'install XML::Compile::Transport::SOAPHTTP'
    mkdir /opt/meme
    mv -v meme-5.1.0 /opt/meme
    cd /opt/meme/meme-5.1.0 && \
	./configure --prefix=/opt/meme  --enable-build-libxml2 --enable-build-libxslt  --with-url=http://meme-suite.org && make && make install

####################################################################################
%apphelp meme
    /opt/meme/bin/meme --help

%apprun meme
    /opt/meme/bin/meme "$@"

####################################################################################
%apphelp memechip
    /opt/meme/bin/meme-chip --help

%apprun memechip
    /opt/meme/bin/meme-chip "$@"

####################################################################################
%apphelp dreme
    /opt/meme/bin/dreme --help

%apprun dreme
    /opt/meme/bin/dreme "$@"

####################################################################################
%apphelp glam2
    /opt/meme/bin/glam2 --help

%apprun glam2
    /opt/meme/bin/glam2 "$@"

####################################################################################
%apphelp momo
    /opt/meme/bin/momo --help

%apprun momo
    /opt/meme/bin/momo "$@"

####################################################################################
%apphelp ame
    /opt/meme/bin/ame --help

%apprun ame
    /opt/meme/bin/ame "$@"

####################################################################################
%apphelp centrimo
    /opt/meme/bin/centrimo --help

%apprun centrimo
    /opt/meme/bin/centrimo "$@"

####################################################################################
%apphelp spamo
    /opt/meme/bin/spamo --help

%apprun spamo
    /opt/meme/bin/spamo "$@"

####################################################################################
%apphelp gomo
    /opt/meme/bin/gomo --help

%apprun gomo
    /opt/meme/bin/gomo "$@"

####################################################################################
%apphelp fimo
    /opt/meme/bin/fimo --help

%apprun fimo
    /opt/meme/bin/fimo "$@"

####################################################################################
%apphelp mast
    /opt/meme/bin/mast --help

%apprun mast
    /opt/meme/bin/mast "$@"

####################################################################################
%apphelp mcast
    /opt/meme/bin/mcast --help

%apprun mcast
    /opt/meme/bin/mcast "$@"

####################################################################################
%apphelp motiph
    /opt/meme/bin/motiph --help

%apprun motiph
    /opt/meme/bin/motiph "$@"

####################################################################################
%apphelp glam2scan
    /opt/meme/bin/glam2scan --help

%apprun glam2scan
    /opt/meme/bin/glam2scan "$@"

####################################################################################
%apphelp tomtom
    /opt/meme/bin/tomtom --help

%apprun tomtom
    /opt/meme/bin/tomtom "$@"

####################################################################################
%apphelp tgene
    /opt/meme/bin/tgene --help

%apprun tgene
    /opt/meme/bin/tgene "$@"

####################################################################################
%apphelp ama
    /opt/meme/bin/ama --help

%apprun ama
    /opt/meme/bin/ama "$@"

