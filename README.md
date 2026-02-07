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
<td>
	<img src="https://github.com/voltcraftmakes/td-m11/blob/main/docs/TD-M11%20Label.jpg" width="88"> <img src="https://github.com/voltcraftmakes/td-m11/blob/main/docs/PCB-M11-back.JPG" width="150"> <img src="https://github.com/voltcraftmakes/td-m11/blob/main/docs/PCB-M11-front.JPG" width="150"> <img src="https://github.com/voltcraftmakes/td-m11/blob/main/docs/PCB-M11-side.JPG" width="150"><br>
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
  <td>New manual compared to one filed with FCC<br>
    Page3 LED Display graphic hard squished to bad ratio<br>
    Page5 Icons for Battery charge status are better<br>
    Page6 I have not seen the 'end of transmission tone' email me if you have one<br>
    Page8 Bluetooth section completely rewritten "When the Bluetooth function is turned on, the icon displays and the red light turns on.  The green light is on after connecting through the cell phone APP (Odmaster)  . The green light flashes during communication and the light is off when communication is over"<br>
    Page9 <br>
    1. Transmit Power notes removed "PMR446 only supports 0.5W Max, FRS 8-14Ch only supports 0.5W Max and Carrier Output Power <=0.5W PMR446 and <=1.0W/0.5W FRS" and manual now shows Carrier Output Power <=2W<br>
    2. Frequency range now listed as UHF:400-480MHZ (was shows as PMR446 and FRS before)<br>
    3. Operating temperature now 60C, was 40C<br>
    4. Adds Wide 25KHZ channel spacing<br>
    5. Modulation Limiting adds W: <=5kHZ<br>
    6. Occupying Bandwidth is now 16kHz, was 11kHz<br>
    Page 10 <B>REMOVED FCC DECLARATIONS</B>: Class B Part 15, (RED) 2014/53/EU, 0-40C <b>limited to 2000m max elevation</b> EN 50566:2017, EN IEC/IEEE 62209-1528:2021, EU 10g SAR results, battery disposal warning, do not mod for FCC cell reception.
    </td>
</tr>
<tr><td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=1641s">CPS Programming Software<br>[27:21]</a></td>
</tr><td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=2020s">Prolific Chipset driver fix<br>[33:40]</a></td>
<tr><td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=2127s">Chirp Programming Software<br>[35:27]</a></td>
</tr><td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=2344s">FCC Device 2A4FBM11 Filing<br>[39:04]</a></td>
  <td> Fcc: https://apps.fcc.gov/oetcf/eas/reports/GenericSearch.cfm  <br>
    Search: FRN: <A href="https://apps.fcc.gov/cores/searchDetail.do?frn=0031948888&csfrToken=">0031948888</A>a> Grantee Code: 2A4FB  or Applicant Name: Guangzhou TID  Show: 100, [SEARCH]<br>
	has 37 results as of 2026-02-06<br>
    https://fccid.io/2A4FBM11 shows 2 versions of report <br>
    <br>
 	<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/Covered-List-and-Covered-Equipment-Letter-7139573-1.pdf">1. Covered List and Covered Equipment Letter TID 2024-02-03</a><br>
	<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/USA-agent-lette-7139576-1.pdf">2. USA agent TID 2024-02-03</a><br>
	<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/Difference-Description-7139572-1.pdf">3. Difference Description TID 2024-02-18</a><br>
	<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/Agent-Authorization-Letter-Templats-7139574-1.pdf">4. Agent Authorization Letter Templats TID 2024-02-19</a><br>
	<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/FCC-Short-Long-Term-Confidentiality-Request-7139575-1.pdf">5. FCC Short & Long Term Confidentiality Request 2024-02-03</a><br>
	<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/External-Photos-7139567-1.pdf">6. External Photos AGC </a><br>
	<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/label-and-location-7139566-1.pdf">7. Label and location</a><br>
	<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/Internal-Photos-7139568-1.pdf">8. Internal Photos AGC</a><br>
	<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/RF%20Exposure%20Info1-3.pdf">9. RF Exposure Info1 Swiss 2023-10-16 </a><br>
	<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/RF%20Exposure%20Info2-3.pdf">10. RF Exposure Info2 2023-05-26</a><br>
	<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/RF-Exposure-Info-7139589-2.pdf">11. SAR Test Report V1.0 AGC 2024-02-02</a><br>
	Test1: IEEE Std. 1528:2013<br>
	Test2: FCC 47 CFR Part 2(2.1093)<br>
	Test3: IEEE Std C95.1 2005<br>
	KDB 447498 D01 General RF Exposure Guidance V06<br>
	KDB 865664 D01 SAR Measurement 100MHz to 6Ghz v01R04<br>
	KDB 643646 D01 SAR Test for PTT Radios V01R03<br>
	<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/test-Report-7139570-1.pdf">12. FCC Test Report AGCTR-ER-FCC-SDOC V1.0 AGC 2024-02-01</a><br>
	Test1: FCC 47 CFR Part 15<br>
	Test2: ANSI C63.4-2014<br>
  <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/test-Report-7139590-2.pdf">13. FCC Test Report2 AGCER-FCC-FRS-V1 AGC 2024-02-01 </a><br>
	Test1:FCC 47 CFR Part 95<br>
	Test2:FCC 47 CFR Part 2<br>
	Test3:ANSI C63.26-2015<br>
	Test4:ANSI/TIA-603-E-2016<br>
	Test5:KDB 888861 D01 (Part 95 GMRS FRS V01)<br>
	<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/Test-Photos-7139577-1.pdf">14. Test Setup Photos1</a><br>
  <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/Test-Setup-Photos-7139591-2.pdf">15. Test Setup Photos2  </a><br>  
	<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/User-manual-7139569-1.pdf">16. User manual</a><br>
<br>    
FCC report review:<br>
1. Firmware (software) listed as V1.0, shipping is 0.9.4 <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/RF-Exposure-Info-7139589-2.pdf">(11)</a> and <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/test-Report-7139570-1.pdf">(12)</a> and <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/test-Report-7139590-2.pdf">(13)</a><br>
2. Board rev listed shown 1.2 in some places, shipping is 1.4 <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/Internal-Photos-7139568-1.pdf">(8)</a> and <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/RF-Exposure-Info-7139589-2.pdf">(11)</a><br>
3. Battery listed as T-20C 1500mAh, shipping is BP-11 1000mAh <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/RF-Exposure-Info-7139589-2.pdf">(11)</a> and <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/test-Report-7139570-1.pdf">(12)</a> and <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/test-Report-7139590-2.pdf">(13)</a><br>
4. Label mark listed as FCC ID: 2A4FBM11 in <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/label-and-location-7139566-1.pdf">(7)</a>, currently shipping is <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/TD-M11%20Label.jpg">FCC ID: 2A-TDM11</a> <br>
5. Internal photos do not show IP67 sealing, shipping unit has ip67 sealing compound (white) for microphone and speaker <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/Internal-Photos-7139568-1.pdf">(8)</a><br>
6. US agent <a href="https://www.fccusagent.com/about/">Tim Payne </a> @ FCCUSAgent.com identified <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/USA-agent-lette-7139576-1.pdf">(2)</a> <br>
7. test equipment <b>Eeatsheep</b> 6dB attenuator listed but not used - is that a real Manufacturer? <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/test-Report-7139590-2.pdf">(13)</a><br>
8. Allows versions TD-M12, TD-M13. no record of TD-M12 ever shipping. TD-M13 is now offered as a POC radio, a completely different radio but supposedly named in this certificate. <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/Difference-Description-7139572-1.pdf">(3)</a>and <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/RF-Exposure-Info-7139589-2.pdf">(11)</a> and <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/test-Report-7139590-2.pdf">(13)</a><br>
9. Emission bandwidth listed as 10.52Khz, standard allows 12.5kHz, manual lists bandwidth is 16khz <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/test-Report-7139590-2.pdf">(13)</a>
10. Test report shows unit never went over 1W ERP, marketing fluff now shows in manual <=2W, but unit is still likely a 1W max unit <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/test-Report-7139590-2.pdf">(13)</a><br>
11. User manual at FCC shows operating range 0-40C, test report says "normal conditions" 15-35C, extreme -20-50C, frequency error tested from -30-50C and new manual now shows operating temperature -20-60C <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/test-Report-7139570-1.pdf">(12)</a> and <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/User-manual-7139569-1.pdf">(16)</a><br><br>
<a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/EXIFMetaData.txt">EXIF Meta Data Analysis</a> of FCC files shows a few intersting things<br>
	1. Sid Sanders listed as author in meta data <a href="https://github.com/voltcraftmakes/td-m11/blob/main/docs/FCC/Covered-List-and-Covered-Equipment-Letter-7139573-1.pdf">(1)</a> most likely <a href="https://www.linkedin.com/in/sid-sanders-5b273814/">retired engineer in 2018</a> who had started Timco Engineering, FCC Authorized Telecommmunications Certification Body (TCB) who is now <a href="https://www.gainesville.com/obituaries/pgai0626343">deceased.</a>
</td>
<tr><td><a href="https://www.youtube.com/watch?v=o2LUXxH6YpM&t=3701s">Radio versions/Accessories<br>[1:01:41] </a></td>
</tr>
</table>


![:VCmakes](https://count.getloli.com/@:VCmakes)
