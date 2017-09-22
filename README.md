# chatter
A Mycroft AI chatbot solution framework, currently under development.  Will use Mycroft AI docker image as the base for running it.

Currently the goal is for this to use mycroft skills for its responses and [Errbot](https://errbot.io) for the backend and connection to chat applications.

A demo version of this bot can be seen in the Mattermost community for MycroftAI at https://chat.mycroft.ai and the name of the bot is @mycrofthelper

Still a work in progress

## Installation
First you need to decide if you are going to use SSL for this bot or not.  If just for testing you can not setup SSL/WSS.  The different steps are listed below.

**Please Note:** For our setup we are using docker to just make it easier since we are only dealing with text you can still use a normal mycroft instance but then you will have to setup your own type of proxy, etc.

For instructions on setting up docker please refer to their documentation at: https://docs.docker.com/engine/installation/

### SSL Setup
We are currently using the submodule https://github.com/Geeked-Out-Solutions/mycroft_proxy and this is the proxy folder.  So you can check out the proxy folder README.md file for instructions.

Once you have setup the docker container you can follow the rest of the guide for setting up your chatbot.


### Non SSL Setup
If you want you don't have to use the docker setup you can just setup a mycroft instance or you can just setup a basic docker instance using the following info:
 
Just replace the directory_on_local_machine with where you want the container mapped on your local machine, IE /home/user/mycroft for example if you created a mycroft folder in your home directory. This is so the pairing file is stored outside the container. If you wanted to run unstable then you would do mycroftai/docker-mycroft:unstable in the below command to run it on the unstable tag instead of latest which is the default.

`docker run -itd -p 8181:8181 -v directory_on_local_machine:/root/.mycroft mycroftai/docker-mycroft` - For stable

`docker run -itd -p 8181:8181 -v directory_on_local_machine:/root/.mycroft mycroftai/docker-mycroft:unstable` - For unstable


## Setup
Now you have a mycroft instance setup and we need to configure how we want to interact with our instance.

### Web Client
TBD

### Slack
We will use the errbot backend framework and a mycroft plugin that will interact with the instance.

### Mattermost
We will use the errbot backend framework and a mycroft plugin that will interact with the instance.

### Discord
We will use the errbot backend framework and a mycroft plugin that will interact with the instance.
