The code in the Anaconda environment had an error which said "too many values to unpack," so we limited the values to just the first 3. Although if we run the modified code in Google Colab, it takes much time for training. So, we have exactly the same code with just a different line.

Anaconda:
.
.
.
 
for step in range(max_steps):
        action = choose_action(state)
        new_state, reward, done = env.step(action)[0:3]
        update(state, action, reward, new_state)
        state = new_state
        rewards_current_episode += reward
.
.
.

Google colab:
.
.
.
 
for step in range(max_steps):
        action = choose_action(state)
        new_state, reward, done = env.step(action)
        update(state, action, reward, new_state)
        state = new_state
        rewards_current_episode += reward
.
.
.
