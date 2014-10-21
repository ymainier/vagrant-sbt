# What
sbt in an Ubuntu 14.04 box in order to compile assignments of Functional Programming Principles in Scala

The base box is ubuntu/trusty64.
Then instructions detailed on https://class.coursera.org/progfun-005/wiki/ToolsSetup has been followed to install a jdk 1.7 and sbt 0.12.4

# Usage
    # Clone this repo
    git clone https://github.com/ymainier/vagrant-sbt.git
    # Start and provision the sbt box
    vagrant up
    # Get the Getting Started assignement
    curl -O http://spark-public.s3.amazonaws.com/progfun/assignments/example.zip
    unzip example.zip
    # Connect to the box
    vagrant ssh

    # in the box... 
    # Go to the example directory
    cd /vagrant/example
    # watch the tests fail
    sbt test
