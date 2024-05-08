## Game Overview

<img width="1523" alt="image" src="https://user-images.githubusercontent.com/61567222/225745302-c8d349b0-b234-45eb-8d35-3c6002ffdcd9.png">
<img width="1459" alt="image" src="https://user-images.githubusercontent.com/61567222/225775912-fa3b0251-0d3c-49c9-a7e8-e40ab9c39fcd.png">


### How to play

1. Click 'Start Game'

2. Follow the instructions on the right panel to play, the icons on the top right indicates the current turn (highlight)

<img width="550" alt="image" src="https://user-images.githubusercontent.com/61567222/225772807-2405b4b5-7081-461b-8cb9-ea492bf75c64.png">
<img width="556" alt="image" src="https://user-images.githubusercontent.com/61567222/225772850-944a510a-5f57-4aef-809d-f6db82dd01e2.png">



3. If you want to restart the game, click on the 'Start Game' again

4. If you want to undo, just click the 'Undo' button.

5. God cards and AI mode are available.


### AI Mode

1. When game starts, choose the 'AI' button.

2. Select your god card and select the god card for AI.

3. After you finished your step, the AI will instantly finishes its steps. Look carefully of what has AI done.

4. Use 'Undo', you can undo both your actions and AI's actions. If you undo AI's actions in the middle, you should help AI to choose one step to resume the game. For example, if you use undo and stop at when AI should select a worker, you should help AI select 1 worker and AI will automatically finishes its remaining steps until your turn begins or game ends.

<img width="504" alt="image" src="https://user-images.githubusercontent.com/61567222/227383401-dbc65aa0-4401-44bc-b523-3bea140d2eba.png">


### Undo

The undo action is implemented by creating a board store to store each states of the board after every step. Each object is deep copied (deep cloned) to be immutable. Therefore, the changing of the current game states will not influence the states stored in the board store object. The store object is basically a stack. When undo action is called. The previous states will be popped out of the stack and the current states will be overwritten by the previous states to realize a undo action.

<img width="573" alt="image" src="https://user-images.githubusercontent.com/61567222/227383765-3f793b0d-4555-43d5-9d5e-2f5cfc003a9d.png">


### God Cards

1. 3 God cards are implemented. The card that gives no power to the player is called the 'Fool' card.

2. No 2 players can select the same god card. However, both players can choose 'Fool' card at the same time. It's also ok for one player to choose 'Fool' card while the other chooses god card.

3. God cards actions are compatible with undo action.

4. For Demeter, after the first tower/dome is built, the game will allow the player to build again (no same place with the previous action). Player can click the block where worker occupied to cancel the second build.

5. Please remember the god cards selected or refer to the top of the history board to see your selections for both players.

<img width="1148" alt="image" src="https://user-images.githubusercontent.com/61567222/227383465-9259cba9-9b15-453d-ac17-b3865a612cdb.png">

<img width="1136" alt="image" src="https://user-images.githubusercontent.com/61567222/227383499-07b0c636-5f6c-48c4-a032-be667faa8e52.png">


### History Board

History Board generally stores the actions taken by both players and it also indicates the next move the player can take.

<img width="573" alt="image" src="https://user-images.githubusercontent.com/61567222/227383552-af85cebe-ff48-4e98-8a9a-95dc895af856.png">

<img width="572" alt="image" src="https://user-images.githubusercontent.com/61567222/227383634-ca41bc14-75fc-4d2f-805b-c295039a5db2.png">



### Winning Requirement

1. One of the workers of the player reaches the 3rd level.

or

2. Both of the workers of the opponents cannot move or build.




**HAVE FUN!**