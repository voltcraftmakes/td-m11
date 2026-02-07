TIDradio TD-M11 FRS/GMRS/PMR446 radio<br>
<br>
This is detailed notes for the <a href="https://youtube.com/playlist?list=PLtvm4lCCHoKhjR_rtdxlchr7XDJ9G2VnH">VCmakes Youtube video series</a> tearing into this radio.

# Videos
<table>
<tr>
  <td>
  <a href="https://youtu.be/o2LUXxH6YpM">Video #1<Br>2026-02-04</a></td>
<td>
Everything we know up to this point about the M11 Radio.  We tear it open, analyze the major components and then review all of the methods of programing and configuring the radio.  We look at the FCC test reports and then the accessories for sale and the current cost of different options and bundles in the market.
</td>
</tr>
<tr>
  <td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=5s">Teardown<br>[0:05] </a> </td>
  <td>Pry cover off back, starting from bottom <br>
  Remove battery<br>
  Remove 6 torque screws: 2 at bottom, 2 beside label, 2 at top, can use small flathead scewdriver if you do not have the correct torx bit<br>
  Pry face of radio off<br>
  Optional - remove power/volume knob<br>
  Remove power/volume flex circuit by lifting tab on connector and lifting cable out<br>
  Gently pry board away from housing, push down at antenna end to seperate from case<br>
  Optional - unsolder charge contacts, mic, speaker<br>
  Optional - remove retainer ring from ptt/volume switch to remove switch  </td>
</tr>
<tr><td>
  <a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=318s">PCB High Res Pictures<br>[5:18]</a></td>
<td><img src="https://github.com/voltcraftmakes/td-m11/blob/main/docs/PCB-M11-back.JPG" width="200"> <img src="https://github.com/voltcraftmakes/td-m11/blob/main/docs/PCB-M11-front.JPG" width="200"> <img src="https://github.com/voltcraftmakes/td-m11/blob/main/docs/PCB-M11-side.JPG" width="200"><br>
 PCB: TD-M11_1.4 20231130<br>
 PCB: TD-M11-PTT_V1.0 20241224<br>
  </td></tr>
<tr><td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=333s">IC Chip Analysis<br>[5:33]</a></td>
  <td>
    <b>8002D Audio Amplifier</b><br>
    <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/8002D%20HAA8002D.PDF">8002D HAA8002D.PDF</a><br>
    <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/8002D%20HXJ8002_Miniature_Audio_Amplifier_Datasheet.pdf">8002D HXJ8002_Miniature_Audio_Amplifier_Datasheet.pdf</a><br>
    <br>
    <b>H0602C RF Amplifier</b><br>
      <A href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/h0602c.pdf">h0602c.pdf</A><br>
      <br>
  <b>Beken BK4819 Analog/DSP Two Way Radio IC</b><br>
      <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/BK4819_Datasheet_V1.0.pdf">BK4819_Datasheet_V1.0.pdf</a><br>
      <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/BK4819(V3)%20Application%20Note%2020210428.pdf">BK4819(V3) Application Note 20210428.pdf</a><br>
      <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/BK4819V3Registers_List_20201218.pdf">BK4819V3Registers_List_20201218.pdf</a><br>
    <br>
  <b>Telink EP2T45F10ER Bluetooth LE 5.3 </b><Br>
    <a href="https://device.report/telink-semiconductor-shanghai/ep2t45f10er">Certification EP2T45F10ER telink semiconductor shanghai co l t d</a> shows Declaration ID D067493 with QUID 236357 is also used for TLSR8208 part ends in B,C,D,G,J depending on package size, Sram, Flash. Hardware version: TLSR, released 2023-06-2, cert date 2024-03-28 very likely datasheet for TLSR8208 is close match to EP2T45F10ER.<br>
    <a href="https://products.telink-semi.cn/#/">Telink part selector</a><br>
    <a href="https://www.telink-semi.com/products/bluetooth-le/tlsr8208">Telink TLSR8208 product page</a><br>
    <a href="https://products.telink-semi.cn/#/parIndex?id=80">Telink TLSR8208B product page</a><br>
    <a href="https://wiki.telink-semi.cn/wiki/chip-series/TLSR8208-Series/"> Telink TLSR8208 series page</a><br>
    <a href="https://doc.telink-semi.cn/doc/en/application_note/res/home/bulb_tlsr8208/lighting_sdk_developer_handbook_en/">TLSR8208 Lighting example</a><br>
    <a href="https://doc.telink-semi.cn/doc/en/software/res/sdk/ble/b80_ble_otp_en/b80_ble_otp_en/">TLSR820x BLE SDK</a><br>
    <a href="https://github.com/telink-semi/tc_ble_simple_sdk/releases/tag/V3.4.2.2">TLSR8208 Github</a><br>
    <br>
  <b>Honor HBM32G003TS20 MCU ARM Cortex M0 48Mhz, 64K Flash, 2K Ram TSSOP20</b><br>
    16 IO, 9ADC, 2 Timer, 3PWM, 1 of IWDT, UART, SPI, I2C Temp:-45C to 85C<br>
    VDD:2.3-3.6V, lower power mode 0.6uA<br>
    <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/HBM32G003%E6%95%B0%E6%8D%AE%E6%89%8B%E5%86%8CV1.5.pdf">HBM32G003数据手册V1.5.pdf</a><br>
    <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/HBM32G003%E6%95%B0%E6%8D%AE%E6%89%8B%E5%86%8CV1.5.zh-CN.en.pdf">HBM32G003数据手册V1.5.zh-CN.en.pdf</a><Br>
    <br>
  <b>Titan TM1652 LED/Display driver</b><br>
    <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/TM1652%20C52186.pdf">TM1652 C52186.pdf</a><Br>
    <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/TM1652%20C52186.zh-CN.en.pdf">TM1652 C52186.zh-CN.en.pdf</a><br>
    <br>
  <b>Switch Metal Dome</b><br>
  <A href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/metal-dome-catalog.pdf">metal-dome-catalog.pdf</A></br>
    </td>
</tr>
<tr><td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=920s">Radio Modes<br>[15:20]</a></td>
<td>
  <b>Radio Shortcuts</b> - set channel to 1,2,3,4,5,15 and hold a combination of [PTT], [CH+], [CH-] and power radio on, releasing keys after radio has boot triggers actions:<br><br>
<b>CH1</b> Power on + [PTT] = Crack CTCSS tone, use [CH+]/[CH-] to select channel to crack, transmit with other radio, Crack successful after beep. Note:Radio will not match CTCSS frequency exactly it may be 1-2hz or more off.<br>
<b>CH2</b> Power on + [PTT] = Clone Radio, Transmit<br>
<b>CH3</b> Power on + [PTT] = Clone Radio, Receive (this radio has memory overwritten)<br>
<b>CH4</b> Power on + [PTT] = Clone Radio, Transmit (undocumented)<br>
<b>CH5</b> Power on + [PTT] = Copy Radio, Receive (this radio has memory overwritten) (undocumented)<br>
<b>CH15</b> Power on + [PTT] + [CH+] = Voice Prompts, enable Chinese, need software to disable voice prompt after enabled<br>
<b>CHx</b> Power on + [CH+] + [CH-] = Programming mode / TURN ON BLUETOOTH (undocumented, start from any channel)<br>
</tr>
<tr><td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=1204s">Odmaster Bluetooth Programming<br>[20:04]</a></td>
  <td>
    <A href="https://web.odmaster.net/login">Odmaster TIDradio Web</A><br>
    <a href="https://apps.apple.com/us/app/odmaster/id1512532413">Odmaster - Apple</a><br>
    <a href="https://play.google.com/store/apps/details?id=com.tid.walkie&hl=en_US">Odmaster - Android</a><br>
  </tr>
<tr><td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=1589s">Manual<br>[26:29]</a></td>
  <td>New manual compared to one filed with FCC
    Technical spec missing
    Page3 LED Display graphic hard squished to bad ratio<br>
    Page5 Icons for Battery charge status are better<br>
    Page6 I have not seen the 'end of transmission tone' email me if you have one<br>
    Page8 Bluetooth section completely rewritten "When the Bluetooth function is turned on, the icon displays and the red light turns on.  The green light is on after connecting through the cell phone APP (Odmaster)  . The green light flashes during communicatoni and the light is off when communication is over"<br>
    
    
    
    
  </td>
</tr>
<tr><td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=1641s">CPS Programming Software<br>[27:21]</a></td>
</tr><td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=2020s">Prolific Chipset driver fix<br>[33:40]</a></td>
<tr><td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=2127s">Chirp Programming Software<br>[35:27]</a></td>
</tr><td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=2344s">FCC 2A4FBM11 Filing<br>[39:04]</a></td>
  <td>Fcc report review:<br>
1. Firmware as 1.0, shipping is 0.9.4<br>
2. Board rev listed as 1.2 in some places, shipping is 1.4<br>
3. Battery listed as T-20C 1500mAh, shipping is BP-11 1000mAh<br>
4. Label mark listed as 2A4FBM11, shipping is 2A-TDM11<br>
5. Internal photos do not show IP67 sealing, shipping unit has ip67 sealing compound (white) for microphone and speaker<br>
6. version 1 of report appears for EU market, Version 2 for FCC?<br>
7. US agent identified<br></td>
<tr><td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=3701s">Radio versions/Accessories<br>[1:01:41] </a></td>
</tr>
</table>


![:VCmakes](https://count.getloli.com/@:VCmakes)
