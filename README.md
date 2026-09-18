# Alphazeta
Azerty-like polytonic greek layout

If you want to add this layout, you need to edit rules/evdev.xml and symbols/gr in /usr/share/X11/xkb/.

In evdev.xml, add :
```html
        <variant>
         <configItem>
          <name>alphazeta</name>
          <description>Greek (alphazeta)</description>
         </configItem>
        </variant>
```
after the polytonic layout

In gr add :
```
partial alphanumeric_keys alternate_group
    xkb_symbols "alphazeta" {

    include "gr(polytonic)"

    name[Group1] = "Greek (alphazeta)";

    key.type[Group1] = "FOUR_LEVEL";

    key <AE01>  { [ ampersand,          1,  onesuperior,   exclamdown ] };
    key <AE02>  { [    eacute,          2,   asciitilde,    oneeighth ] };
    key <AE03>  { [  quotedbl,          3,   numbersign,     sterling ] };
    key <AE04>  { [apostrophe,          4,    braceleft,       dollar ] };
    key <AE05>  { [ parenleft,          5,  bracketleft, threeeighths ] };
    key <AE06>  { [     minus,          6,          bar,  fiveeighths ] };
    key <AE07>  { [    egrave,          7,        grave, seveneighths ] };
    key <AE08>  { [underscore,          8,    backslash,    trademark ] };
    key <AE09>  { [  ccedilla,          9,  asciicircum,    plusminus ] };
    key <AE10>  { [    agrave,          0,           at,       degree ] };
    key <AE11>  { [parenright,     degree, bracketright, questiondown ] };
    key <AE12>  { [     equal,       plus,   braceright,  dead_ogonek ] };


    key <AD01> { type[Group1]="THREE_LEVEL",
     [ Greek_alpha, Greek_ALPHA, NoSymbol ] }; // α Α
    key <AD02> { [  Greek_zeta,  Greek_ZETA ] }; // ζ Ζ
    key <AD06> { [ Greek_theta, Greek_THETA ] }; // θ Θ
    key <AD07> { [ Greek_upsilon, Greek_UPSILON ] }; // υ Υ
    key <AC01> { [ Greek_chi, Greek_CHI ] }; // χ Χ
    key <AC02> { [ Greek_sigma, Greek_SIGMA, Greek_finalsmallsigma, Greek_SIGMA ] }; // σ Σ ς
    key <AC07> { [ dead_acute, dead_psili, dead_grave, dead_dasia ] }; // ´  ̓ `  ̔
    key <AC10> { [ Greek_mu, Greek_MU ] }; // μ Μ
    key <AC11> { [ dead_acute, dead_psili, dead_grave, dead_dasia ] }; // ´  ̓ `  ̔
    key <AB01> { [ Greek_omega, Greek_OMEGA ] }; // ω Ω
    key <AB02> { [ Greek_xi, Greek_XI ] }; // ξ Ξ
    key <AB04> { [ dead_iota, dead_tilde, apostrophe, quotedbl ] }; // ͺ ~ '
    key <AB07> { [ comma, question ] }; // , ?
    key <AB08> { [ semicolon, colon ] }; // ; :
    key <AB09> { [ period, periodcentered ] }; // . ·
    };
```
after the polytonic function
