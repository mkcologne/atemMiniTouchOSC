# atemMiniTouchOSC
Full TouchOSC Setup for Atem Mini Pro

Download it [here](https://github.com/mkcologne/atemMiniTouchOSC/blob/master/AtemMiniPro0.9.touchosc)

Some commands works with Macros.
Instructions at the end of the ReadMe.

![alt text](https://github.com/mkcologne/atemMiniTouchOSC/blob/master/Images/01.png)

![alt text](https://github.com/mkcologne/atemMiniTouchOSC/blob/master/Images/03.png)

![alt text](https://github.com/mkcologne/atemMiniTouchOSC/blob/master/Images/04.png)

![alt text](https://github.com/mkcologne/atemMiniTouchOSC/blob/master/Images/05.png)

![alt text](https://github.com/mkcologne/atemMiniTouchOSC/blob/master/Images/06.png)

![alt text](https://github.com/mkcologne/atemMiniTouchOSC/blob/master/Images/07.png)

# How to add the Macros

• Make sure you don't have Macros between #94 and #99

• Save your Showfile

• Open the XML file with the Editor of your Choice

• Find the Macro-Section
    (start)  <MacroPool>
    (end)  </MacroPool>
    
 • Add this lines between this Tag (If they arent there add <MacroPool> Tag as well:
  
 
        <Macro index="94" name="StartStream" description="">
            <Op id="StreamRTMP" start="True"/>
        </Macro>
        <Macro index="95" name="StopStream" description="">
            <Op id="StreamRTMP" start="False"/>
        </Macro>
        <Macro index="96" name="StartRec" description="">
            <Op id="RecordToMedia" start="True"/>
        </Macro>
        <Macro index="97" name="StopRec" description="">
            <Op id="RecordToMedia" start="False"/>
        </Macro>
        <Macro index="98" name="ChangeDisc" description=""/>
        <Macro index="99" name="Key1Auto" description="">
            <Op id="TransitionSource" mixEffectBlockIndex="0" source="Key1"/>
            <Op id="AutoTransition" mixEffectBlockIndex="0"/>
            <Op id="MacroSleep" frames="35"/>
            <Op id="TransitionSource" mixEffectBlockIndex="0" source="Background"/>
        </Macro>
 
 
• Restore the Showfile and set it up as Start-State which stores the Macros on the Device

• Have Fun!
