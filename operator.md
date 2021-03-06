Hi!

Many thanks for joining the galmon.eu project as a station operator! 

Here are some things to think about:

 * Please ask bert@hubertnet.nl or [ahu on
   IRC](https://webchat.oftc.net/?channels=galileo) or
   [@PowerDNS_Bert](https://twitter.com/PowerDNS_Bert) for a station id. 
 * Please do not randomly pick a station ID!!
 * The rule is: one station ID per receiver. Do not under any circumstances
   use the same ID on multiple receivers, even if you think it should be
   fine. We have 2^64 IDs available, just ask for more IDs
 * Even if you think it should be fine to reuse the same ID, for example
   because your observer page on galmon.eu will look nicer, DO NOT DO IT. It
   messes up our algorithms which track the clock of your receiver.
 * You can set --owner and --remark fields, which helps with administration.
   These fields will show up on https://galmon.eu/observers.html
 * Ublox8 based receivers support GPS/Galileo + BeiDou OR GLONASS. You can't
   do all four at the same time. GPS and Galileo share a slot. If you want
   to know if you should add BeiDou or GLONASS, you can either use your own
   preference or ask us what we are missing in your region.

Downtime
--------
The project is grateful for every bit you can provide. Don't feel bad about
downtime either because your family needs the power plug for Christmas
decorations (this happened) or for whatever reason. 

A good way to increase uptime is to use the Systemd file to ensure automatic
startup on reboots. Some stations with bad power, bad hardware or bad cables
have had great success enabling the Raspberry Pi watchdog.

(need instruction here how to do that for various Raspberries, it differs)

Upgrades
--------
From time to time we upgrade the ubxtool receiver software. Old data also
works but typically if you upgrade, the value to the network increases.

Improving reception
-------------------
A good view of the sky can help tremendously, although as noted, we are
happy with every bit we receive. It helps to put your receiver on a "ground
plate" which is a fancy word for a piece of metal (or mesh even). 

In addition, if you are in a northerly region, your view to the south is
most important. Conversely, if you are in the south, more action will be to
the north.
