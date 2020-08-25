ARG VERSION="10.5.3.2"
ARG APAMA_BUILDER=store/softwareag/apama-builder:${VERSION}

FROM ${APAMA_BUILDER} 
USER root

RUN yum -y update && \
    yum -y install git

RUN pip3 install pysys -U    

RUN mkdir /tools && \
    cd /tools && \
    git clone https://github.com/SoftwareAG/apama-eplapps-tools.git && \
    git clone https://github.com/Yoav11/EPL_assert_demo.git
