NestaCMS on Openshift
=============
Long version how-to with manual installation there http://igortirador.github.com/blog/2012/10/06/nestacms-on-openshift/

This git repository helps you get up and running quickly w/ a NestaCMS installation

on OpenShift.

Running on OpenShift
----------------------------

Create an account at http://openshift.redhat.com/

Create a ruby-1.9 application

    rhc app create -a nestacms -t ruby-1.9

Add this upstream nestacms repo

    cd nestacms
    git remote add upstream -m master git://github.com/IgorTirador/nestacms-example.git
    git pull -s recursive -X theirs upstream master
    
Then push the repo upstream

    git push

That's it, you can now checkout your application at:

    http://yourappname-$yournamespace.rhcloud.com

