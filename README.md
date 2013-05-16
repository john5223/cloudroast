CloudRoast, CloudCAFE Test Repo
================================
<pre>
 (----) (----)--)
  (--(----)  (----) --)
(----) (--(----) (----)
-----------------------
\                     /
 \                   /
  \_________________/    
     )\ `   `(` `
     ( ) ` )' )  \_
    (   )  _)  \   )
  ) )   (_  )   ,  (
  (  ,  )   (   (
    (  (    )    )
  === CloudRoast ===
= A CloudCAFE Test Repository =
</pre> 

CloudRoast is a rich, full bodied blend of premium roasted automated test cases. CloudRoast tests are based on the expanded unittest driver in the 
[Open CAFE Core](https://github.com/stackforge) and built using the [CloudCAFE Framework](https://github.com/stackforge).
 
CloudRoast tests support smoke, functional, integration, scenario and reliability based test cases for OpenStack. It is meant to be highly flexible 
and leave the logic of the testing in the hands of the test case developer while leaving the interactions with OpenStack, various resources and 
support infrastructure to CloudCAFE.

Installation
------------
CloudRoast can be [installed with pip](https://pypi.python.org/pypi/pip) from the git repository after it is cloned to a local machine. 
 
* First follow the README instructions to install the [CloudCAFE Framework](https://github.com/stackforge)
=======
CloudCAFE, An CAFE Implementation for OpenStack
================================
<pre>
   _ _ _
  ( `   )_ 
 (    )   `)  _
(____(__.___`)__)

    ( (
       ) )
    .........    
    |       |___ 
    |       |_  |
    |  :-)  |_| |
    |       |___|
    |_______|
=== CloudCAFE ===
= An Open CAFE Implementation =
</pre> 

CloudCAFE is an implementation of the [Open CAFE Framework](https://github.com/stackforge) specifically designed to test deployed 
versions of [OpenStack](http://http://www.openstack.org/). It is built using the [Open CAFE Core](https://github.com/stackforge). 

Supported Operating Systems
---------------------------
CloudCAFE has been developed primarily in Linux and MAC environments, however, it supports installation and 
execution on Windows

Installation
------------
CloudCAFE can be [installed with pip](https://pypi.python.org/pypi/pip) from the git repository after it is cloned to a local machine. 
 
* First follow the README instructions to install [Open CAFE Core](https://github.com/stackforge)
* Clone this repository to your local machine  
* CD to the root directory in your cloned repository.
* Run "pip install . --upgrade" and pip will auto install all other dependencies.

Configuration
--------------
CloudRoast runs on the [CloudCAFE Framework](https://github.com/stackforge) using the cafe-runner. It relies on the configurations installed to: 
<USER_HOME>/.cloudcafe/configs/<PRODUCT> by CloudCAFE.

At this stage you will have the Open CAFE Core engine, the CloudCAFE Framework implementation and the Open Source automated test cases. You are now 
ready to:
1) Execute the test cases against a deployed Open Stack.
                       or
2) Write entirely new tests in this repository using the CloudCAFE Framework.

Logging
-------
If tests are executed with the built-in cafe-runner, runtime logs will be output to 
<USER_HOME>/.cloudcafe/logs/<PRODUCT>/<CONFIGURATION>/<TIME_STAMP>. 

In addition, tests built from the built-in CAFE unittest driver will generate 
csv statistics files in <USER_HOME>/.cloudcafe/logs/<PRODUCT>/<CONFIGURATION>/statistics for each and ever execution of each and every test case that 
provides metrics of execution over time for elapsed time, pass/fail rates, etc...

Basic CloudRoast Package Anatomy
-------------------------------
Below is a short description of the top level CloudRoast Packages.

##test_repo
This is the root package for all automated tests. This is namespace is currently **required** by the cafe-runner for any Test Repository plug-in.

##identity
OpenStack Identity Service cafe-runner plug-in test cases. 

##compute
OpenStack Compute Service cafe-runner plug-in test cases. 
=======
CloudCAFE works in tandem with the [Open CAFE Core](https://github.com/stackforge) cafe-runner. This installation of CloudCAFE includes a reference 
configuration for each of the CloudCAFE supported OpenStack products. Configurations will be installed to: <USER_HOME>/.cloudcafe/configs/<PRODUCT>

To use CloudCAFE you **will need to create/install your own configurations** based on the reference configs pointing to your deployment of OpenStack.

At this stage you will have the Open CAFE Core engine and the CloudCAFE Framework implementation. From this point you are ready to:
1) Write entirely new tests using the CloudCAFE Framework
					or
2) Install the [CloudRoast Test Repository](https://github.com/stackforge), an Open Source body of OpenStack automated tests written with CloudCAFE 
that can be executed or extended. 

Logging
-------
CloudCAFE leverages the logging capabilities of the CAFE Core engine. If tests are executed with the built-in cafe-runner, runtime logs will be output   
to <USER_HOME>/.cloudcafe/logs/<PRODUCT>/<CONFIGURATION>/<TIME_STAMP>. In addition, tests built from the built-in CAFE unittest driver will generate 
csv statistics files in <USER_HOME>/.cloudcafe/logs/<PRODUCT>/<CONFIGURATION>/statistics for each and ever execution of each and every test case that 
provides metrics of execution over time for elapsed time, pass/fail rates, etc...

Basic CloudCAFE Package Anatomy
-------------------------------
Below is a short description of the top level CloudCAFE Packages.

##cloudcafe
This is the root package for all things CloudCAFE.

##common
Contains modules that extend the CAFE Core engine specific to OpenStack. This is the primary namespace for tools, data generators, common 
reporting classes, etc...

##identity
OpenStack Identity Service plug-in based on CAFE Core extensions. 

##compute
OpenStack Compute plug-in based on CAFE Core extensions. 

##blockstorage
OpenStack Block Storage plug-in based on CAFE Core extensions. 

##objectstorage
OpenStack Object Storage plug-in based on CAFE Core extensions. 
