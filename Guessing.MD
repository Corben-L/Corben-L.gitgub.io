flowchart TD
    A[Game Opens] -->B[Game Generates Number 1-50]
    B-->C(Take Player Next Input)
    C -->|Player Input  Within Bounds < Generated Number| D[Game Output: Too Low]-->C
    C -->|Player Input Within Bounds > Generated Number| E[Game Output: Too High]-->C
    C -->|Player Input Out Of Bounds| F[Game Output: Remember To Guess 1-50]-->C
    C -->|Player Input Non Numerical| G[Game Output: Remember To Guess Using Numerical Digits]-->C
    C-->|Player Input Correct| H[Game Output: CORRECT]
    H--> I[End Game]
    I-->J[Output: Restart Button]
    I-->K[Output: Exit Game Button]
    J-->|Option Selected|B
    K-->|Option Selected|L[Game Closes]