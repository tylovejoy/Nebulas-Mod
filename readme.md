# Nebula's Force Orb Order Mod for Hax Framework

## **WARNING:** 
This is a modification to the KNEAT template made by Hax. BEFORE PASTING ANY CODE, MAKE SURE YOU ARE NOT OVERWRITING ANY EXISTING VARIABLES or SUBROUTINES. 
Variables and subroutines in the workshop are numbered, check that the NEW variables and subroutines defined in this mod are free in your live map (ie. make sure its number is a free slot in the variable list (non-free variables are greyed out); if not, change its number to a number with a free slot).

## NEW VARIABLES/SUBROUTINES:
```
subroutines
{
	70: TCDtextMOD
}
```


I recommend using Notepad++ as your text editor!


## STEP ONE: 
Create your CP in the Hax framework. The mod assigns the order of the orbs at CP creation, so pay attention to the order that you place the effects! 

The effect in the first slot is set as the First effect to be collected.

The effect that is placed in the second slot is set as the Last effect to be collected.

The effect in the third slot is set as the Second effect to be collected.


## STEP TWO:
Paste the "Checkpoint # Finder" rule into your live map.

This allows you to view what checkpoint you are currently standing on by pressing your interact key. 

Find the checkpoints that require this mod, and record their Checkpoint Number. Be sure to keep a seperate list of CPs involving 2 vs 3 orbs.


## STEP THREE:

Replace "CP#X" in the conditions below with the relevent CP numbers. Be sure to place the CP Number in the Rule corresponding to the correct number of orbs.

The || operator denotes an OR statement, and is used to delimit multiple checkpoints. Remove them if there is only one checkpoint this rule will be used for.
Feel free to add as many || statements and checkpoints as needed.

If you are NOT using one of the two orb rules, disable it in the workshop editor after you've completed step four (eg. If you have no CPs with 3 ordered orbs, then disable the 3 Orb Force Order rule).

The Conditions for TCDdetect Modded line requires the CP Numbers for all CPs involving ordered effects.


### Conditions for 2 Orb Force Order rule - Insert CP Numbers With 2 Orbs Here
```
{
	Event Player.Checkpoint == (CP#1 || CP#2 || CP#3);
}
```
### Conditions for 3 Orb Force Order rule - Insert CP Numbers With 3 Orbs Here
```
{
	Event Player.Checkpoint == (CP#4 || CP#5 || CP#6);
}
```
### Conditions for TCDdetect Modded rule - Insert CP Numbers Of All CPs With Ordered Orbs
```
{
	Event Player.Checkpoint != (CP#1 || CP#2 || CP#3 || CP#4 || CP#5 || CP#6);
}
```
Select the whole line between the curly braces (not including them) and replace the line corresponding rule in the Nebulas Mod.txt file that says:
> "### REMOVE THIS LINE AND REPLACE WITH MODIFIED CONDITION FROM README.TXT ###"

There are THREE INSTANCES of this, replace them all or you will get an error! 

## STEP FOUR:
Disable the following rules (don't delete, save for backup): TCPdetect, and TCD Initiate Sub

Copy and paste the entirety of "Nebulas Mod.txt" into your live map.





## TODO:
Fix line numbers in readme
additional conditions needed to be pasted in TCDtextMOD sub rule

## KNOWN BUGS:
Ability symbols stay appearing after level has finished when ability orbs were used on the last checkpoint.

