# Nebula's Force Orb Order Mod for Hax Framework

## **WARNING:** 
This is a modification to the KNEAT template made by Hax. BEFORE PASTING ANY CODE, MAKE SURE YOU ARE NOT OVERWRITING ANY EXISTING VARIABLES or SUBROUTINES. 
Variables and subroutines in the workshop are numbered, check that the NEW variables and subroutines defined in this mod are free in your live map (ie. make sure its number is a free slot in the variable list (non-free variables are greyed out); if not, change its number to a number with a free slot).


# INSTALLATION


## NEW VARIABLES/SUBROUTINES:
```
variables
{
	global:
		110: CParrayCreated
		111: CParray3orb
		112: CParray2orb

}
subroutines
{
	110: TCDtextMOD
}
```


I recommend using Notepad++ as your text editor!


## STEP ONE: 
Create your CP in the Hax framework. The mod assigns the order of the orbs at CP creation, so pay attention to the order that you place the effects!  
The effect in the first slot is set as the First effect to be collected.  
The effect that is placed in the second slot is set as the Last effect to be collected.  
The effect in the third slot is set as the Second effect to be collected.


## STEP TWO:
Paste the entire "Checkpoint Finder System.txt" into your live map.  
Press the button for the "Hello!" voiceline to initialize the array.
This allows you to mark the checkpoint you are currently standing on by pressing the button for Ultimate Status (2 Orbs) or Reload (3 Orbs).  
A small message will appear on screen that the checkpoint has been set to True.  
If you accidentally mark a checkpoint, press the same button again and a message will appear on screen saying the checkpoint has been set to False.
You are unable to set a single checkpoint to both 3 Orb and 2 Orb.
Find the checkpoints that require this mod, mark them accordingly, and then DISABLE these rules!  
**Now save your map!!!**


## STEP THREE:
Disable the following rules (don't delete, save for backup): TCPdetect, and TCD Initiate Sub  
Copy and paste the entirety of "Nebulas Mod.txt" into your live map.


## KNOWN BUGS:
Ability symbols stay appearing after level has finished when ability orbs were used on the last checkpoint.



