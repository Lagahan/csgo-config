# Autoexec files

- You can create an `autoexec.cfg` file in `(steam directory)\steamapps\common\Counter-Strike Global Offensive\csgo\cfg\` which will run each time the game boots up.  
- This is handy for maintaining common settings across accounts, PCs.  
- Unfortunately it doesn't store your Video settings.  
- Below is a copy of mine with comments on what each variable does.  
- Anything starting with `//` will be ignored by CSGO as a comment.  
- Backup your current config file at `C:\Program Files\Steam\userdata\xxxxx\730\local\cfg\config.cfg` where `xxxxx` is your Steam accounts user ID before using this.  
- I have my launch options commented in at the top of the file.  

```
//------------------------------------------------------LAUNCH OPTIONS------------------------------------------------------//
// -freq 240 -refresh 240 -high -novid -nojoy -console -d3d9ex
//--------------------------------------------------------------------------------------------------------------------------//

echo " "
echo " "
echo "Configuring Config..."
//------------------------------------------------------BINDS---------------------------------------------------------------//
echo " "
echo "Configuring Binds..."
unbindall
//--------MOVEMENT----------------------------//
bind "w" "+forward"                           // Move Forward
bind "s" "+back"                              // Move Backward
bind "a" "+moveleft"                          // Strafe Left
bind "d" "+moveright"                         // Strafe Right
bind "SHIFT" "+speed"                         // Walk
bind "SPACE" "+jump"                          // Jump
bind "MWHEELUP" "+jump"                       // Jump
bind "CTRL" "+duck"                           // Crouch

//--------FIRING------------------------------//
bind "MOUSE1" "+attack;r_cleardecals"         // Fire
bind "MOUSE2" "+attack2"                      // Secondary Fire
bind "r" "+reload"                            // Reload

//--------WEAPONS-----------------------------//
bind "1" "slot1"                              // Primary Weapon
bind "2" "slot2"                              // Secondary Weapon
bind "3" "slot3"                              // Knife
bind "4" "slot5"                              // Bomb
bind "5" "slot6"                              // HE Grenade
bind "MWHEELDOWN" "slot7"                     // Flashbang
bind "MOUSE4" "slot8"                         // Smoke Grenade
bind "6" "slot9"                              // Decoy Grenade
bind "MOUSE5" "slot10"                        // Molotov Cocktail
bind "n" "+lookatweapon"                      // Vanity Mode

//--------ITEMS-------------------------------//
bind "[" "slot12"                             // Healthshot (Blackout)
bind "]" "slot13"                             // Utility Items

//--------INVENTORY---------------------------//
bind "q" "lastinv"                            // Last Weapon Used
bind "x" "drop"                               // Drop Weapon
bind "e" "+use"                               // Use
bind "b" "buymenu"                            // Buy Menu
bind "u" "+spray_menu"                        // Spray

//--------COMMS-------------------------------//
bind "y" "messagemode2"                       // Team Message
bind "t" "messagemode"                        // Chat Message
bind "ALT" "+voicerecord"                     // Use Mic
bind "KP_ENTER" "ignorerad"                   // Disable ingame radio callouts (hit every round)
bind "PGDN" "voicetoggle"                     // Mute Voice
bind "," "radio1"                             // Command Radio Message
bind "." "radio2"                             // Standard Radio Message
bind "/" "radio3"                             // Report Radio Message
alias voicetoggle "incrementvar voice_scale 0 0.15 0.15"

//--------BUY EQUIPMENT-----------------------//
bind "F1" "buy vest; buy vesthelm;"           // Armor + Helmet (If affordable)
bind "F2" "buy defuser;"                      // Defuser
bind "F3" "buy p250;"                         // P250
bind "F4" "buy tec9; buy fiveseven;"          // Tec 9 / Five Seven
bind "F5" "buy deagle; buy revolver;"         // Deagle / Revolver

bind "F6" "buy galilar; buy famas;"           // Galil / Famas
bind "F7" "buy ak47; buy m4a1;"               // AK47 / M4A1-S / M4A4
bind "F8" "buy awp;"                          // AWP

//bind "F9" "buy ump45;"                      // UMP
bind "F9" "buy hegrenade;"                    // HE Grenade
bind "F10" " buy smokegrenade;"               // Smoke
bind "F11" "buy flashbang;"                   // Flash
bind "F12" " buy incgrenade; buy molotov;"    // Fire

//--------COMMANDS----------------------------//
bind "TAB" "+showscores"                      // Scoreboard
//bind "1" "clear"                            // Clear console
alias dc "disconnect"
alias hp "mm_dedicated_search_maxping 150"
alias lp "mm_dedicated_search_maxping 68"

//--------BOTMATCH----------------------------//
alias resetbots "bot_kick; bot_add; bot_add; bot_add; bot_add; bot_add; bot_add; bot_add; bot_add; bot_add; bot_add; bot_add; bot_add;"
//--------------------------------------------------------------------------------------------------------------------------//

//------------------------------------------------------CROSSHAIR-----------------------------------------------------------//
echo " "
echo "Configuring Crosshair..."
//--------SHAPE-------------------------------//
cl_crosshairdot "0"
cl_crosshairgap "-2"
cl_crosshairgap_useweaponvalue "0"
cl_crosshairscale "0"
cl_crosshairsize "2"
cl_crosshairstyle "4"
cl_crosshairthickness "0.5"
cl_fixedcrosshairgap "-7"

//--------1 Removes top line------------------//
cl_crosshair_t "0"

//--------OUTLINE-----------------------------//
cl_crosshair_drawoutline "1"
cl_crosshair_outlinethickness "1"

//--------COLOUR------------------------------//
cl_crosshairusealpha "1"
cl_crosshairalpha "255"
cl_crosshaircolor "5"
cl_crosshaircolor_b "0"
cl_crosshaircolor_g "255"
cl_crosshaircolor_r "0"

//--------DYNAMIC MOVEMENT--------------------//
cl_crosshair_dynamic_maxdist_splitratio "0.500000"
cl_crosshair_dynamic_splitalpha_innermod "1.000000"
cl_crosshair_dynamic_splitalpha_outermod "0.200000"
cl_crosshair_dynamic_splitdist "1"

//--------SNIPER SCOPE------------------------//
cl_crosshair_sniper_show_normal_inaccuracy "0"
cl_crosshair_sniper_width "2"
//--------------------------------------------------------------------------------------------------------------------------//

//------------------------------------------------------HUD-----------------------------------------------------------------//
echo " "
echo "Configuring HUD..."
hud_scaling "0.8"
hud_showtargetid "0"

// Safezones for HUD 
// Lower than 1 will bring the HUD elements closer to the center of the screen.
safezonex "1"
safezoney "1"

cl_hud_healthammo_style "1"
cl_hud_playercount_pos "1"
cl_hud_playercount_showcount "1"
cl_hud_color "8"
cl_hud_background_alpha "1"
cl_hud_bomb_under_radar "0"
cl_teammates_colors_show "2"
cl_teamid_overhead_always "2"

cl_showloadout "1"
cl_showfps "0"
cl_showpos "0"
cl_show_clan_in_death_notice "0"
spec_show_xray "0"
cl_spec_stats "0"

// Disable help.
cl_autohelp "0"
cl_showhelp "0"
gameinstructor_enable "0"

//--------RADAR-------------------------------//
cl_hud_radar_scale "1.2"
cl_radar_rotate "1"
cl_radar_always_centered "1"
cl_radar_scale "0.28"
cl_radar_icon_scale_min "0.4"
cl_radar_square_with_scoreboard "0"

//--------NET_GRAPH---------------------------//
net_graph "1"
net_graphproportionalfont "0"
net_graphheight "0"
net_graphpos "2"
net_graphholdsvframerate "0"
net_graphmsecs "100"
net_graphshowinterp "0"
net_graphshowlatency "0"
net_graphshowsvframerate "0"
net_graphsolid "1"
net_graphtext "1"
//--------------------------------------------------------------------------------------------------------------------------//

//------------------------------------------------------MOUSE---------------------------------------------------------------//
echo " "
echo "Configuring Mouse..."
sensitivity "1.28"
zoom_sensitivity_ratio_mouse "1"
m_pitch "0.022"
m_yaw "0.022"

m_forward "0"
// Raw mouse input
m_rawinput "1"
m_mousespeed "0"
m_mouseaccel1 "0"
m_mouseaccel2 "0"
m_customaccel "0"
m_customaccel_exponent "0"
m_customaccel_max "0"
m_customaccel_scale "0"
//--------------------------------------------------------------------------------------------------------------------------//

//------------------------------------------------------VIEWMODEL-----------------------------------------------------------//
echo " "
echo "Configuring Viewmodel..."
viewmodel_presetpos "0"
viewmodel_offset_x "-2"
viewmodel_offset_y "2"
viewmodel_offset_z "-2"
viewmodel_fov "68"

cl_righthand "1"
cl_bobcycle "0.98"
cl_bob_lower_amt "5"
cl_bobamt_lat "0.1"
cl_bobamt_vert "0.1"
cl_viewmodel_shift_left_amt "0.5"
cl_viewmodel_shift_right_amt "0.25"
//--------------------------------------------------------------------------------------------------------------------------//

//------------------------------------------------------RENDERER------------------------------------------------------------//
echo " "
echo "Configuring Renderer..."

// These are mostly performance settings
cl_forcepreload "1"
r_eyegloss "0"
r_eyemove "0"
r_eyesize "0"
r_drawtracers_firstperson "1"
r_dynamic "0"
engine_no_focus_sleep "1"
muzzleflash_light "0"

// Multi-threading
mat_queue_mode 2

fps_max "0"
fps_max_menu "0"
//--------------------------------------------------------------------------------------------------------------------------//

//------------------------------------------------------NETWORK-------------------------------------------------------------//
echo " "
echo "Configuring Connection..."
rate "307200"
cl_interp "0"
cl_interp_ratio "1"

mm_dedicated_search_maxping "70"
//--------------------------------------------------------------------------------------------------------------------------//

//------------------------------------------------------AUDIO---------------------------------------------------------------//
echo " "
echo "Configuring Audio..."
cl_downloadfilter "nosounds"

lobby_voice_chat_enabled "0"
snd_legacy_surround "0"
// Dont mute game when alt tabbed
snd_mute_losefocus "0"
snd_pitchquality "1"
snd_prefetch_common "1"

// Below are settings to tweak the positional sound system
snd_headphone_pan_exponent "1"
snd_headphone_pan_radial_weight "1"
snd_front_headphone_position "45"
snd_rear_headphone_position "135"

snd_stereo_speaker_pan_exponent "1"
snd_stereo_speaker_pan_radial_weight "1"
snd_front_stereo_speaker_position "45"
snd_rear_stereo_speaker_position "135"

snd_surround_speaker_pan_exponent "1"
snd_surround_speaker_pan_radial_weight "0"
snd_front_surround_speaker_position "45"
snd_rear_surround_speaker_position "138"

// Disable all music except 10 second bomb warning
snd_musicvolume "0.1"
snd_deathcamera_volume "0"
snd_mapobjective_volume "0" // The bomb music played prior to the ten-second warning
snd_menumusic_volume "0"
snd_roundend_volume "0"
snd_roundstart_volume "0"
snd_tensecondwarning_volume "0.1" // The ten-second warning
snd_mute_losefocus "0" // This will allow game noise to play even though youve alt-tabbed out

volume "0.4"
voice_enable "1"
voice_forcemicrecord "0"
voice_inputfromfile "0"
voice_scale "0.2"
voice_mixer_boost "1"
voice_mixer_volume "1"
voice_caster_enable "1"
voice_caster_scale "0.5"
//--------------------------------------------------------------------------------------------------------------------------//

//------------------------------------------------------GAME SETTINGS-------------------------------------------------------//
echo " "
echo "Configuring Game Settings..."

// These are ingame preferences
cl_freezecampanel_position_dynamic "0"
cl_freezecameffects_showholiday "0"
cl_disablehtmlmotd "1"
cl_disablefreezecam "1"

closeonbuy "0"
budget_show_history "0"
budget_show_averages "0"
budget_show_peaks "0"
player_nevershow_communityservermessage "1"

// Crouch - 0 Hold 1 Toggle
option_duck_method "0"
option_speed_method "0"

// Dont auto switch weapons
cl_autowepswitch "0"
cl_use_opens_buy_menu "0"

cl_dm_buyrandomweapons "0"
cl_teammate_colors_show "1"

//--------------------------------------------------------------------------------------------------------------------------//

echo " "
host_writeconfig
echo " "
dsp_reload
snd_restart
echo "Done."
echo " "
```

----