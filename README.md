Mule 3.x Standalone - Openshift DIY Cartridge
============================

This git repository helps you get up and running quickly with a Mule
on OpenShift.


Running on OpenShift
----------------------------

Register at http://openshift.redhat.com/, and then create a raw (do-it-yourself) application:

    rhc app create -a mule -t diy-0.1 -l yourlogin@yourmail.com

Add this upstream mule-diy-cartridge repo:

    cd mule
    git remote add quickstart -m master https://github.com/ryandcarter/mule-diy-cartridge.git
    git pull -s recursive -X theirs quickstart master
    
Then push the repo upstream:  

    git push

That's it, you can now see your running application at:

    http://mule-yournamespace.rhcloud.com

Updating your application
----------------------------

To deploy your changes to openshift just add your changes to the index, commit and push:

    git add . -A
    git commit -m "a nice message"
    git push

Licence
----------------------------
This project is distributed under [Apache 2 licence](http://www.apache.org/licenses/LICENSE-2.0.html). 
