FROM bioconductor/devel_proteomics
MAINTAINER Christian Panse <cp@fgcz.ethz.ch>

RUN sudo apt-get install git -y 

RUN cd /tmp && git clone https://github.com/Bioconductor-mirror/specL.git 

RUN cd /tmp && R CMD build --no-build-vignettes specL \
	#&& R CMD check specL_*.tar.gz \
	&& R CMD INSTALL specL_*.tar.gz \
	&& echo "packageVersion('specL')" | R --no-save
