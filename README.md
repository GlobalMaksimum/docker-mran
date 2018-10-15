[Microsoft R Open: The Enhanced R Distribution](https://mran.microsoft.com/open) (previously [Revolution Analytics](http://blog.revolutionanalytics.com/) ) on [ubuntu:18.04](https://hub.docker.com/r/_/ubuntu/) image 
(~84 MB image size seems to be a good alternative for [Alpine Linux](https://alpinelinux.org/) for Ubuntu lovers :heart::)

We try to keep image as compact as possible. Compared to [r-ver](https://github.com/rocker-org/rocker-versioned), since MRO includes [Intel MKL](https://software.intel.com/en-us/mkl) image size is 200 MB more :/

### Quickstart

```
docker run -it --rm  --name myflumsy-R globalmaksimum/mran:latest
```


```

R version 3.5.1 (2018-07-02) -- "Feather Spray"
Copyright (C) 2018 The R Foundation for Statistical Computing
Platform: x86_64-pc-linux-gnu (64-bit)

R is free software and comes with ABSOLUTELY NO WARRANTY.
You are welcome to redistribute it under certain conditions.
Type 'license()' or 'licence()' for distribution details.

R is a collaborative project with many contributors.
Type 'contributors()' for more information and
'citation()' on how to cite R or R packages in publications.

Type 'demo()' for some demos, 'help()' for on-line help, or
'help.start()' for an HTML browser interface to help.
Type 'q()' to quit R.

Microsoft R Open 3.5.1
The enhanced R distribution from Microsoft
Microsoft packages Copyright (C) 2018 Microsoft Corporation

Using the Intel MKL for parallel mathematical computing (using 8 cores).

Default CRAN mirror snapshot taken on 2018-08-01.
See: https://mran.microsoft.com/.

>

```
