# 🌐 Internet and Wifi 🛜

## The old setup
Until recently our internet router was a Teltonika RUTX11 <a href="https://www.teltonika-networks.com/de/products/routers/rutx11">(for more infos visit the Teltonika homepage)</a> and a Panorama Antennas LPMDM-6-60-24-58 <a href="https://panorama-antennas.com/product/lgmhm-6-60-great-white-2x2-mimo-4g-5g-optional-mimo-wifi-optional-gps-gnss-vehicle-antenna/">(for more infos visit the Panorama Antennas homepage)</a>. The RUTX11 is a 4G router and that was the reason why I changed the setup. The 4G router did a great job and the bandwith was always good as long as there was mobile phone reception. It gave us the oportunity to stay online, when our phones couldn't because of the poor reception.

## The new setup
The new setup is a GL iNet Spitz AX or GL-X3000 <a href="https://store-eu.gl-inet.com/collections/spitz-ax-gl-x3000/products/spitz-ax-gl-x3000-wi-fi-6-4g-lte-5g-nrdual-sim-openwrt-c19g">(for more infos visit the GL iNet homepage)</a> and a Panorama Antennas LPMM4B-6-60 <a href="https://panorama-antennas.com/product/lgmhm4b-6-60-24-58-mako-4x4-mimo-4g-5g-up-to-6x6-mimo-wifi-gps-gnss-vehicle-antenna/">(for more infos visit the Panorama Antennas homepage)</a>.

<b>Q:</b> Why the new router?</br>
<b>A:</b> To get the most out of our unlimited 5G sim card 😉

<b>Q:</b> Why the new antenna?</br>
<b>A:</b> First, because the Spitz AX has four antenna ports now and I wanted to use all four of them with the external antenna to have a better mobile phone reception. Second, one of the third and fourth antenna ports of the router also serves as a GPS antenna. In the previous setup we had an external GPS dongle at the RUTX11 which we do not need anymore.

## How to get the location information from the GL iNet router
Why do we need the location of the van?
<ul>
<li>Security: To know where the van is.</li>
<li>Comfort: To get the latest weather information for the current location.</li>
<li>Future reasons: To trigger events based on the location.</li>
</ul>

To configure the router follow this guide: <a href="https://forum.gl-inet.com/t/howto-gl-x3000-gps-configuration-guide/30260">[howto] GL-X3000 GPS configuration guide</a>

You'll find the modem AT-command line tool by login in the router and on the main page there are informations about the mobile phone reception. Click on the three dots in the upper right corner, there you will find the command line tool.

In Home Assistant is used the GPSD integration: <a href="http://192.168.1.2:8123/config/integrations/integration/gpsd">HA GPSD integration</a>
