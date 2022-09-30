# OSSM - Open Source Sex Machine
OSSM (pronounced like "Awesome") is a user friendly every day sex machine for the people.

This project aims to help people curious about sex machines explore their interest. A second objective is optionally learning how mechanics, electronics, physics and computing are involved in your sexual pleasure.  We encourage a developing ecosystem of options.  If you can build a better _reference board/remote_ contribute back to the community and offer them for sale. 

Please note that this is a _work in progress_ and is closer to an alpha than beta product.  There are a number of machines completed and in use but you will have to explore the solution space even using the recommended hardware and a reference board.  Documentation is a work in progress and there are number of flavours of OSSM.  

During development we are attempting to keep compatibility with the current BOM going forward, but it's not guaranteed. If a better motor or other part is found the project may pivot.  Being open source you can continue to support it yourself and keep your machine maintained.  

*Primary design goals* are to make a machine that is Accessible, Compact, Quiet, Moderate cost, 3D printable (no cutting/machining), High performance, flexible, Easily sourced components, Doesn't look like a giant machine.

## Getting Started

Deciding how to build your OSSM

Getting started on building an OSSM can be a bewildering number of choices. One way to look at building an OSSM is that with a diverse set of skills it is quite an easy task. however, many people have a subset of these skills and tools:

- Mechanical skills for assembling the OSSM

- 3D printing skills and a functional FDM printer

- Software development skills and experience with PlatformIO

- Electronics skills including soldering and component specification

- Computer Aided Design (CAD) skills

There are easier and harder ways to build an OSSM. The more skills you have the more you can improvise with different hardware and software. The less skills you have the harder time you have if you stray off the well-trodden path.

Keep in mind that the OSSM community is small. The more time spent supporting people can distract community members from making OSSM better. When you start your build, it is worthwhile reflecting on what is the best path for you to take. If you have no experience, no skills, no tools and cannot afford a reference board and the recommended servo, this is a project you should come back to later in your maker development. 

As of October 2022, the OSSM is far from being a turnkey offering. There are multiple versions of firmware, different motor and how it is mounted requires research.

The easiest path to getting an operational OSSM is to purchase a reference board and use the recommended JMC servo motor (more below)

<h3><p align="center"><a href="FAQ.md">Read the Frequently Asked Questions</a></p></h3>

There are a few hardware flavours to choose from, we've included user modified versions in case that fits your use case better!

<h3><p align="center"><a href="https://github.com/KinkyMakers/OSSM-hardware/blob/master/Documentation/Assembly%20Instructions.pdf">Build Instructions</a></p></h3>

Join our Discord to be part of the discussion. https://discord.gg/MmpT9xE

### Software

The software is available in this github repository along with specialised version in forks, the software is written and compiled utilizing PlatformIO on Visual Studio Code. <a href="OSSM PlatformIO Readme.md">Reference for working with the code in PlatformIO here</a>

###Microcontroller 
We recommend using a reference board that already has a Microprocesser installed, but for experienced (and experimental users) it can be built using ESP32 microcontroller. This code is still arduino IDE compatible but offers many times better performance.  

### PCB design
Simple PCB to power an ESP32 (wifi enabled microcontroller) from 24V and breakout the pins for the OSSM control is available in the repository. Alternatively you can purchase a reference board that makes it all easy.  Plug onto the recommended servo and connect up the power to the terminal block.  

### Mechanical design
The OSSM use a compact belt design with components that have become widely available due to 3D printing popularity.
It is driven by a Nema23 patterned motor. The recommended and most widely supported feature rich is a JMC Servo which is the default option for the current developers.  Servo motors offer good torque at a wide range of speeds and require less power and are slightly more expensive.  Many of the more advanced features are exclusive to to later JMC firmare.  Experienced users have the option to use a Nema23 patterned motor of **your** choosing, although we reccomend small integrated closed loop steppers for their cost to performance ratio if not using a JMC servo.  

<img src="https://github.com/KinkyMakers/OSSM-hardware/blob/5cbd1378f6389e5d8ece273931e7b261c27d1871/Documentation/OSSM%20mechanical%20overview.png" width="750" >

### Safety

The safety of the OSSM build is yet to be fully characterized as it is a work in progress. The OSSM is a work in progress and as it is a framework for building your own sex machine your specific combination may have risks not inherent to other builds. These risks may be undocumented. 

While using the OSSM we can suggest the following heiracrhy of safety, however it is up to you and your build to decide what risks exist and how to mitigate them. 

- A) Have ability to move away
- B) Have ability to remove the power
- C) If in bondage, that is responsibility of the Top




## Bill Of Materials

We are calling this the reference build, when deviating from it please check compatability with existing BOM

1) **[3D Printed Parts](Hardware/OSSM%20Printed%20Parts)**
   - This has recently had significant changes
   - [Make sure to choose one of the options for the toy adapters](Hardware/OSSM%20Printed%20Parts/end%20effector%20options)
   - Mounting options are still something that need to be worked on
   - Thank you @Elims for the [belt tensioner design](https://media.discordapp.net/attachments/756320102919700607/858110808281317396/unknown.png) ( https://github.com/theelims/FuckIO )
2) ** IHSV57 NEMA23 Servo with 8mm shaft** : [Amazon.ca](https://www.amazon.ca/Integrated-Servo-Motor-IHSV57-30-10-3000rpm/dp/B081CVJHC7) | [JMC](https://www.jmc-motor.com/product/953.html)
   - *Avoid the StepperOnline version until we can further test*
   - Make sure you get something with **8mm** shaft.
   - There are *3* sizes of this motor.  100W = iHSV57-30-**10**, 140W = iHSV57-30-**14**, 180W = iHSV57-30-**18** 
   - Search around for the best deal for you - reccommend searching "ihsv57" on Aliexpress.com and choosing the -10 -14 or -18
   - For details on picking the right motor for your use case - check this [FAQ](https://github.com/KinkyMakers/OSSM-hardware/blob/master/FAQ.md#q--what-strength-of--motor-do-i-need)
   - If you are using the 140W or180W version it is recommended to use a 10mm wide belt and pulley (see the next two items)
3) **GT2 Pulley 8mm Bore 20 Tooth** : [Amazon.ca](https://www.amazon.ca/Saiper-Timing-Aluminum-Synchronous-Printer/dp/B07MDH63GX/ref=sr_1_5?dchild=1&keywords=8mm+bore+gt2&qid=1627821975&sr=8-5)
4) **GT2 Timing Belt** : [Amazon.ca](https://www.amazon.ca/Printer-Timing-Teeth-Pulley-Wrench/dp/B08PKPK4D8/ref=sr_1_8?dchild=1&keywords=gt2+timing+belt&qid=1627821669&sr=8-8)
* Only the GT2 belt is needed from this kit, however it's often cheaper with the incorrect sized pulleys in a bundle
* Your desired stroke length plus about 200mm should be your minimum order length
5) **Bearings** 5x11x4mm : [Amazon.ca](https://www.amazon.ca/gp/product/B07CVBW44R/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
6) **MGN12H Rail and bearing** : [Amazon.ca](https://www.amazon.ca/Usongshine-guidage-lin%C3%A9aire-MGN12H-300mm/dp/B07XLL484J/ref=pd_sbs_201_1/139-0384147-0570541?_encoding=UTF8&pd_rd_i=B07XT8ZY9H&pd_rd_r=e7dc0ab7-e244-4a6c-ba42-59d7da76e03b&pd_rd_w=jhRlq&pd_rd_wg=zovAp&pf_rd_p=0ec96c83-1800-4e36-8486-44f5573a2612&pf_rd_r=YZGA61RD95B0E3H004ZA&refRID=YZGA61RD95B0E3H004ZA&th=1)
   - Minimum 250mm in length
   - Rail length = desired stroke + 180mm
   - Must be MGN12**H** rail
7) **Power Supply** : [Amazon.ca](https://www.amazon.ca/LEDENET-Adapter-Flexible-Lighting-5-52-5mm/dp/B078N5DC2J/ref=sr_1_9?keywords=24v+4a&qid=1636728925&sr=8-9)
   - Larger motors generally need more power. 
   - 180W -> 24V 6A
   - 140W -> 24V 6A
   - 100W -> 24V 4A
   - Choose the closest supply to the guidelines, **the ossm will still work**, but may be limited at maximum thrust force.
   - Ensure the power supply is fully enclosed (like a laptop power supply)
   - Ensure the power supply has the correct approvals for your location
   - Cheap power supplies are "pays your money, takes your chances". 
8) **Metric Cap Screws** : [Amazon.ca](https://www.amazon.ca/Comdox-500pcs-Socket-Screws-Assortment/dp/B06XQLTLHP/ref=sr_1_12?dchild=1&keywords=metric+socket+head+cap+screw+kit&qid=1600747665&sr=8-12)
   - A kit like this will provide what's needed:
   - 2x m5x20
   - 2x M5X45
   - 1x m5x12 (can also use m5x20)
   - 10x m3x8
   - 2x m3x16
   - 8x m5 nuts
   - 8x m3 nuts
9) A reference board (most people) 
   - [An official OSSM reference PCB](https://research-and-desire.myshopify.com/collections/all/products/ossm-reference-board) 

10) Experienced users may wish to use a **ESP32 Development Board**  
   - We do not currently have a best suggestion if you are not using a reference board, most generic development boards are the same
   - We have found that the 3.3v boards may miss steps at high speed, so please use a level shifter as well. 

## Official OSSM reference board

![image](https://user-images.githubusercontent.com/43324815/150361448-80e9fdaf-4a8c-4054-a920-6eab9aa68678.png)
