# Hobby projects involving a cluster of Raspberry Pi computers
The purpose is to learn about several subjects within computing, networking and application development by defining mini-projects and working on these. The base for these mini-projects will be a computer-cluster consisting of raspberry Pi computers.

Some things I want to experiment with are:
- set up a kubernetes environment
- set up means of monitoring/managing the kube environment
- Setting up a web application for multiple purposes
  - pull API info for buses, weather
  - Build IoT sensors and devices and connect these

I will be using this document to log my progress and learnings. If there are any readers, feel free to interact here or by getting in touch through some other media.

The style of the blog will be that I post irregular updates as intresting progress is (or maybe isn't) made. I will most likely post a lot of questions, which may serve as questions asked to myself, to be answered at a later point in time. Lastly, as mentioned, there isnt really a long term end goal for this project, but rather short term mini projects.


## Hardware specs of cluster as of 2/9
I was up to this point already a proud owner of one Raspberry Pi model 3B, but since I want to start a small cluster, I decided to start out by buying two more. The Pis themselves are not enough to get started, so some other purchases were needed, mostly in regards to power. The choices for supplying the cluster with power are explained below, followed by a complete hardware list for the build.

### Power management
The 3B model has a current draw of up to 2.5 A at 5V, which is quite rare to find on normal usb power supply units meant for phones. I decided to get a USB charger station with capacity per usb port up to 2.4 at 5V. If there are any power problems, I may look into solving them by underclocking the Pi computers or acquiring something more beefy. An assumption is that the Pis won't draw much power at all with HDMI and Wifi turned off. **Is there an easy way to measure this?**

### Hardware list for build
Component type | Solution | Amount
-------------- | -------- | ------
Computers | Raspberry Pi Model 3B | 3
Memory  | SanDisk microSD cards, 16GB | 3
Power | Linocell 10A USB charger station | 1
Networking | By cable to my main router | 1

![TODO: Image of components:](img)

### First iteration of setting up a kubernetes cluster
The OS installed to the Pis was Raspbian Stretch Lite, written to the SD-cards using etcher. The SD cards were then configured for headless starts by SSH. At first start, the names of the units were changed according to wether they are workers or the master. I use the Pi which was bought some time ago as the master. It has some customizations to usernames and folder structure, from old use. **could cause some problems, will probably reinstall**

For the most part, I used documentation provided in <link to kubernetes for pi guide>.

![TODO: Image of components:](img)
### Reflection and future work
want to look at:
 - Launching simple pod with hello world style web page
 - cluster should set it self up easily from being off
 - shut off HDMI, wifi
 - get a separate switch (probably have one around somewhere...)
 
