
# 포켓몬 데이터 검증


- 개수
	- 1446개
- 아이디 형식
	- 언더바, 소문자, 숫자만 허용
- 중복
	- 아이디로 검증

# 이름 검증

폼이 있는 포켓몬에서 언더바가 아닌 대시가 발견된다. 약 10개정도

# 종족값 검증


기본스탯의 합이 종족값이라고 생각했으나..
아래 두 데이터만 왜인지 정확히 10이 차이난다.

charizard_gigantamax 634 644
kingler_gigantamax 575 585


# 포켓몬 폼

폼이름과 폼키가 혼용되고 있다.

예시)
영어 이름: gigantamax, monsoon (폼키를 통해서 국제화를 하여 영어이름으로 바꾼 것)
폼 키: g_max, monsoon_pattern

- 폼 변환 배열에도 이전과 이후가 폼 영어이름으로 되어있다.
- 아이디에 폼 변환이 있을 시 폼의 영어 이름이 들어간다.
- formName에는 폼키가 들어가 있다.

-> 이넘의 영어이름을 하자고 하였으니 폼키를 기준으로 하는게 어떨까?


koName에서 한국어 폼키가 아닌 영어 폼키가 나오고 있다.


아래 데이터는 폼변환이 가능하다고 나오나 변환 정보가 빈배열로 주어지고 있다.

pikachu_cosplay
pikachu_cool_cosplay
pikachu_beauty_cosplay
pikachu_cute_cosplay
pikachu_smart_cosplay
pikachu_tough_cosplay
pichu
pichu_spiky
unown_a
unown_c
unown_b
unown_d
unown_e
unown_f
unown_h
unown_g
unown_i
unown_k
unown_j
unown_l
unown_m
unown_n
unown_o
unown_p
unown_q
unown_r
unown_s
unown_t
unown_u
unown_x
unown_y
unown_z
unown_exclamation
unown_v
unown_question
unown_w
burmy_plant
burmy_trash
burmy_sandy
wormadam_plant
wormadam_sandy
wormadam_trash
shellos_east
shellos_west
gastrodon_west
gastrodon_east
rotom
rotom_heat
rotom_wash
rotom_frost
rotom_fan
rotom_mow
basculin_red_striped
basculin_blue_striped
basculin_white_striped
deerling_winter
sawsbuck_summer
sawsbuck_spring
deerling_autumn
deerling_spring
sawsbuck_winter
sawsbuck_autumn
deerling_summer
froakie
froakie_battle_bond
frogadier_battle_bond
frogadier
greninja
scatterbug_meadow
scatterbug_icy_snow
scatterbug_polar
scatterbug_tundra
scatterbug_continental
scatterbug_garden
scatterbug_elegant
scatterbug_marine
scatterbug_modern
scatterbug_archipelago
scatterbug_high_plains
scatterbug_sandstorm
scatterbug_river
scatterbug_monsoon
scatterbug_sun
scatterbug_savanna
scatterbug_jungle
scatterbug_ocean
scatterbug_poke_ball
scatterbug_fancy
spewpa_meadow
spewpa_polar
spewpa_icy_snow
spewpa_tundra
spewpa_continental
spewpa_garden
spewpa_elegant
spewpa_modern
spewpa_marine
spewpa_archipelago
spewpa_high_plains
spewpa_sandstorm
spewpa_river
spewpa_monsoon
spewpa_savanna
spewpa_sun
spewpa_ocean
spewpa_jungle
spewpa_fancy
spewpa_poke_ball
vivillon_icy_snow
vivillon_meadow
vivillon_tundra
vivillon_polar
vivillon_continental
vivillon_garden
vivillon_elegant
vivillon_modern
vivillon_marine
vivillon_high_plains
vivillon_archipelago
vivillon_sandstorm
vivillon_river
vivillon_monsoon
vivillon_savanna
vivillon_jungle
vivillon_sun
vivillon_poke_ball
vivillon_fancy
flabebe_red
flabebe_yellow
flabebe_orange
flabebe_blue
flabebe_white
floette_red
florges_red
floette_yellow
florges_yellow
floette_orange
vivillon_ocean
floette_blue
floette_white
florges_orange
florges_blue
florges_white
furfrou
furfrou_heart
furfrou_star
furfrou_dandy
furfrou_debutante
furfrou_diamond
furfrou_matron
furfrou_pharaoh
meowstic_male
meowstic_female
furfrou_kabuki
furfrou_la_reine
pumpkaboo
pumpkaboo_small
pumpkaboo_large
pumpkaboo_super
gourgeist
gourgeist_small
gourgeist_super
gourgeist_large
zygarde_10
zygarde_50
oricorio_pompom
oricorio_baile
rockruff_own_tempo
rockruff
lycanroc_midday
oricorio_sensu
lycanroc_midnight
oricorio_pau
lycanroc_dusk
magearna_original
marshadow
marshadow_zenith
magearna
sinistea_phony
sinistea_antique
polteageist_phony
polteageist_antique
indeedee_male
indeedee_female
zarude
zarude_dada
basculegion_male
basculegion_female
oinkologne_male
oinkologne_female
maushold_four
maushold_three
squawkabilly_green_plumage
squawkabilly_blue_plumage
squawkabilly_yellow_plumage
squawkabilly_white_plumage
tatsugiri_droopy
tatsugiri_curly
tatsugiri_stretchy
dudunsparce_two_segment
dudunsparce_three_segment
gimmighoul_roaming
gimmighoul_chest
koraidon_apex_build
miraidon_ultimate_mode
poltchageist_counterfeit
sinistcha_unremarkable
paldea_tauros_combat
paldea_tauros_aqua
paldea_tauros_blaze


