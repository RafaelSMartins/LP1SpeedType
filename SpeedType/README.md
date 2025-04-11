# SpeedType​
## Diagrama UML

```mermaid
classDiagram
    class Program {
        +static void Main(string[] args)
    }

    class Game {
        +SentenceProvider sentenceProvider
        +Evaluator evaluator
        +GameResult[] gameStats
        +Game()
        +void ShowMenu()
        +void StartGame()
        +void ShowGameStats()
    }

    class GameResult {
        +double wpm
        +double TimeTaken
        +int accuracy
    }

    class SentenceProvider {
        +string[] sentences
        +Random random
        +SentenceProvider()
    }
    class Evaluator {
        +double CalculateWPM
        +int CalculateAccuracy()
        +int correctCharts
    }

    Program --> Game
    Game --> Evaluator
    Evaluator --> GameResult
    Game --> SentenceProvider
    GameResult --> Program