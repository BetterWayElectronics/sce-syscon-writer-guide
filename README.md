

<h2>Syscon Guide - SCE Syscon Method</h2>
<b>Last Updated 2/2/23</b>
<br><br>
<li><b>What is this?</b> This is a tool to read and write your PS4's Syscon on-board (and off-board) without the need to replace it with a blank (the now considered 'old way').
<li><b>Why do I need this?</b> Modifying the Syscon allows for downgrading (via CoreOS swap), repairing of loadBios -8 type errors and enables service mode.
<li><b>Why isn't this free?</b> This uses a proprietary and unreleased exploit on the R78 chip. It must be pre-flashed and locked on a fresh Arduino. The target market are repariers, hence the price.
<li><b>Is there a cheaper way?</b> Yes, here is the <a href="https://betterwayelectronics.com.au/syscon.html">free/cheap method</a> - it requires replacing Sony's Syscon with blank RL78 chips.
<li><b>Is this difficult to install?</b> You have to solder 1 lifted wire to the Syscon whilst on-board and 3 others to alternative points. Once glitched you drop that pin and keep rest of the alternative points on the board.
<li><b>Any discounts?</b> If you buy in bulk, yes.
<li><b>Video Guide?</b> <a href="https://www.youtube.com/watch?v=hcmMSYmwSUQ">On my YouTube</a>
</li>

<h3>Shopping List</h3>
<b>Required:</b>
	<li><a href="https://betterwayelectronics.com.au/bweps4sysconwriter"><b>BwE PS4 Syscon Writer ($300AUD) (In Stock Now!)</b></a>
		<li><a href="https://www.aliexpress.com/item/32273550144.html?mp=1">FT232RL TTL Serial Module (For UART) ($2AUD)</a>
	<li><a href="https://www.aliexpress.com/item/32841564699.html">4N35 Optocoupler ($1.35AUD)</a>
	<li><a href="https://www.aliexpress.com/item/32214404363.html">Colourful Mini Breadboard ($1AUD)</a>
	<li><a href="https://www.aliexpress.com/item/4000203371860.html">Male->Female Dupont Cables ($2AUD)</a>
	<li><a href="https://www.aliexpress.com/item/32247209964.html">47 ohm Resistor ($1AUD)</a>
	<li><a href="https://www.aliexpress.com/item/32247209964.html">4.7-5k ohm Resistor ($1AUD)</a>
	<li><a href="https://www.aliexpress.com/item/32660088529.html">1N4148/1N4448 Diode ($1AUD)</a>
	<li><a href="https://betterwayelectronics.com.au/downloads/BwE_PS4_Syscon_Software.rar">BwE PS4 Syscon Software (Reader & Writer) (Updated 7/1/23)</a>
	<li><a href="https://betterwayelectronics.com.au/downloads/BwE_PS4_NOR_Validator.rar">BwE PS4 NOR Validator v1.9.9 (Updated 7/1/23)</a>
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

<h3>Compatibilitiy</h3>
<img src="https://i.imgur.com/4fpFJvI.jpg" width="50%" height="50%"><br>
Do you have the Syscon on the right? You're outta luck. The glitch only works on Renesas RL78 chips. The guide ends here.<br>
<b>The chip MUST have A0#-COL or A0#-COL2 where the # is a number.</b>

<h3>Syscon Pinout</h3>

<div style="display: flex;">
  <div style="width: 420px; padding: 10px;">
    <img src="https://i.imgur.com/UnGh1ne.png" width="50%" height="50%">
    <br><b>FAT Syscon</b>
  </div>
  <div style="width: 420px; padding: 10px;">
      <img src="https://i.imgur.com/mzsNJHP.png" width="50%" height="50%">
    <br><b>Slim/Pro Syscon</b>
  </div>
</div>
<br>

<h3>Wiring To Syscon</h3>

  <b>Pinout</b><br><br>
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

<div style="display: flex;">
  <div style="width: 620px; padding: 10px;">
    <img src="https://i.imgur.com/y7WMewt.png" width="70%" height="70%">
    <br><b>Schematic 1</b>
  </div>
  <div style="width: 620px; padding: 10px;">
    <img src="https://i.imgur.com/c3lVUa8.jpg" width="70%" height="70%">
    <br><b>Schematic 2</b>

  </div>
</div>

<br>

<img src="https://i.imgur.com/wGuXI7O.jpg" width="70%" height="70%">
<br><b>Connection Points</b>
<br>
<img src="https://i.imgur.com/v3cesIO.jpg"  width="50%" height="50%">
<br><b>Fully Assembled</b>

<br><br>
<b>Dumping On-Board</b><br>
<li>If you are dumping on board, <b>lift pin 15 (Pro) or pin 22 (Fat)</b>. To do this add flux and low melt solder to the pins and let it soak in.
<li>Use tweezers and a thin tip and while applying heat to the pin push from behind with the tweezers until the pin is lifted.
<li>Wire pin 5 and 6 flat against the resistors, directly to the pins or the alternative solder points. Following best practice.
<li>You do not have to wire pin 16 as you can have the console on standby mode.
<br><br>
<b>Dumping Off-Board</b><br>
<li>To remove the Syscon chip entirely, apply flux to all of the pins and flood them with low melt solder (chipquik if not using hot air).
<li>Apply 480c at 40% pressure from a height of approximately 15cm until the solder is visibly liquidous on all sides.
<li>Pull up the chip with an SMD vacuum pen.
<li>Tin the pads on the PS4 with low melt solder.
<li>Clean pins 1-16 on the Syscon of any solder bridges and solder to pre-tinned breakout board (or place into DIP socket).
<br><br>
<li>When reattaching the Syscon first apply a light layer of flux on the already tinned pads.
<li>Line up Syscon appropriately or solder each corner manually to ensure the chip does not move during reflow.
<li>Apply 480c at 40% pressure from a height of approximately 20cm and slowly drop until you see flux bubble/move and solder shine/glimmer.
<li>If you do not want to use hot air, use drag soldering technique or manually solder each pin individually with thin tip tinned with low melt solder.
<br>
<br>Note: When reading/writing Syscon on-board (<b>after patching</b>) wire only pin 5, 6 and ground either directly to the chip or alternative points and have the console on standby.

</li>
<div style="display: flex;">

  <div style="width: 380px; padding: 10px;">
    <img src="https://i.imgur.com/Pkq9Oha.jpg" width="750px" height="650px">
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

<h3>Reading Syscon (Currently ONLY works on A0#-COL/2 chips):</h3>
<img src="https://i.imgur.com/zV8EvTU.png" width="55%" height="55%">

  <li>Connect from your Arduino to the Syscon Chip (See Wiring To Syscon Below)
  <li>Launch BwE_PS4_Syscon_Reader.exe, it will auto detect your COM port or prompt you for one.
  <li>It will glitch the chip (if this is your first read and you have not enabled OCD mode) and then dump!
  <li>It will then re-dump and compare in order to validate them.
  </li>
  <br>If the dumps do not match change resistors (100ohm, 510ohm, 1kohm).
  <br>If it does not even dump check your connections (seriously) or change your Optocoupler.


<h3>Patching Syscon Dump:</h3>

<ol>
  <li>Run BwE PS4 NOR Validator
  <li>Select Option 2 - Scan & Patch PS4 Syscon
  <li>Optional: Select Verbose Mode (Only required for Manual Patching)
  <li>Syscon will scan for a patchable slot, if there is one available it will say at the bottom in "Final Results".
  <li>If it says "Active Slot Patchable" select Option 1 "Auto Patch"
  <li>If it says "Unable to Auto-Patch" it will prompt you to Manually Patch - If so you must select an earlier 080B (Use Verbose Mode) to overwrite the last 080B.
  <li>If it says "Syscon NOT Patchable" then call it quits, game over. Your PS4 has either had its initialisation overwritten or some other historical event is blocking the patch.
  <li>Apply the patch!
  <li>It will show you what you are overwriting (and potentially the data you are overwriting it with).
  <li>File will be saved as "???_080B_patched.bin" - Keep this and the original, label it appropriately and store it!
</ol>

<img src="https://i.imgur.com/s8X8hKA.png" width="45%" height="45%">

<h3>Programming SCE Syscon:</h3>
<img src="https://rimgo.pussthecat.org/N9KR6jI.png" width="55%" height="55%">
<ol>
  <li>Connect from your Arduino to the Syscon Chip (<b>lift pin 15 and 16 (Pro) or pin 22 and 23 (Fat)if writing on board</b>).
  <li>Launch BwE_PS4_Syscon_Writer.exe it will auto detect your COM port or prompt you for one.
  <li>Select OCD mode for your first write only, this will disable the need to lift pins ever again! 
  <li>Write the patched dump (or original if you only want to enable OCD mode) 
  <li>If you selected confirm it will check the dump was written correctly - If there was an error, restart the Arduino and run full and OCD mode (regardless if you have done it before or not).
  <li><b>Do NOT boot the console with patched syscon until you have ALSO patched the NOR.</b>
      </ol>
  </li>
  <b>Notes:</b><br>
  You now only need to connect Pins 5, 6 and GND to the Syscon directly or to the alternative points for all future reads and writes!
  <br>
  You can only write with the supplied Arduino, TTL will not function nor will Renesas Software.<br>
  <b>All future writes do not require full or OCD commands (this will make it only write to 0x60000+)</b>, but I highly suggest adding confirm to validate the write.

<div style="display: flex;">
  <div style="width: 420px; padding: 10px;">
    <img src="https://i.imgur.com/9gaPgrL.png" width="50%" height="50%">
    <br><b>Writing Example</b>
  </div>
  <div style="width: 420px; padding: 10px;">
    <img src="https://i.imgur.com/mNjgOVx.png" width="50%" height="50%">
    <br><b>Verifying</b>
  </div>
</div>

<h3>Reading & Writing NOR:</h3>

<li>Dump the NOR using SPIWay (illustrated below) or through a CH341A or something faster like the XGECU (illustrated below).
<li>You can either solder directly to the pins, their resistors/pads and dump/flash on-board (<b>@ ~3.0v Only</b>) or remove the chip entirely, I highly recommend just removing the chip entirely.
<li>You can also follow <a href="https://repair.wiki/w/PS4_UART_Guide">this guide</a> on the Repair Wiki in which I illustrate the process behind enabling UART (<b>I recommend you do this</b>).
<br><br>
<img src="https://i.imgur.com/6fbidS0.jpg" width="50%" height="50%">
<br><b>XGECU</b><br>
<img src="https://i.imgur.com/FJdxQpj.jpg" width="50%" height="50%">
<br><b>CH341A (Modified for 2.8v)</b><br>

<img src="https://i.imgur.com/8t7iBVp.png" width="45%" height="45%">
<br><b>Teensy (SPIWay)</b><br>
<br><br>

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
    <img src="https://www.psdevwiki.com/ps4/images/thumb/f/fa/MX25L1006E_Pinout.png/800px-MX25L1006E_Pinout.png" width="50%" height="50%">
    <br><b>8 Pin WSON8 - Pro & Slim</b>
  </div>
  <div style="width: 320px; padding: 10px;">
    <img src="https://www.psdevwiki.com/ps4/images/thumb/c/cd/MX25L25635FMI-10G_Pinout.png/800px-MX25L25635FMI-10G_Pinout.png" width="50%" height="50%">
    <br><b>16 Pin SOP16 - Fat</b>
  </div>
</div>
<br>
<div style="display: flex;">
  <div style="width: 320px; padding: 10px;">
    <img src="https://i.imgur.com/cI0WcwT.jpeg" width="50%" height="50%">
    <br><b>Hardwiring Example</b>
  </div>
  <div style="width: 320px; padding: 10px;">
    <img src="https://i.imgur.com/wPHOhBY.jpeg" width="50%" height="50%">
    <br><b>Non-Invasive Method</b>
  </div>
    <div style="width: 320px; padding: 10px;">
    <img src="https://i.imgur.com/wtgghfk.jpeg" width="50%" height="50%">
    <br><b>2.8v CH341A Mod</b>
  </div>
   <div style="width: 320px; padding: 10px;">
    <img src="https://i.imgur.com/V06INO1.png" width="50%" height="50%">
    <br><b>2.8v CH341A Mod</b>
  </div>
</div>


<h3>Patching NOR Dump:</h3>

<ol>
  <li>Run BwE PS4 NOR Validator</li>
  <li>Select Option 1 "Validate or Patch PS4 NOR"1</li>
  <li>Select your NOR file</li>
  <li>Select Option 9 "Validate" and patch for UART when prompted</li>
  <li>If your NOR is valid go back and select Option 5 "Patch CoreOS & Southbridge (LoadBios & Downgrading)"</li>
  <li>Read the warnings!</li>
  <li>Select Option 1 "Patch SB Flag, CoreOS Header & UART"</li>
  <li>Select CoreOS Header Patch (Or choose Auto) - There are multiple choices as each console may behave differently with each patch, just go with the first.
  <li>NOR will be saved as "?_sb-coreos-uart-patched_*_**.bin"</li>
  <li><b>Do NOT boot the console with patched NOR until you have ALSO backed up and or patched the Syscon.</b>

</ol>

<img src="https://i.imgur.com/d7ANNtH.png" width="65%" height="65%">

<h3>Final Step - LoadBios Repair / Downgrade:</h3>

There are two methods, both are basically the same so pick whichever suits you!
<br><br>
<li>Patch the UART patched NOR with the SB & CoreOS patch of your choice
<li>Boot console and read UART log
<li>If UART log says "CheckUpdVersion" AND OR the Bootloader version has changed...
<li>Write the Syscon patch to the console
<li>If not, try another patch and repeat the process
<li>On success the console will boot to safe mode and prompt to install lower firmware (recovery).
<br>
<br>The other method:
<br><br>
<li>Patch the NOR with SB & CoreOS patch of your choice
<li>Write the Syscon patch to the console
<li>If the console does not boot...
<li>Repeat first two steps, pick a new Patch for NOR and keep the same patch for Syscon.
<li>On success the console will boot to safe mode and prompt to install lower firmware (recovery).
<br>
<br>Troubleshooting:
<br><br>
<li>If you still have loadBios -8 and the Bootloader version has changed you have an issue with your RAM, replace and or repair it.
<li>If you have BlStorageHeader error, you did not follow my instructions and have soft bricked your syscon, I will have to patch for you -- for $$$$ (or wait for update to my software).
<br>
<h3>Credits/Greetz:</h3>
DARKNESMONK
  <br>PDJ
  <br>Hoea
  <br>Donators & Suppliers of Dumps/Syscons
