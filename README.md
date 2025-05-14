# FWA router on a budget

## The problem

I live in a detached house, in digital divide rural area in Italy. For years I used to buy Internet connectivity from WISP using pure 5GHz WiFi or 28GHz radio (eg. Eolo), but these WISP use to do overprovisioning, so the bandwidth they sell is rarely available. 
Moreover, these solutions (not due to wireless technology limits but to WISP infrastrures) aren't always reliable, so there are availability problems during thunderstorms, windstorms, rainstorms. Internet connection for me is mandatory, doing teleworking.
Due to poor reliability of WISPs I had to setup a 4G backup connection too. But in Italy telco market is always fluid, changing and unpredictable. I bought a 4G SIM from Fastweb, when they were NMVO of Wind. 
I have a WindTre BTS at 1Km in LOS from my home and now this BTS have 5G too. When Fastweb and Vodafone merged, Fastweb begun to use Vodafone infrastructures... but the nearest Vodafone BTS is 3Km away and NLOS! So became very slow!

## The solution

I tried a WindTre SIM and obtained, with a 5G phone, 450/100Mbps! Outside, because inside due to thick walls speed really slows down. So I decided to unsubscribe all others utilities and subscribe a WindTre FWA (5G router included) or a WindTre unlimited SIM.
But FWA come with inside router only and I hate using consumer chinese routers (expecially if telco customized and locked down). And WindTre FWA and unlimited SIMs are behind CGNAT, so I couldn't have public IP, my own home servers. Moreover with WindTre there are disconnections every 4 hours.
There are telco brokers that sells DeNAT SIM with dynamic public IP address and disconnections every 24 hours. But what about the router? 4G LTE routers are relatively cheap, also CAT6+. Instead, 5G routers are extremely expensive, also chinese ones.
I love MikroTik devices, they are cheap but (usually...) reliable and powerful. But they don't have outside 5G routers and the only inside one they sell, Chateau, is extremely expensive. Also used outside routers are expensive and unobtainable.
So I decided to look for used 5G modules, when succeded to found a pair used and cheap, I decided to build an outside router from scratch! For the router itself I used a MikroTik RouterBoard RBM33G (RBM11G could be used, but oddly it's costlier then RBM33G).

## My making

I bought an electrical waterproof box (with transparent lid, but it was just a whim to made some pictures and this documentation), the [RouterBoard RGB33G](https://mikrotik.com/product/rbm33g), a Kalea Informatique [M.2 to USB3.0 adapter](https://www.kalea-informatique.com/m-2-ngff-3g-4g-5g-module-to-usb-3-0-adapter-with-dual-sim-card-slot-and-power.htm) for 3G/4G/5G modules and an used 5G M.2 module.
NB: It's mandatory to found a 4G/5G module with USB3.0 port, not cheap PCIe only because they won't work with RouterBoards. Moreover, M.2 to miniPCIe adapter cannot be used with RouterBoards or the speed will be limited to USB2.0 speed (480Mbps, so not more then ~250Mbps LTE speed).
I bought also a pair of chinese cheap omnidirectional antennas (2x2 MIMO), a waterproof ethernet connector, some 2mm and 3mm hexagonal spacers (I preferred nylon for 2mm and brass for 3mm, because 3mm ones are used to mechanically support the entire internal structure while 2mm ones 
are used to supports PCBs of RouterBoard and adapter and to stabilize the structure).
