```mermaid


graph TD;

    subgraph "package farkle"
        A[InitGame class] --> B[MainGame class];
        B --> C[GUI class];
        C --> D[Application class];
        C --> E[ComputerPlayer class];
        C --> F[HumanPlayer class];
        C --> G[Player abstract class];
        C --> H[Die class];
        C --> I[Difficulty enum];
    end

    subgraph "InitGame class"
        J[Initialize initPanel];
        J --> K[Initialize humanPlayerPanel];
        J --> L[Initialize computerPlayerPanel];
        J --> M[Initialize humanPlayersCount];
        J --> N[Initialize computerPlayersCount];
    end

    subgraph "MainGame class"
        O[Initialize mainPanel];
        O --> P[Initialize diceContainer];
        O --> Q[Initialize buttonContainer];
        O --> R[Initialize southContainer];
        O --> S[Initialize diceButtons];
        O --> T[Initialize rollButton];
        O --> U[Initialize stopButton];
        O --> V[Initialize scoreButton];
        O --> W[Initialize currentScoreLabel];
        O --> X[Initialize totalScoreLabel];
        O --> Y[Initialize currentRoundLabel];
        O --> Z[Initialize buttonState];
        O --> AA[Initialize dieValue];
        O --> AB[Initialize PLAYABLE_DIE];
        O --> AC[Initialize SCORE_DIE];
        O --> AD[Initialize LOCKED_DIE];
        O --> AE[Initialize currentRound];
        O --> AF[Handle Dice Button Pressed];
        O --> AG[Handle Stop Button Pressed];
        O --> AH[Handle Score Button Pressed];
        O --> AI[Handle Roll Button Pressed];
        O --> AJ[Reset Dice];
    end

    subgraph "GUI class"
        AK[Initialize playerList];
        AK --> AL[Initialize playerTurnCount];
        AK --> AM[Initialize initGame];
        AK --> AN[Initialize frame];
        AK --> AO[Initialize cardsPanel];
        AK --> AP[Initialize cardLayout];
        AK --> AQ[Initialize submitButton];
        AK --> AR[Initialize endTurnButton];
        AK --> AS[Load InitGame];
        AK --> AT[Load nextPlayer];
    end

    subgraph "Application class"
        AU[Main method];
        AU --> AV[Create GUI object];
    end

    subgraph "Player class"
        AW[Initialize name];
        AW --> AX[Initialize currentScore];
        AW --> AY[Initialize totalScore];
        AW --> AZ[Constructor: Player(name)];
        AW --> BA[getName()];
        AW --> BB[setName(name)];
        AW --> BC[getCurrentScore()];
        AW --> BD[setCurrentScore(currentScore)];
        AW --> BE[getTotalScore()];
        AW --> BF[setTotalScore(totalScore)];
    end

    subgraph "Difficulty enum"
        BG[Initialize EASY];
        BG --> BH[Initialize HARD];
    end

    subgraph "Die class"
        BI[Initialize numOfSides];
        BI --> BJ[Initialize faceValue];
        BI --> BK[Constructor: Die(numOfSides, faceValue)];
        BI --> BL[getNumOfSides()];
        BI --> BM[setNumOfSides(numOfSides)];
        BI --> BN[getFaceValue()];
        BI --> BO[setFaceValue(faceValue)];
        BI --> BP[roll()];
        BI --> BQ[rollDice(diceList)];
        BI --> BR[getDiceString(diceList)];
    end

    subgraph "HumanPlayer class"
        BS[Constructor: HumanPlayer(name)];
    end

    subgraph "ComputerPlayer class"
        BT[Constructor: ComputerPlayer(name)];
        BT --> BU[Constructor: ComputerPlayer(name, difficulty)];
        BT --> BV[getDifficulty()];
        BT --> BW[setDifficulty(difficulty)];
    end
```
