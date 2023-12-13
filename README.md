# NIM-ecla
Immplementation of the game of NIM in EclaLang.

## Rules

The game is implemented as depicted in Alain Resnais' 1961 masterpiece "Last year at Marienbad", watch it if you haven't. Watch it again if you already have.

There are five rows, each containing an odd number of sticks from 1 to 7.

The players take turn to pick the sticks. They can take as many as they want, but only from one row at a time.

The player who picks the last stick loses.

## How to play

The game is code in Eclalang, so you'll need a working version of Ecla to run it. 
You can get one on the [Ecla repository](https://github.com/Eclalang/Ecla) on github.
Simply run the nim.ecla with the Ecla build you have in a terminal.

You will first be asked if you want to play against another human, or against a machine. 
If you choose human v. human, the game starts,
if you choose human v. machine, you'll be asked if you want to play against a simple AI (that picks randomly),
or against a perfect one, that will always win if it plays first.

## TODO

- implement human v. human game
- implement random AI game
-  implement perfect AI game

## Ecla bugs I found:

- auto assign in for

the following code:
```ecla
for(i := 1; i < 4; i++){
    ...
}
```
returns an error `Expected variable name instead of :`

while this code:
```ecla
for(var i int = 1; i < 4; i++){
    ...
}
```
is still valid.

- unclear error

the following code:
```ecla
function getMax(l : []int) int{
    ...
}
```
returns an error `Expected '{'`, because I did not put the parenthesis around the return type. 