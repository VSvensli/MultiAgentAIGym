# MultiAgentAIGym

This gym mimics other OpenAI gyms



## Example

```python
# Spesify number of agents
n_agents = 1

start_positions = [[100,100]]
goal_positions = [[20,20]]

# Initialize environment
env = points(n_agents,obstacles)

# Reset the simulation, with the option to spesify start positions or pick random(default)
env.reset(start_positions,goal_positions)

for i in range(100):
    action = np.random.randint(0,4,n_agents)
    
    # Progress the simulation by one frame and take on action [0...3]
     states, actions, rewards, dones = env.step(action)
    
    # Render the environment
    env.render()
    
    # Close the environment if all agents are done
    if env.get_dones().all():
        break
env.close()
```

