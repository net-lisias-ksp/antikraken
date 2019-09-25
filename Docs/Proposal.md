# McLisias Anti Kraken :: Software Proposal Document

This project aims to detect the most commons mistakes and glitches found on KSP installments.

KSP 1.x series are the initial goal, but once KSP 2 is on the wild a new iteration for supporting it will be started as its internals are known and common issues to KSP 1 are detected.

## Checks

1. GameData/GameData
	+ A very usual mistake
	+ Should be a game blocker until fixed
2. Add'Ons installed on the wrong place
	+ The second most common mistake
	+ Had to detect, however, as some metadata is needed
3. Add"Ons duplicated
	+ The third most common mistake, always happening together 2.
	+ Way easier to detect
	+ False positives need to me traced, mainly due DLLs like MiniAVC.dll
	+ Should be a game blocker until fixed

## Automatic fixes

Automatic fixes are hairy, but can be done under certain circumstances.

1. GameData/GameData
	+ As long there are no collisions, its contents can be moved to GameData and then GameData/GameData be deleted
2. Add'Ons on wrong place
	+ Once there's metadata available and there're no collisions, the Add'On can be moved to the correct place 
3. Add"Ons duplicated
	+ The oldest copies can be deleted, and the item 2 can be applied if needed.
 
