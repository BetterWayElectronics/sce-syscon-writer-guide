
<h2>Syscon Guide - SCE Syscon Method</h2>
<b>Last Updated 16/6/23</b>
<br><br>
<li><b>What is this?</b> This is a tool to read and write your PS4's Syscon on-board (and off-board) without the need to replace it with a blank (the now considered 'old way').
<li><b>Why do I need this?</b> Modifying the Syscon allows for downgrading (via CoreOS swap), repairing of loadBios -8 type errors and enables service mode.
<li><b>Why isn't this free?</b> This uses a proprietary and unreleased exploit on the R78 chip. It must be pre-flashed and locked on a fresh Arduino. The target market are repariers, hence the price.
<li><b>Is there a cheaper way?</b> Yes, here is the <a href="https://betterwayelectronics.com.au/syscon.html">free/cheap method</a> - it requires replacing Sony's Syscon with blank RL78 chips.
<li><b>Is this difficult to install?</b> You have to solder 1 lifted wire to the Syscon whilst on-board and 3 others to alternative points. Once glitched you drop that pin and keep rest of the alternative points on the board.
<li><b>Any discounts?</b> If you buy in bulk, yes.
<li><b>Do you need a backup of the previous version syscon?</b> No you don't need a backup of anything to do this downgrade process, you are switching slots!

<li><b>Can I go from 10.50 to 9.00?</b> Only if 9.00 was your PREVIOUS firmware.
<li><b>Can I go from 10.01 to 9.00?</b> Only if 9.00 was your PREVIOUS firmware.
<li><b>Can I go from 9.50 to 9.00?</b> Only if 9.00 was your PREVIOUS firmware.
<li><b>Can I go from 9.00 to 5.50?</b> Only if 5.50 was your PREVIOUS firmware.
<li><b>Which firmware will I go back to?</b> Whichever was your PREVIOUS firmware.

</li>

<style>
    .thumbnail-container {
        position: relative;
    }
    .thumbnail-text {
        position: absolute;
        top: 20%;
        left: 50%;
        transform: translate(-60%, -60%);
        color: white;
        text-align: center;
        font-size: 0.8rem;
    }
</style>

<h3>Video Guides</h3>
<a href="https://www.youtube.com/watch?v=hcmMSYmwSUQ/" class="thumbnail-container">
    <img src="https://i.ytimg.com/vi/hcmMSYmwSUQ/hqdefault.jpg" alt="Video thumbnail" width="320" height="180">
    <div class="thumbnail-text">English</div>
</a>
<a href="https://www.youtube.com/watch?v=q1F0AL3ttjY/" class="thumbnail-container">
    <img src="https://i.ytimg.com/vi/q1F0AL3ttjY/hqdefault.jpg" alt="Video thumbnail" width="320" height="180">
    <div class="thumbnail-text">Portuguese</div>
</a>
<a href="https://www.youtube.com/watch?v=W7RpkG5hiA0/" class="thumbnail-container">
    <img src="https://i.ytimg.com/vi/W7RpkG5hiA0/hqdefault.jpg" alt="Video thumbnail" width="320" height="180">
    <div class="thumbnail-text">Hindi/Urdo</div>
</a>



<h3>Shopping List</h3>
	<li><a href="https://betterwayelectronics.com.au/bweps4sysconwriter"><b>BwE PS4 Syscon Writer</b></a>
	<li><a href="https://betterwayelectronics.com.au/downloads/BwE_PS4_Syscon_Software.rar">BwE PS4 Syscon Software (Reader & Writer) (Free w/ Writer)</a>
	<li><a href="https://betterwayelectronics.com.au/downloads/BwE_PS4_NOR_Validator.rar">BwE PS4 NOR Validator</a>
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

								<h3>Purchase Links:</h3>
									<div style="font-size: 18px; display: flex; flex-wrap: wrap;">
										<div style="width: 340px; padding: 10px;">
											<a href="https://buy.stripe.com/cN2030dDfece8jm9AO">
												<img src="https://i.imgur.com/ZjZmLLC.jpeg" width="90%" height="70%">
											</a>
											<br>
											<a href="https://buy.stripe.com/28o9DAdDfgkm8jmdRn"><b>Syscon Writer Blue Edition <span style="color:green">(New!)</span></b></a>
											<br>Voltage Switch, UART Mode, Faster Processor, Fully Integrated Design. Warranty!
											<br><b>$385AUD (233Euro, $252USD)</b>
										</div>
										
										<div style="width: 320px; padding: 10px;">
											<a href="https://buy.stripe.com/cN2030dDfece8jm9AO">
												<img src="https://i.imgur.com/HpX4doh.jpeg" width="90%" height="70%">
											</a>
											<br>
											<a href="#hardware"><b>Syscon Writer Black Edition <span style="color:red">(SOLD OUT & DISCONTINUED!)</span>)</b></a>
											<br>Presoldered Daughterboard - Easier Connections 
											<br><b><s>$340AUD (210Euro, $225USD)</s></b>
										</div>
									</div><br><br>
									<h3>Discount Models (Limited Stock):</h3>
									<div style="font-size: 16px; display: flex; flex-wrap: wrap;">
										<div style="width: 340px; padding: 10px;">
											<a href="https://buy.stripe.com/eVa8zwbv7c46czC6oR">
												<img src="https://i.imgur.com/CN0lt06.jpeg" width="80%" height="60%">
											</a>
											<br>
											<a href="https://buy.stripe.com/eVa8zwbv7c46czC6oR"><b>Prototype Syscon Writer Purple Edition <span style="color:yellow">(Refurbished)</span></b></a>
											<br>Voltage Switch, Faster Processor, Fully Integrated Design. Fully Functional! No Warranty!
											<br><b>$300AUD (180Euro, $198USD)</b>

										  </div>
										  
										<div style="width: 320px; padding: 10px;">
											<a href="https://buy.stripe.com/4gw7vsar3fgi0QU8wU">
												<img src="https://i.imgur.com/xWVXO0C.jpeg" width="80%" height="60%">
											</a>
											<br>
											<a href="https://buy.stripe.com/4gw7vsar3fgi0QU8wU"><b>Prototype Error Edition <span style="color:red">(Non-Functional, Requires Repair)</span></b></a>
											<br>Voltage Switch, Faster Processor, Fully Integrated Design. Includes Repair Instructions! No Warranty!
											<br><b>$250AUD (150Euro, $165USD)</b>
										</div>
										
									</div>
				
								<b>Note: All Syscon Writers Come With HWID Locked <a href="#software">Syscon Writer & Reader Software</a> For Free!</b><br>(Available with USB License for Multi-PC Use)
								<br>



<h3>Compatibilitiy</h3>
<img src="https://i.imgur.com/4fpFJvI.jpg" width="50%" height="50%"><br>
Do you have the Syscon on the right? You're outta luck. The glitch only works on Renesas RL78 chips. The guide ends here.<br>
<b>The chip MUST have A0#-COL or A0#-COL2 where the # is a number.</b>

<h3>Syscon Pinout</h3>

<div style="display: flex;">
  <div style="width: 420px; padding: 10px;">
    <img src="https://i.imgur.com/UnGh1ne.png" width="100%" height="100%">
    <br><b>FAT Syscon</b>
  </div>
  <div style="width: 420px; padding: 10px;">
      <img src="https://i.imgur.com/mzsNJHP.png" width="100%" height="100%">
    <br><b>Slim/Pro Syscon</b>
  </div>
</div>
<br>

<img src="https://i.imgur.com/frGD9v1.jpeg" width="100%" height="100%">
<br><b>Connection Points</b>


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
<img src="https://i.imgur.com/9dgSPfr.png" width="55%" height="55%">
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
    <img src="https://www.psdevwiki.com/ps4/images/thumb/f/fa/MX25L1006E_Pinout.png/800px-MX25L1006E_Pinout.png" width="90%" height="90%">
    <br><b>8 Pin WSON8 - Pro & Slim</b>
  </div>
  <div style="width: 320px; padding: 10px;">
    <img src="https://www.psdevwiki.com/ps4/images/thumb/c/cd/MX25L25635FMI-10G_Pinout.png/800px-MX25L25635FMI-10G_Pinout.png" width="90%" height="90%">
    <br><b>16 Pin SOP16 - Fat</b>
  </div>
</div>
<br>
<div style="display: flex;">
  <div style="width: 320px; padding: 10px;">
    <img src="https://i.imgur.com/cI0WcwT.jpeg" width="90%" height="90%">
    <br><b>Hardwiring Example</b>
  </div>
  <div style="width: 320px; padding: 10px;">
    <img src="https://i.imgur.com/wPHOhBY.jpeg" width="90%" height="90%">
    <br><b>Non-Invasive Method</b>
  </div>
    <div style="width: 320px; padding: 10px;">
    <img src="https://i.imgur.com/wtgghfk.jpeg" width="90%" height="90%">
    <br><b>2.8v CH341A Mod</b>
  </div>
   <div style="width: 320px; padding: 10px;">
    <img src="https://i.imgur.com/V06INO1.png" width="90%" height="90%">
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

<b>There are <b>three</b> methods, pick whichever suits you! The third is the quickest, but not as tested as the others</b>
<br><br>
<b>Official Method:</b><br>
<li>Patch the UART patched NOR with the CoreOS patch
<li>Boot console and read UART log
<li>If UART log says "checkUpdVersion 0xffffffff != 0x(Lower Firmware)" <b>and</b> has a lower Secure Loader firmware...
<li>You can then write the Syscon patch to the console
<li>If not, try another patch and repeat the process (you must try ALL patches)
<li>On success the console will boot to safe mode and prompt to install lower firmware (recovery).
<br><br>
<b>Lazy Method (No UART Needed)</b><br>
<li>Patch the NOR with CoreOS patch
<li>Write the Syscon patch to the console
<li>If the console does not boot...
<li>Repeat first two steps, pick a new Patch for NOR (you must try ALL patches) and re-use the same patch for Syscon.
<li>On success the console will boot to safe mode and prompt to install lower firmware (recovery).
<br><br>
<b>New Method (Legitimate CoreOS Patch)</b><br>
<li>Dump NOR & Syscon (keep, do not delete)
<li>Update Console to <b>SAME</b> firmware (if 9.03, install 9.03 again etc) via safemode
<li>Dump NOR again after update but rename and add '_updated_coreos' to the end of the file name (Example: nor1.bin is now nor1_updated_coreos.bin)
<li>Run NOR Validator and select the <b>first</b> dump you made. In the CoreOS patcher (Option 5) you can now select Generate Legitimate Patch (Option 3)
<li>Program will output your dump with the name '_patched_coreos' (Example: nor1.bin is now now1_patched_coreos.bin)
<li>Upload the newly patched dump back to the PS4 along with a <b>patched</b> copy of the <b>original</b> Syscon
<br>
<br><b>Troubleshooting:</b>
<br>
<li>If you still have loadBios -8 and the Bootloader version has changed you have an issue with your RAM, replace and or repair it.
<li>If you have errors about wrong version at the bottom of the UART log, you need to patch your Southbridge.
<li>How can you see the previous firmware? Upload only the patched Syscon and read UART. Standby Version = Previous Firmware
<li>Why so many CoreOS patches? Because CoreOS is encrypted, we cannot make a real patch, we are corrupting it in a way that allows it to think the value is real. Different consoles behave differently so there is now 14 patches. Luckily there is a new method (see above) which is signifigantly quicker, it uses the legitimate header value from an update (even if its the same firmware) and it patches that on your old dump.
<li>The standby version and or the release version has changed, but the console still just says checkUpdVersion 0xfffff etc. This is because the Syscon patch has failed, you need to use the <a href="/sysconrebuilder"><b>Syscon Rebuilder</b></a> to rebuild the syscon and patch it with the -2 patch (Option 4), this will remove the error.
<br>

<style>
.secure-loader {
  background-color: #FFFFCC;
}
</style>
<br><br>
<b>How Does It Look From UART?</b>
<br>
<li><b>Patch 1</b><br><span class="secure-loader">secure loader build: May 10 2022 05:23:21 (r10568:release_branches/release_09.600) [711MHz]</span>
<br>Boots Normally (Fail)
<li><b>Patch 2</b><br><span class="secure-loader">secure loader build: May 10 2022 05:23:21 (r10568:release_branches/release_09.600) [711MHz]</span>
<br>Boots Normally (Fail)
<li><b>Patch 3</b><br><span class="secure-loader">secure loader build: May 10 2022 05:23:21 (r10568:release_branches/release_09.600) [711MHz]</span>
<br>Boots Normally (Fail)
<li><b>Patch 4</b><br><span class="secure-loader">secure loader build: May 10 2022 05:23:21 (r10568:release_branches/release_09.600) [711MHz]
<br>ERROR: main(4122) loadBios -8</span>
<br>BLOD (Fail)
<li><b>Patch 5</b><br><span class="secure-loader">secure loader build: May 10 2022 05:23:21 (r10568:release_branches/release_09.600) [711MHz]</span>
<br>Boots Normally (Fail)
<li><b>Patch 6</b><br><span class="secure-loader">secure loader build: May 10 2022 05:23:21 (r10568:release_branches/release_09.600) [711MHz]</span>
<br>Boots Normally (Fail)
<li><b>Patch 7</b><br><span class="secure-loader">secure loader build: May 10 2022 05:23:21 (r10568:release_branches/release_09.600) [711MHz] 
<br>ERROR: main(3738) checkUpdVersion 0xffffffff != 0x9600000</span>
<br>Slot Switched To Current Slot (Fail)
<li><b>Patch 8</b><br><span class="secure-loader">secure loader build: Sep  1 2021 05:19:44 (r10468:release_branches/release_09.000) [711MHz]
<br>ERROR: main(3738) checkUpdVersion 0xffffffff != 0x9008000</span>
<br><b>Secure Loader & CheckUpdVersion Lower = Success!! Patch Syscon Now!</b>
<li><b>After Syscon Patch</b><br><span class="secure-loader">secure loader build: Sep  1 2021 05:19:44 (r10468:release_branches/release_09.000) [711MHz]
<br>standby 09600000</span>
<br><b>9.00 Secure Loader and 9.60 Standby. Slots successfully switched! Booting into 9.00!</b>

<h3>Getting Support</h3>
If you want support from BwE, you must provide a UART log for each NOR patch (without flashing Syscon) then another with only the patched Syscon.
<br>That means a <b>total of 15 logs</b>, they must be labelled to represent each patch number and in .txt format. Zip it and email it/message it to me. 
<br><b>If you do not do this, I will not provide support</b>

<h3>Credits/Greetz:</h3>
DarkNESMonk
<br>Wildcard
<br>fail0verflow
<br>JEFF
  <br>PDJ
  <br>Hoea
  <br>Donators & Suppliers of Dumps/Syscons
