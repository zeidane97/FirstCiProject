#  Continuous Integration
[![Build Status](http://ec2-54-175-79-54.compute-1.amazonaws.com/buildStatus/icon?job=project-2804-devCI)](http://ec2-54-175-79-54.compute-1.amazonaws.com/job/project-2804-devCI/)
##Hello last commit i think
##hello encore un commit 2
##hello encore un commit 3
##hello encore un commit 4
##second commit
##third commit
##fourth commit
## Project description

- Project Battleboat deployed with Continous Integration project with branch control
- The goal of this app is to serve a static website and connect to a MySQL database as a simple backend app would do.

## Test if application is working

- To test ths application after deploy container you can use this following script :

```sh
EXTERNAL_HOSTNAME=`curl http://169.254.169.254/latest/meta-data/public-hostname`\
&& if [[ $(curl -s -o /dev/null -w "%{http_code}" $EXTERNAL_HOSTNAME':8181/health') == 200 ]];\
then echo "Application déployée"; exit 0; else echo "Application injoignable"; exit 1; fi
```
