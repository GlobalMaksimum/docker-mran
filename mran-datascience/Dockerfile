FROM globalmaksimum/mran:latest
LABEL maintainer="support@globalmaksimum.com"

# ARG DATA_MANIPULATION true
# ARG GRAPHIC_DISPLAY true
# ARG HTML_WIDGETS true
# ARG REPRODUCABLE_RESEARCH true
# ARG MACHINE_LEARNING true

RUN apt-get update && apt-get install -y \
build-essential && \
rm -rf /var/lib/apt/lists/*

# Data Manipulation
RUN Rscript -e 'install.packages("dplyr")'
RUN Rscript -e 'install.packages("data.table")'
RUN Rscript -e 'install.packages("lubridate")'
RUN Rscript -e 'install.packages("jsonlite")'

# Graphic Display
RUN Rscript -e 'install.packages("ggplot2")'
RUN Rscript -e 'install.packages("corrplot")'
RUN Rscript -e 'install.packages("lattice")'

# HTML Widgets
# Required by plotly package
RUN apt-get update && apt-get install -y \
libssl-dev && \
rm -rf /var/lib/apt/lists/*

RUN Rscript -e 'install.packages("ggvis")'
RUN Rscript -e 'install.packages("DT")'

RUN apt-get update && apt-get install -y \
libgit2-dev && \
rm -rf /var/lib/apt/lists/*

# Required by rCharts package
RUN Rscript -e 'install.packages("devtools")'

# Required by rCharts package
RUN apt-get update && apt-get install -y \
unzip && \
rm -rf /var/lib/apt/lists/*
RUN Rscript -e 'library(devtools); remove.packages(c("curl","httr")) ; install.packages(c("curl","httr")); Sys.setenv(CURL_CA_BUNDLE="/opt/microsoft/ropen/3.5.1/lib64/R/lib/microsoft-r-cacert.pem"); install_github("ramnathv/rCharts")'

# Required by plotly package
RUN apt-get update && apt-get install -y \
gfortran && \
rm -rf /var/lib/apt/lists/*
RUN Rscript -e 'install.packages("plotly")'


# Reproducable Research
RUN Rscript -e 'install.packages("knitr")'
RUN Rscript -e 'install.packages("markdown")'
RUN Rscript -e 'library(devtools); install_github("ramnathv/slidify"); install_github("ramnathv/slidifyLibraries")'

# Machine Learning
# Required by mlr package 
RUN apt-get update && apt-get install -y \
libxml2-dev && \
rm -rf /var/lib/apt/lists/*
RUN Rscript -e 'install.packages("mlr")'
RUN Rscript -e 'install.packages("xgboost")'
RUN Rscript -e 'install.packages("caret")'
RUN Rscript -e 'install.packages("gbm")'
RUN Rscript -e 'install.packages("prophet")'
RUN Rscript -e 'install.packages("randomForest")'


CMD ["R"]