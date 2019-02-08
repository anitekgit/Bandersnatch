# bandersnatch-engine
Create your own adventure game

![alt text](https://i.imgur.com/Nh8cTSr.png)


This repo will be used to design and create the Bandersnatch game engine which will allow the bandersntach community to collectivly create the Bandersnatch 1984 game.

1.0 GOALS

Create a web based solution that allows users to decision points and observations and allow the community to upvote/downvote their facorite nodes.

Definitions

Coder - a Bandersnatch engine creator
User - a Bandersnatch engine user which designs builds and creates the Bandersnatch 1984 game.
Player - a Bandersnatch 1984 player  

A node is one of the following

1. Decision
2. Observation

A decision will have one or more images and exactly two decisions. Players may use left or right arrows, their mouse, or touch screen to select their choice. If more than one image is uploaded then a simple animation transition will occur. Its up to the user to ensure these images make sense. The idea is to upload similar images such that a transition will look like a cheesy animation. A player will have 10 seconds to choose.

An observation will have one or more images, text. A player may hit the spacebar, tap the screen to continue or wait 10 seconds to continue.

A decision may be followed by 0 or more decisons or 0 or more observations. likewise an observation may be followed by 0 or more decisions or 0 or more observations.

JSON example

DECISION MAKER 2.0

{
images: [],
header: "",
decisions: {0:"",path:nodeId,1:"",path:nodeId},
}

OBSERVATION

{
images: [],
header: "",
decisions: nodeId,
}

In the database the decision and the observation will be the same object: a node. The difference is whether or not a player can make a choice and go down a different path.

The engine UI will allow users to upload images, set the text for the header and decisions, and there will be a drop down that allows the user to put an existing node as the nodeId. This will link the decisions and observations creating the network. This can be left null if that path hasnt been created yet. 

1.5 GOALS

Modify the above JSON objects allowing a list of nodeIds. In the engine designer allow the community to upvote/downvote their favorite nodes. 

Allow players to play the Bandersnatch 1984 game. The game will be based on the nodes with the highest votes. This will be dynamic. If a new node is created or if the vote totals change it will automatically be reflected in the game. Players may be able to pick how they want to play the game by selecting most votes for all time, 6 months, 3 months, 1 month.

2.0 GOALS

In the Bandersnatch episode the player can navigate through a maze. Add a new node type with 4 decision points up,right,down,left.



-----------
License

THIS OR ANY DERIVATIVE WORK MAY NOT BE USED FOR COMMERCIAL PURPOSES. ANY DERIVATIVE WORK MUST ALSO CONTAIN THIS NON COMMERCIAL USE LICENSE REQUIREMENT.

Besides this restriction this code may be copied and edited and otherwise conforms to the GPL 3 license.  The restriction that this code not be used for commercial purposes superceeds the GPL 3 license. The sections where the GPL 3 license gives rights to use this code for commerical purposes are void.


