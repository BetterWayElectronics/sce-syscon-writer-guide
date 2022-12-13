
<h2>Syscon Guide - SCE Syscon Method</h2>
<b>What even is this?</b> Well its a guide on how to read and write your PS4's Syscon on board, <b>without</b> replacing it with a blank.
<br><b>Why tho?</b> You can downgrade (via CoreOS swapping) and repair LoadBIOS type corruptions. You can also enable service mode!
<br><b>Why isn't this FREE?!</b> This uses a proprietary and unreleased exploit on the R78 chip. It must be pre-flashed and locked on a fresh Arduino.
<br><b>Why so expensive?</b> The target market are businesses who will dump and flash dozens of consoles, not desoldering and replacing chips is important. Theres always the <a href="https://betterwayelectronics.com.au/syscon.html">free/cheap method.</a>
<br><b>What are the benefits?</b> You only have to solder 5 wires to dump then 3 after that! No desoldering, retain and use the SCE Syscon.
<br><b>Where's the rest of the guide?</b> It is TBA, but my software handles most of the downgrade process anyways.
<br>
<h3>Shopping List</h3>
<b>Required:</b>
	<li><a href="https://buy.stripe.com/7sIeXU0Qt1ps2Z24gj"><b>BwE PS4 Syscon Writer ($180AUD) (Pre-Order Now @ Discount Price! Shipments Late December/Early 2023)</b></a>
	<li><a href="https://www.aliexpress.com/item/32841564699.html">4N35 Optocoupler ($1.35AUD)</a>
	<li><a href="https://www.aliexpress.com/item/32214404363.html">Colourful Mini Breadboard ($1AUD)</a>
	<li><a href="https://www.aliexpress.com/item/4000203371860.html">Male->Female Dupont Cables ($2AUD)</a>
	<li><a href="https://www.aliexpress.com/item/32247209964.html">47 ohm Resistor ($1AUD)</a>
	<li><a href="https://www.aliexpress.com/item/32247209964.html">4.7-5k ohm Resistor ($1AUD)</a>
	<li><a href="https://www.aliexpress.com/item/32660088529.html">1N4148/1N4448 Diode ($1AUD)</a>
	<li><a href="https://www.betterwayelectronics.com.au/downloads/Syscon.rar">Requisite Software (Reader, Writer, Verifier, Patcher)</a>
</li>
<br>
<b>Optional:</b>
	<li><a href="https://www.aliexpress.com/item/1005001437032289.html">Multi LQFP (64-100) to DIP Board ($4AUD)</a>
	<li><a href="https://www.aliexpress.com/item/1005002888994993.html">LQFP64 to DIP Board ($4AUD)</a>
	<li><a href="https://www.aliexpress.com/item/1762279813.html">LQFP64 Socket Adapter ($45AUD)</a>
	<li><a href="https://www.aliexpress.com/item/1005003352270633.html">LQFP100 Socket Adapter ($45AUD</a>
</li>
<br>
<b>Soldering, Whats That?:</b>
  <li><a href="https://www.aliexpress.com/item/4001063621549.html">T12-942 QUICKO Soldering Station (SET 5) ($58AUD)</a></li>
  <li><a href="https://www.aliexpress.com/item/1005004623323483.html">DC24v 6A Adapter for Soldering Station ($28AUD)</a></li>
  <li><a href="https://www.aliexpress.com/item/32948598235.html">Fake Amtech Flux ($7AUD)</a></li>
  <li><a href="https://www.aliexpress.com/item/1005004532993074.html">Lead Solder Low-ish Melt ($3AUD)</a></li>
  <li><a href="https://www.aliexpress.com/item/33022639575.html">Solder Wick ($1AUD)</a></li>
  <li><a href="https://www.aliexpress.com/item/1005003102463009.html">Love Heart Tweezers ($7AUD)</a></li>
  <li><a href="https://www.aliexpress.com/item/4000315816666.html">32-34AWG Cable 10m ($4.50AUD)</a></li>
</li>

<h3>Syscon Pinout</h3>

<div style="display: flex;">
  <div style="width: 420px; padding: 10px;">
    <img src="https://i.imgur.com/UnGh1ne.png" width="45%" height="45%">
    <br><b>FAT Syscon</b>
  </div>
  <div style="width: 420px; padding: 10px;">
      <img src="https://i.imgur.com/mzsNJHP.png" width="45%" height="45%">
    <br><b>Slim/Pro Syscon</b>
  </div>
</div>
<br>
<h3>Reading Syscon (Currently does NOT work on SIE INC Chips):</h3>


  <li>Connect from your Arduino to the Syscon Chip (On or Off Board)
  <li>Launch SysconReader.exe in Terminal with your COM port (Eg: SysconReader.exe COM4)
  </li>
  <br>If the dumps do not match change resistors (100ohm, 510ohm 1kohm).
  <br><br>
  <b>Wire up your Flasher:</b><br><br>
  <li>D6 -> 47 ohm Resistor -> Pin 1 4N35
  <li>D5 -> Pin 6 Pro / Pin 13 FAT
  <li>D4 -> Pin 15 Pro / Pin 22 FAT
  <li>D3 -> Pin 5 Pro / Pin 12 FAT
  <li>D2 -> Diode (-) -> D3
  <li>D3 -> Pin 4 4N35
  <li>GND -> Pin 2 4N35
  <li>GND -> Pin 14 Pro / Pin 21 FAT
  <li>TXD -> Pin 5 4N35
  <li>5V -> 4.7k ohm Resistor -> Pin4 4N35
  <li>5V -> Pin 16 Pro / Pin 23 FAT

<br>
<img src="https://i.imgur.com/y7WMewt.png" width="50%" height="50%">
<br><b>Schematic</b>
<br>
<img src="https://i.imgur.com/b4nFFP4.jpeg"  width="50%" height="50%">
<br><b>Fully Assembled</b>
<br>

<h3>Wiring To Syscon</h3>

<img src="https://i.imgur.com/E6sxlx4.jpeg" width="50%" height="50%">
<br><br>
<li>If you are dumping on board, <b>lift pin 15 and 16</b>. To do this add flux and low melt solder to the pins and let it soak in.
<li>Use tweezers and a thin tip and while applying heat to the pin push from behind with the tweezers until the pin is lifted.
<li>Wire pin 5 and 6 flat against the resistors, directly to the pins or the alternative solder points. Following best practice.
<br><br>
<li>When reading Syscon on board (after patching) wire <i>only</I> pin 5, 6 and ground either directly to the chip or alternative points.
</li>
<div style="display: flex;">

  <div style="width: 380px; padding: 10px;">
    <img src="https://i.imgur.com/oqYIJ17.jpeg" width="350px" height="350px">
    <br><b>Dumping on-board example</b>
  </div>
</div>

<h4>Best Practice</h4>
<div style="display: flex;">
  <div style="width: 320px; padding: 10px;">
    <img src="https://i.imgur.com/pjizFZc.png" width="300px" height="200px">
    <br><b>Solder the jumper wires flat against the legs.</b>
  </div>
  <div style="width: 320px; padding: 10px;">
    <img src="https://i.imgur.com/wm4PrwP.png" width="300px" height="200px">
    <br><b>The entire jumper wire must fill the entire pad.</b>
  </div>
  <div style="width: 320px; padding: 10px;">
    <img src="https://i.imgur.com/nXx3oep.png" width="300px" height="200px">
    <br><b>The wire must be parallel to the component termination.</b>
  </div>
</div>


<h3>Patching Syscon Dump:</h3>

<ol>
  <li>Run BwE PS4 NOR Validator
  <li>Select Syscon
  <li>Scan & Apply Downgrade/Service Mode Patches
  <li>Enable Debug Mode
</ol>

<img src="https://i.imgur.com/s8X8hKA.png" width="45%" height="45%">

<h3>Programming SCE Syscon:</h3>

<ol>
  <li>Connect from your Arduino to the Syscon Chip (On or Off Board)
  <li>Launch SysconWriter.exe in Terminal with your COM port (Eg: SysconWriter.exe COM4)
  <li>Select OCD mode for your first write only
  <li>Write the patched dump 
      </ol>
  </li>
  <b>Notes:</b><br>
  You now only need to connect Pins 5, 6 and GND to the Syscon directly or to the alternative points for all future reads and writes!
  <br>
  You can only write with the supplied Arduino, TTL will not function nor will Renesas Software.

<div style="display: flex;">
  <div style="width: 420px; padding: 10px;">
    <img src="https://i.imgur.com/9gaPgrL.png" width="45%" height="45%">
    <br><b>Writing Example</b>
  </div>
  <div style="width: 420px; padding: 10px;">
    <img src="https://i.imgur.com/mNjgOVx.png" width="45%" height="45%">
    <br><b>Verifying</b>
  </div>
</div>

<h3>Reading & Writing NOR:</h3>

<li>Dump the NOR using SPIWay (illustrated below) or through a CH341A or other programmer.
<li>You can either solder directly to the pins, their resistors/pads and dump/flash on-board (<b>@ ~3.0v Only</b>) or remove the chip entirely.
<li>You can also follow <a href="https://repair.wiki/w/PS4_UART_Guide">this guide</a> on the Repair Wiki in which I illustrate the process behind enabling UART (which you should do).

<img src="https://i.imgur.com/8t7iBVp.png" width="45%" height="45%">

<table border="#999" cellspacing="0" cellpadding="5" class="wikitable" style="border:1px solid #999; border-collapse: collapse;">

<tbody><tr bgcolor="#cccccc">
<th>8-Pin</th>
<th>16-pin</th>
<th>Usage</th>
<th>Teensy++ 2.0<br />SPIway</th>
<th>Description
</th></tr>
<tr>
<td>-</td>
<td>1</td>
<td>SIO3</td>
<td>B5</td>
<td>8pin: Not Available - not used / 16pin: Serial Data Input &amp; Output (for 4xI/O read mode)
</td></tr>
<tr>
<td>8</td>
<td>2</td>
<td>VCC</td>
<td>+5V pad</td>
<td>+3V DC Power Supply
</td></tr>
<tr>
<td>7</td>
<td>3</td>
<td>HOLD#/RESET#</td>
<td>B6</td>
<td>8pin: Hold, to pause the device without deselecting the device / 16pin: Hardware Reset Pin Active low
</td></tr>
<tr>
<td>-</td>
<td>4</td>
<td style="color:white; background-color:darkgrey;">NC</td>
<td style="color:white; background-color:darkgrey;">NC</td>
<td style="color:white; background-color:darkgrey;">No Connection
</td></tr>
<tr>
<td>-</td>
<td>5</td>
<td style="color:white; background-color:darkgrey;">NC</td>
<td style="color:white; background-color:darkgrey;">NC</td>
<td style="color:white; background-color:darkgrey;">No Connection
</td></tr>
<tr>
<td>-</td>
<td>6</td>
<td style="color:white; background-color:darkgrey;">NC</td>
<td style="color:white; background-color:darkgrey;">NC</td>
<td style="color:white; background-color:darkgrey;">No Connection
</td></tr>
<tr>
<td>1</td>
<td>7</td>
<td>CS#</td>
<td>B0</td>
<td>Chip Select
</td></tr>
<tr>
<td>2</td>
<td>8</td>
<td>SO/SIO1</td>
<td>B3</td>
<td>Serial Data Output (for 1 x I/O) or Serial Data Input &amp; Output (for 2x I/O or 4x I/O read mode)
</td></tr>
<tr>
<td>3</td>
<td>9</td>
<td>WP#/SIO2</td>
<td>B4</td>
<td>Write Protection: connect to GND or Serial Data Input &amp; Output (for 4x I/O read mode)
</td></tr>
<tr>
<td>4</td>
<td>10</td>
<td>GND</td>
<td>GND</td>
<td>Ground
</td></tr>
<tr>
<td>-</td>
<td>11</td>
<td style="color:white; background-color:darkgrey;">NC</td>
<td style="color:white; background-color:darkgrey;">NC</td>
<td style="color:white; background-color:darkgrey;">No Connection
</td></tr>
<tr>
<td>-</td>
<td>12</td>
<td style="color:white; background-color:darkgrey;">NC</td>
<td style="color:white; background-color:darkgrey;">NC</td>
<td style="color:white; background-color:darkgrey;">No Connection
</td></tr>
<tr>
<td>-</td>
<td>13</td>
<td style="color:white; background-color:darkgrey;">NC</td>
<td style="color:white; background-color:darkgrey;">NC</td>
<td style="color:white; background-color:darkgrey;">No Connection
</td></tr>
<tr>
<td>-</td>
<td>14</td>
<td style="color:white; background-color:darkgrey;">NC</td>
<td style="color:white; background-color:darkgrey;">NC</td>
<td style="color:white; background-color:darkgrey;">No Connection
</td></tr>
<tr>
<td>5</td>
<td>15</td>
<td>SI/SIO0</td>
<td>B2</td>
<td>Serial Data Input (for 1 x I/O) or Serial Data Input &amp; Output (for 2x I/O or 4x I/O read mode)
</td></tr>
<tr>
<td>6</td>
<td>16</td>
<td>SCLK</td>
<td>B1</td>
<td>Clock Input
</td></tr>
</tbody></table>

<br>
<div style="display: flex;">
  <div style="width: 320px; padding: 10px;">
    <img src="https://www.psdevwiki.com/ps4/images/thumb/f/fa/MX25L1006E_Pinout.png/800px-MX25L1006E_Pinout.png" width="45%" height="45%">
    <br><b>8 Pin WSON8 - Pro & Slim</b>
  </div>
  <div style="width: 320px; padding: 10px;">
    <img src="https://www.psdevwiki.com/ps4/images/thumb/c/cd/MX25L25635FMI-10G_Pinout.png/800px-MX25L25635FMI-10G_Pinout.png" width="45%" height="45%">
    <br><b>16 Pin SOP16 - Fat</b>
  </div>
</div>
<br>
<div style="display: flex;">
  <div style="width: 320px; padding: 10px;">
    <img src="https://i.imgur.com/cI0WcwT.jpeg" width="45%" height="45%">
    <br><b>Hardwiring Example</b>
  </div>
  <div style="width: 320px; padding: 10px;">
    <img src="https://i.imgur.com/wPHOhBY.jpeg" width="45%" height="45%">
    <br><b>Non-Invasive Method</b>
  </div>
    <div style="width: 320px; padding: 10px;">
    <img src="https://i.imgur.com/wtgghfk.jpeg" width="45%" height="45%">
    <br><b>2.8v CH341A Mod</b>
  </div>
</div>


<h3>Patching NOR Dump:</h3>

<ol>
  <li>Run BwE PS4 NOR Validator</li>
  <li>Select NOR</li>
   <li>Validate NOR</li>
  <li>Patch and Swap CoreOS</li>
  <li>Enable UART Mode</li>
</ol>

<img src="https://i.imgur.com/OKeE5Mm.png" width="65%" height="65%">

<h3>Credits/Greetz:</h3>
DARKNESMONK
  <br>PDJ
  <br>Hoea
  <br>Donators & Suppliers of Dumps/Syscons
