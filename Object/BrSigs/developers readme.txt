BR Sigs for openBVE .

Note these signals were custom built for the 2010-2011 NWW routes http://bve4.net but should have enough combinations to import into your own routes. Using photoreal textures, they come complete with lens hoods, rear views and signal glows. 

.csv objects may be used as static signals (freeobjs) for use on other tracks
.animated objects are intended for use in the .SigF statement for active signals.

Note that the static versions cannot be imported into a route as direct replacements for BVE4 BRSigs, as their alignment is different. You would need to alter the position of the freeobject.

Example routefile signal index:


Signal(1).Load NWM_open\brsigs_open\2aspect_GR.animated
Signal(2).Load NWM_open\brsigs_open\2aspect_YR.animated
Signal(3).Load NWM_open\brsigs_open\3Aspect.animated
Signal(4).Load NWM_open\brsigs_open\4aspect.animated
Signal(5).Load NWM_Open\brsigs_open\repeater.animated
Signal(6).Load NWM_open\brsigs_open\4aspect_featherL.animated
Signal(7).Load NWM_open\brsigs_open\4aspect_featherR.animated
Signal(8).Load NWM_open\brsigs_open\3aspect_featherR.animated
signal(9).Load NWM_open\brsigs_open\4aspect_callon.animated
signal(10).Load NWM_open\brsigs_open\3aspect_featherl.animated
Signal(11).Load NWM_open\brsigs_open\2aspect_callon2.animated	
Signal(12).Load NWM_open\brsigs_open\4aspect_feather2L.animated
Signal(13).Load NWM_open\brsigs_open\4aspect_feather2r.animated
Signal(15).Load NWM_open\brsigs_open\2aspect_feather_callon2.animated
Signal(16).Load NWM_open\brsigs_open\2aspect_featherrlit_callonunlit.animated
Signal(17).Load NWM_open\brsigs_open\2aspect_featherrlit_callon2.animated
Signal(18).Load NWM_open\brsigs_open\3aspect_callon.animated
Signal(19).Load NWM_open\brsigs_open\2aspect_GY_distant.animated
Signal(20).Load NWM_open\brsigs_open\3aspect_indM.animated
Signal(21).Load NWM_open\brsigs_open\3aspect_ind1.animated
Signal(22).Load NWM_open\brsigs_open\3aspect_ind2.animated
Signal(23).Load NWM_open\brsigs_open\3aspect_ind3.animated
Signal(24).Load NWM_open\brsigs_open\3aspect_ind4.animated
Signal(27).Load NWM_open\brsigs_open\2Aspect_YR_ind2_colit.animated
Signal(28).Load NWM_open\brsigs_open\3aspect_indB.animated
Signal(29).Load NWM_open\brsigs_open\3Aspect_ind2_colit.animated
Signal(30).Load NWM_open\brsigs_open\2aspect_YR_ind1_co.animated
Signal(31).Load NWM_open\brsigs_open\2aspect_YR_ind2_co.animated
Signal(32).Load NWM_open\brsigs_open\2aspect_YR_ind3_co.animated
Signal(33).Load NWM_open\brsigs_open\2aspect_YR_ind4_co.animated
Signal(34).Load NWM_open\brsigs_open\4aspect_ind1.animated
Signal(35).Load NWM_open\brsigs_open\4aspect_ind2.animated
Signal(36).Load NWM_open\brsigs_open\4aspect_ind3.animated
Signal(37).Load NWM_Open\brsigs_open\platformbanner.animated
Signal(38).Load NWM_Open\brsigs_open\callon_Sdg.animated
Signal(39).Load NWM_open\brsigs_open\4aspect_ind4.animated
Signal(40).Load NWM_open\brsigs_open\4aspect_indG.animated
Signal(41).Load NWM_open\brsigs_open\4aspect_indM.animated
Signal(42).Load NWM_Open\brsigs_open\callon.animated
Signal(43).Load NWM_open\brsigs_open\3aspect_indG.animated
Signal(44).Load NWM_open\brsigs_open\3aspect_ind0.animated
signal(50).Load NWM_open\brsigs_open\4Aspect.animated
signal(51).Load NWM_open\brsigs_open\4Aspect_Ya.animated
signal(52).Load NWM_open\brsigs_open\4Aspect_2Ya.animated
signal(53).Load NWM_open\brsigs_open\4Aspect_F_Y.animated
signal(54).Load NWM_open\brsigs_open\4Aspect_F_2Y.animated
signal(55).Load NWM_open\brsigs_open\4FeatherL.animated
signal(56).Load NWM_open\brsigs_open\4Aspect_Y_approachcontrol.animated
signal(57).Load NWM_open\brsigs_open\4Aspect_Rb.animated
signal(58).Load NWM_open\brsigs_open\4Aspect_Ng.animated
signal(59).Load NWM_open\brsigs_open\3aspect_alt_main.animated
signal(60).Load NWM_open\brsigs_open\3aspect_alt_callon.animated

Examples

to place a four aspect animated signal, using the above signal index number of 4

1025,
.Sigf 4;1;-2.5;4.3, <-- where signalindexnumber;1;xpos;ypos
.Section 0;2;3;4,

The four aspect flashing signals used upon approach to high speed junctions require some cheating, and 3 signals overlayed thus:

First flasher 
(flashing double yellow if signal at 4025m is clear, but otherwise; steady double yellow aspect at best dependant on whether the sections until 5025m are clear).

2025,
.sigf 54;1;-2.15;6.35,
.sigf 52;2;-2.15;6.35,
.sigf 57;1;-2.15;6.35,
.Section 0;2;3;4,

second flasher 
(flashing yellow if signal at 4025m is clear, but otherwise; steady yellow aspect at best).

3025,
.sigf 53;1;-2.2;4.7,
.sigf 51;2;-2.2;4.7, 
.sigf 57;1;-2.2;4.7, 
.Section 0;2;3;4,

junction left signal
(held at yellow if route is clear, until approach; then clears to less restrictive aspect if route is clear for the next 3 signalling sections or more)

4025,
.sigf 58;1;-2.3;4.7,   
.sigf 56;1;-2.3;4.7,
.sigf 55;1;-2.3;4.7,
.Section 0;2;3;4, 

These objects and textures are in the public domain and are free to reuse / redistribute / modify without permission.

With thanks to Anthony Bowden of railsimroutes.net for the animation code and brains behind the flashing signal aspects.

Michelle of the openBVE project for the glow graphics contained within the graphics sub folder.

By TSC Team
2010. v1.00

http://www.trainsimcentral.co.uk
http://bve4.net


