#WebLogic 12.2.1 infra (JRF) with SOA, BAM, OSB Cluster

with OSB & SOA with BPM, BAM, B2B & Enterprise schedular

##Details
- CentOS 7 vagrant box
- Puppet 5
- Vagrant >= 2
- Oracle Virtualbox >= 5.1

Download & Add the all the Oracle binaries to /software

edit Vagrantfile and update the software share to your own local folder
- soadb.vm.synced_folder "/Users/edwin/software", "/software"
- soa2admin2.vm.synced_folder "/Users/edwin/software", "/software"

Vagrant boxes
- vagrant up soadb
- vagrant up soa2admin2
- vagrant up mft1admin

## Database
- soadb 10.10.10.5 with Welcome01 as password

###operating users
- root vagrant
- vagrant vagrant
- oracle oracle

###software
- Oracle Database 12.1.0.2 SE Linux
- linuxamd64_12102_database_se2_1of2.zip
- linuxamd64_12102_database_se2_2of2.zip

## Middleware

### default soa osb domain with 1 node
- soa2admin2 10.10.10.21, WebLogic 12.2.1 with Infra ( JRF, ADF, SOA, OSB ) requires RCU

http://10.10.10.21:7001/em with weblogic1 as password

###operating users
- root vagrant
- vagrant vagrant
- oracle oracle

###software
- JDK: jdk-8u192-linux-x64.tar.gz
- FMW Infrastructure: fmw_12.2.1.3.0_infrastructure.jar (uncompressed zip)
- OSB: V886445-01.zip
- SOA: V886440-01.zip

