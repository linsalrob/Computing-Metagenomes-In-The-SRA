# Installing the required software

If you use the `SDSU Computational Genomics` AWS Image freely available on Amazon Web Services and Google Cloud Computing, then all this software is available for you already installed.

However, if you wish, you can install it yourself. These instructions should install most of the software you need on either an Ubuntu-based image or a CentOS-based image.


## Installing on Ubuntu (version 18 or higher)

Install eutils from NCBI. The installation is described in the [Entrez Programming Utilities Help](https://www.ncbi.nlm.nih.gov/books/NBK179288): 

```bash
cd ~
/bin/bash
perl -MNet::FTP -e \
    '$ftp = new Net::FTP("ftp.ncbi.nlm.nih.gov", Passive => 1);
     $ftp->login; $ftp->binary;
     $ftp->get("/entrez/entrezdirect/edirect.tar.gz");'
gunzip -c edirect.tar.gz | tar xf -
rm edirect.tar.gz
builtin exit
export PATH=${PATH}:$HOME/edirect >& /dev/null || setenv PATH "${PATH}:$HOME/edirect"
./edirect/setup.sh
```





## Installing on CentOS (version 7 or higher)

Install eutils from NCBI. The installation is described in the [Entrez Programming Utilities Help](https://www.ncbi.nlm.nih.gov/books/NBK179288): 

```bash
cd ~
/bin/bash
perl -MNet::FTP -e \
    '$ftp = new Net::FTP("ftp.ncbi.nlm.nih.gov", Passive => 1);
     $ftp->login; $ftp->binary;
     $ftp->get("/entrez/entrezdirect/edirect.tar.gz");'
gunzip -c edirect.tar.gz | tar xf -
rm edirect.tar.gz
builtin exit
export PATH=${PATH}:$HOME/edirect >& /dev/null || setenv PATH "${PATH}:$HOME/edirect"
./edirect/setup.sh
```

