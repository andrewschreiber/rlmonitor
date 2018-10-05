# RLmonitor
Tensorboard plugin for visualizing reinforcement learning

## Setup
Clone the repo.

### Run Cartpole with DQN
    cd examples/baselines

Follow instuctions from https://github.com/andrewschreiber/baselines to
install Gym. Then:

Train a model:

    python -m baselines.run --alg=deepq --env=CartPole-v0 --save_path=./cartpole_model.pkl --num_timesteps=1e5

Visualize playing the model:

    python -m baselines.run --alg=deepq --env=CartPole-v0 --load_path=./cartpole_model.pkl --num_timesteps=0 --play

# Next steps
- [ ] Setup Repo
  - [x] DQN code
  - [x] DQN attached to tensorboard
  - [ ] Tensorboard plugin example
- [ ] Understanding
  - [x] DQN
  - [ ] Tensorboard
  - [ ] Tensorboard plugins
  - [ ] Polymer.js
  - [ ] t-SNE
