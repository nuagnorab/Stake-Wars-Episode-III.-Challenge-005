# Stake-Wars-Episode-III.-Challenge-005
Stake Wars: Episode III. Challenge 005


### Tasks: Setup a running validator node for shardnet on any one of the most popular cloud providers and document the process to create an article about it.

![image](https://user-images.githubusercontent.com/53389997/181671179-f1cca49e-aadb-4b8d-8e0e-3b9e4ba8497e.png)


For this callenge, I choose using a cloud provider named contabo.
Reason to choose contabo is that it is a well-known cloud provider with great specs and more affortable pricing.


### Follow the guide of Stake Wars III challenges:

1. Create your Shardnet wallet -> DONE

![image](https://user-images.githubusercontent.com/53389997/181671496-d7277163-fbc5-47f4-8bc7-245f4f196399.png)


There are different way to create a shardnet wallet, the easiest way for people is go to https://wallet.shardnet.near.org/create
then follow the steps to choose you own shardnet.near address.

2. Setup a validator and sync it to the actual state of the network. -> DONE

In order to setup a validator, you will need to set up a node that meet the hardware requirements.

Run the following command in the terminal to check if your server is qualify being a node/validator.

``lscpu | grep -P '(?=.*avx )(?=.*sse4.2 )(?=.*cx16 )(?=.*popcnt )' > /dev/null \
  && echo "Supported" \
  || echo "Not supported"``


If it returns "Supported" then you are good to start setting up the node for the shardnet.

https://github.com/near/stakewars-iii/blob/main/challenges/002.md

Follow the official steps and you should be able to have your node up and running.


3. Deploy a new staking pool for your validator. -> DONE

>NEAR uses a staking pool factory with a whitelisted staking contract to ensure delegators’ funds are safe. In order to run a validator on NEAR, a staking pool must be deployed to a NEAR account and integrated into a NEAR validator node. Delegators must use a UI or the command line to stake to the pool. A staking pool is a smart contract that is deployed to a NEAR account.

You must deploy a staking pool for your node/validator, so that you will get your reward for running a node.
A old wisdom once said, if you good at something, never do it for free.

Nothing better explain the process than the official page. You can go through the steps and have your node mounted.

https://github.com/near/stakewars-iii/blob/main/challenges/003.md

4. Setup tools for monitoring node status. -> DONE

The easiest way to monitor the node status would be running this command in the CLI:

``journalctl -n 100 -f -u neard | ccze -A``
