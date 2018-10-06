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

See the model playing Carptole:

    python -m baselines.run --alg=deepq --env=CartPole-v0 --load_path=./cartpole_model.pkl --num_timesteps=0 --play


### Tensorboard
To visualize training, use the following commands to setup Baselines to
send tensorboard log files.

    export OPENAI_LOG_FORMAT='stdout,log,csv,tensorboard'
    export OPENAI_LOGDIR=log_data

In a seperate terminal tab/window, reactive your python virtual
environment and in the rlmonitor directory run:

    tensorboard --logdir log_data/tb

Return to the original terminal tab and run your training:

    python -m baselines.run --alg=deepq --env=CartPole-v0 --save_path=./cartpole_model.pkl --num_timesteps=1e5

Go to the linked URL in the tensorboard tab to see your model train.

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
