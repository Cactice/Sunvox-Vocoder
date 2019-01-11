# sunvox-autotune
Autotune developed for Sunvox using logic Gates and Pitch Shifters

# Structure

## Comparison
Compares two sounds and outputs 2 bit data of which is louder.

| Right | Left  | Explanation             |
|-------|-------|-------------------------|
| True  | True  | This should not happen  |
| True  | False | Right is Bigger         |
| False | True  | Left is Bigger          |
| False | False | They are the same value |

### If
There is an A/D converter which can detect if only one of R or L channel is above a certain threshold.(R XOR L)
Issue with the current model: if they are both the same value than this part will be stuck in a loop of changing the threshold in which both R & L would be 0.
#### Update-threshold (4bit)
If R XNOR L than it updates the threshold so the two would be in a XOR situation.
##### Latch
##### Half Adder
##### A/D convert

## Shifter

###
