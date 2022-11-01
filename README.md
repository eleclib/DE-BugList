# DE-BugList

From Oldest to Newest in #bug-reports channel on AIScripters\
NOTE: The bugs listed have not fully been re-checked for being resolved, some may have been fixed while others may not have been. This list is pending.

Number of Found Bugs since Dec 28, 2021: 63\
Number of Bugs unchecked since then: 48\
Number of Bugs fixed since then: 9\
Number of Bugs partially fixed since then: 3\
Number of Bugs broken since then: 0\
Number of Bugs as "Won't Fix": 1\
Percentage of Bugs fixed: ??%\
Percentage of Bugs broken: ??%\
Percentage of Bugs "Won't Fix": ??%

...\
CHECKED\
...

- [Won't Fix] AI unable to up-find-remote wild-camel/wild-camel-class
- [Fixed] up-get-fact / up-get-focus-fact / up-get-target-fact / up-get-player-fact   don't return true
- [Fixed] counting buildings (dynamically) does not include pending
- [Fixed] up-create-group unable to assign to an empty list
- [Fixed] unable to count other players' organ-gun-line/gbeto-line/gbeto/organ-gun/elite-organ-gun (retuns -1) but elite-gbeto works
- [Fixed] counting other players' barracks huskarl or elite barracks huskarl returns -1, counting huskarl-set returns 2 less than expected
- [Fixed] object-data-move-x/y not working when object not moving
- [Partially Fixed] DUC finding ally buildings [building-class/all-units-class finds all the pieces of TC (109, 618, 619, 620, 1649) instead of just 109]
- [Partially Fixed] up-get-object-type-data: object-data-speed doesnt work and returns -2, object-data-dropsite incorrectly gives 109 (town-center) when it shouldnt be avilable for this command [object-data-dropsite gives 68 (mill) whereas it should be something like -1]
- [Partially Fixed] up-get-object-data: object-data-train-site not working for villagers (including idle villager type), object-data-dropsite bugged for villagers (always gives 109 (town-center)) when it should give mill, lumber camp, or mining camp depending on what it was assigned to [object-data-gather-type still has the same bug as before where it doesn’t change until the villager starts gathering the new resource. It needs to change immediately when the villager is assigned to the new resource.]
- [Fixed] creating scenario with x players, saving, new SP start, exit, add player to map, save, exit, enter SP lobby -> crash
- [Fixed] timers bugged when setting to negative value
- [Fixed] game crash without error box if constant is undefined

...\
IN PROGRESS\
...



...\
PENDING\
...

- unit assistance cant be disabled between sn-safe-town-size and sn-maximum-town-size
- object-data-target-id only return -1 when units in formation with action-patrol or action-attack-move even when they are attacking enemy's object
- cant queue techs one after another, only a tech and a unit (fixed?)
- up-assign-builders for palisade wall and stone-wall doesnt work (fixed?)
- up-object-type-count/-total broken (does not account for pending structures being built and maybe units too?) - up-object-type-count/-total broken for anything that isnt a unit-line or building-line with exception to villagers and gates
- many ResourceAmount constants defined by DE inconsistent with UserPatchConst.per constant definitions
- up-find-resource broken ((up-find-resource c: -1 c: 40) causes a crash) (fixed?)
- tc ungarrison onto deer (up-gather-inside c: town-center c: -1) prevents gather points from being set
- up-create-group when the local list includes garrisoned units does not work correctly, any garrisoned units will be excluded from the goup
- object-data-gather-type is only set when villager starts gathering when it should be set immediately when it is assigned. it does reset "correctly" to -1 when villager is returning from the camp after dropping off their resources
- object-data-action-time behaves differently in DE but its also bugged in UP
- old battering ram id (35) no longer works for DUC since feudal battering ram was added as the base unit (is warning)
- unable to DUC find ally/enemytrade carts
- (sn-ignore-tower-elevation 0) still does not prefer high elevation
- (up-get-point position-enemy gl-target-point-x) does not get nearest target player building (ex. castle)
- place-control works differently in DE compared to UP, sometimes buildiings are placed in back instead of preferred front
- clicking on own ai trade carts causes massive fps tank
- (generate-random-number 0) crashes DE
- tsa bug: units moving toward (-1,-1) with action-attack (apparently DUC leak)
- unit ungarrison from ram paused and when ram gets destroyed by enemy; units set to action-attack but units stand there with no idle animation (object-data-idling is 0)
- id loop search for boars failing in DE (barb boar search code), UP works fine (object id assignment different between verisons?)
- rally points; unable to go from house to house, tower to house: garrison type?
- rules being skipped
- players in treaty no longer considered allies by the AI, causing unexpected behavior
- place-point makes buildings placed far from target point, even with small placement zone size
- map eyecandy (tree on water) causing game crash upon hovering with mouse
- setting promotional picture for a mod to make mod public, game crashes
- villagers going to boar on opposite part of map regardless of LOS (uncapped max hunt distance).
- DUC searching for Ally markets not returning the market (fixed in earlier PUP build?)
- extreme ai doesnt shoot arrows (garrisoned) when upping to next age
- changing color of a player in scenario causes spawn at random location on map
- up-chat-data-to-player inconsistencies with formatting
- up-log-data is broken "invalid negative master object id passed -1"
- AI Game Perspective Switching with chat messages focus stuck on Player 1 and all P1's perspective data
- up-build with a goal set to with-escrow doesnt allow AI to use escrowed resources to place buildings (no foundation) until the building can be placed without escrowed resources
- load-random with '+' load feature doesnt work; script sub-file doesnt get loaded (Meleon)
- taunts 15 and 18 are incorrect sounds; being rushed, enemy sighted wrong (and possibly others)
- setting sn-number-boat-explore-groups to 0 doesnt stop the first trained ship from exploring
- one villager remaining forced to explore
- up-build not as reliable in DE? - negative sn-placement-fail-delta causing incorrect placement and build delay
- dropsite-min-distance deer-hunting returning 255 instead of -1   as well as hunting, boar-hunting and live-boar
- classes dont work for up-set-offensive-priority, despite scripter64 documentation
- trebuchet set counting wrong
- 2 villagers explore and 1 to build houses, when houses finish, it gathers sheep despite gatherers capped at 0 - in UP villagers correctly starts exploring after finishing houses
- position-flank has offset x coords 0-12 higher than what it should be, UP seems to use mirrored flank position
- position-mirror gives position-opposite effect instead of position-mirror
- Resetting Offense Priorities each pass causes a crash
- Chat Box Lag for Win11 users, letters cant be typed until after delay
- action-stop can cause a crash
- there are cases where the path distance calculation is wrong (path distances on arena f.e. not always showing that objects inside the enemy's walled town were inaccessible)
- idle-farm-count yielding negative values on map water nomad (one farm is occupied, returns -1, two farms returns -2)


