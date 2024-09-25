```mermaid
flowchart TD
  A[Game Opens] -->B[Game Generates Number 1-50]
//Prep from program before player input is taken
  B-->C(Take Player Next Input)
//Player makes inputs during this step
  C -->|Player Input  Within Bounds < Generated Number| D[Game Output: Too Low]-->C
  C -->|Player Input Within Bounds > Generated Number| E[Game Output: Too High]-->C
//Game needs to decide if player input is within bounds before it can decide if it's too low or too high. Player is redirected to input
  C -->|Player Input Out Of Bounds| F[Game Output: Remember To Guess 1-50]-->C
  C -->|Player Input Non Numerical| G[Game Output: Remember To Guess Using Numerical Digits]-->C
//Player answer is in incorrect format or entirely out of bounds, player is redirected to input
  C-->|Player Input Correct| H[Game Output: CORRECT]
  H--> I[End Game]
//Player has beaten game, no further guess inputs needed
  I-->J[Output: Restart Button]
  I-->K[Output: Exit Game Button]
//Player is given option to either close or restart game
  J-->|Option Selected|B
  K-->|Option Selected|L[Game Closes]
//Player decision to restart or close game is acted on
```
