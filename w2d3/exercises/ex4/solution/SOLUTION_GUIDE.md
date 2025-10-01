### Solution Guide — ex5: Becoming number 1

#### Overview
The developer has created a cool game for their website! You are an apple going around a map and eating snakes to get faster and faster. All snakes are the same size and eating one increases the apple tree by one. When you hit one of the walls, you fail. The apple is always one game pixel and the snakes are also one game pixel.

The developer wants customers to be able to download their game state and continue playing afterward. So you can just download the game state and upload a modified state that gives a high score.

Download any game state and save it as test.pkl 

```python

import pickle
with open("test.pkl", "rb") as f:
    s = f.read()
a = pickle.loads(s)
a['apple_size'] = 100000
with open("hacked.pkl", "wb") as f:
    pickle.dump(a,f)
```

Then upload the hacked.pkl file to the game and you will be the number 1 player!

```python
# create pickle files
python sample_exploit.py
```