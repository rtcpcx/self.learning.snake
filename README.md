# self.learning.snake.game
Developed an intelligent Snake game  using reinforcement learning techniques.
# How To Play and see Neural Network in action
* Step 1: Download all file's and save accordingly in a file named snake pygame.
* Step 2: Open new terminal at folder .
* Step 3: Write "conda activate pygame_env" in terminal .
* Step 4: Write "python agent.py" in terminal .
* Step 5: Launch and see reinforcement learning in work .

# Steps Envolved 
# Step 1: Importing Necessary Libraries
* Import the required libraries, including torch (PyTorch), random, numpy, deque, and modules specific to your Snake game.
# Step 2: Defining Constants and Hyperparameters
* Set constants and hyperparameters for your Snake game, such as MAX_MEMORY, BATCH_SIZE, and LR (learning rate).
# Step 3: Creating the Agent Class
* Define the Agent class, which represents the intelligent agent controlling the Snake game.
# Step 4: Initializing Agent Parameters
* Inside the Agent class constructor, initialize parameters like the number of games played (n_games), exploration rate (epsilon), discount rate (gamma), memory buffer (memory), the neural network model (model), and the Q-learning trainer (trainer).
# Step 5: Defining the get_state Method
* Implement the get_state method, which calculates the current state of the game. It assesses dangers, movement direction, and food location.
# Step 6: Implementing the remember Method
* Create the remember method to store experiences (state, action, reward, next_state, done) in the agent's memory buffer.
# Step 7: Implementing the train_long_memory Method
* Define the train_long_memory method to train the agent's Q-network using experiences sampled from the memory buffer.
# Step 8: Implementing the train_short_memory Method
* Implement the train_short_memory method for updating the Q-network based on a single experience.
# Step 9: Implementing the get_action Method
* Create the get_action method to determine the agent's action based on the current state. It balances exploration and exploitation.
# Step 10: Defining the train Function
* Define the main training loop in the train function.
* Initialize variables for tracking game statistics, create an instance of the agent, and initialize the Snake game.
* Enter a while loop for continuous training and gameplay.
* Inside the loop:
* Get the current state of the game.
* Determine the agent's action.
* Execute the action and receive the reward and new state.
* Train the agent's short-term memory with the experience.
* Remember the experience in the agent's memory buffer.
* If the game is done (snake collision), reset the game, increment the game count, and train the agent's long-term memory.
* Update and display game statistics, including the score and record.
* Plot and visualize the game's progress.
# Step 11: Main Execution Block
* In the main block of the script, call the train function to start the training process.
This code represents a reinforcement learning approach to train an AI agent to play the Snake game. The agent learns to make decisions (actions) by observing the game's state and receiving rewards, ultimately aiming to maximize its score over multiple games. The training loop continues indefinitely until you manually stop it, and it periodically saves the model when a new high score is achieved.
