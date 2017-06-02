Auto Install IoT Demo with OpenShift
=========================================
This project adds IoT demo to the original OpenShift install demo from Eric, Andrew. It first installs OpenShift on the local system and then creates IoT demo project to this OpenShift instance. 

This project requires a docker engine, OpenShift command line tools and VirtualBox, but these checks happen when you run the
installation and point you to what is missing.

Pro Tip: Pay close attention to conosle output, will guide you to dependencies you need if missing. These dependencies are 
listed here and the install provides pointers to downloads if missing:

   ```
   1. VirtualBox
   2. Docker engine version 17.03
   3. OpenShift Client (oc) v3.5.5.5
   ```


Installation Steps
-----------------------
```
$ git clone -b Summit-Demo-Setup https://github.com/redhat-iot/ocp-install-demo
$ cd ocp-install-demo
$ ./init.sh

Login to web console at: 
https://192.168.99.101:8443
 
user: openshift-dev                
password: devel  

```
Notes
-----

If you recieve the following error, on Linux:

   ```
   Error: did not detect an --insecure-registry argument on the Docker daemon
   ```

Then ensure that the Docker daemon is running with the following argument by:

   ```
   # Add the following to /etc/sysconfig/docker file and
   # restart the docker service:
   #
   INSECURE_REGISTRY='--insecure-registry 172.30.0.0/16'
   ```

This project has an install script that is setup to allow you to re-run it without worrying about previous
installations. If you re-run it, it removes old 'openshift' machines and reinstalls for you. 


Supporting Articles
-------------------
- [Cloud Happiness - How To Get OpenShift Container Platform v3.5 Installed in Minutes](http://www.schabell.org/2017/05/cloud-happiness-how-to-get-openshift.html)


Released versions
-----------------
See the tagged releases for the following versions of the product:

- v1.6 - OpenShift Container Platform v3.5 based on OpenShift command line tools v3.5.5.5.

- v1.5 - OpenShift Container Platform v3.4 based on OpenShift command line tools v3.4.1.2-fixed.

- v1.4 - OpenShift Container Platform v3.4 based on OpenShift command line tools v3.4.1.2, added more JBoss product templates.

- v1.3 - OpenShift Container Platform v3.4 based on OpenShift command line tools v3.4.1.2, added Windows installer option.

- v1.2 - OpenShift Container Platform v3.4 based on OpenShift command line tools v3.4.1.2, improved docker validation for Linux.

- v1.1 - OpenShift Container Platform v3.4 based on OpenShift command line tools v3.4.1.2.

- v1.0 - OpenShift Container Platform v3.3 based on OpenShift command line tools v3.3.1.3.

![OCP Login](https://github.com/redhatdemocentral/ocp-install-demo/blob/master/docs/demo-images/ocp-login.png?raw=true)

![Cloud Suite](https://github.com/redhatdemocentral/ocp-install-demo/blob/master/docs/demo-images/rhcs-arch.png?raw=true)

