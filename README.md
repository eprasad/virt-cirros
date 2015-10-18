# virt-cirros
 Many run CirrOS on cloud for testing, learning, training or even demos. Its fast, lightweight, agile OS that 
 specializes in running on a cloud. 
 
OpenStack deployments are mostly tested using CirrOS. It is versatile for various test scenarios, Be it network or orchestration. Everyone loves cirros on cloud but what about virtualization? 
 
 Yes, Virtualization Platforms are still there and many use them. I want to do some testing on my virtualization
 platform (vmware,kvm,virtual-box), Can I use CirrOS image?  The answer is yes, The official CirrOS image works with
 any virtualization platform you name it. However, There is a small problem. It comes with cloud-init configured. 
 
 Then what? Cloud-init is a package that contains utilities for early initialization of cloud instances using metdata 
 services of the cloud.  When you start the CirrOS on virt, Before you get login screen, Its cloud-init service is what 
 execures and will start finding the metadata server. If metedata service not found, retries connecting it 20 times. 
 This 20 retries is equal to 20 seconds delay. So the official image of CirrOS will take 20 + seconds to boot on 
 virtualization platforms. 20 seconds is huge for impatient system administrator like me. Correct?   
 
 Solution?   Use this cirros for virt image (virt-cirros), It will boot within few seconds and is specially made
 for virtualization platforms. cloud-init is disbaled  :) 
 
 Download Link : https://github.com/eprasad/virt-cirros/raw/master/virt-cirros-0.3.4-x86_64-disk.img
 

