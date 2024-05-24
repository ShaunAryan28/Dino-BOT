# Dino-BOT

DINO Game Playing AI Bot

*This is a bot that can play the Chrome dinosaur game using artificial intelligence. The bot uses a deep Q-learning algorithm to learn how to jump over cacti and avoid obstacles.  

*Requirements:  
-Python 3.6+, 
-NumPy,  
-OpenCV,   
-Matplotlib,  
-Pytesseract,  
-gym,  
-mss,  

-Output:  
The bot will start playing the game and will try to learn how to jump over cacti and avoid obstacles. The bot will also print out its score and the number of steps it took to reach that score.

>NOTE: You must have a FOLDER named Train and logs in the same directory.

##usage  
>NOTE: Open the Dino game(Chrome://Dino) in the background, minimize your notebook,  move the window to the edge and then run it.

>"model.learn(total_timesteps=9000000, callback=callback)"  
>Makes the model run for the required timesteps and learn(the higher the better)

-I have made a few logs for testing, so you could use one of the pretrained model --> (https://github.com/ShaunAryan28/Dino-BOT)
just Download the best_model and save it in the same directory.

-To use it:
Run the following code:
step1-  
``` model.load('Train/best_model_88000') ```


step2-
```for episode in range(10): 
    obs = env.reset()
    -done = False
    -total_reward = 0
    -while not done: 
        -action, _ = model.predict(obs)
        -obs, reward, done, info = env.step(int(action))
        -time.sleep(0.01)
        -total_reward += reward
-print('Total Reward for episode {} is {}'.format(episode, total_reward))
-time.sleep(2)
```
##END##

