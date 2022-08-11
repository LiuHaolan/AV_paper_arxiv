# [Learning by Cheating](https://arxiv.org/abs/1912.12294)

tl;dr: Two stage training process for end-to-end AV: first train a priviledged agent by observing the groundtruth layout of all traffic participants. Then train a student agent supervised by the priviledged networks.

#### Overall impression
Intuitively, end to end driving comprises two tasks: perception and planning. By decomposing the task into two stages, 
the teacher network only needs to learn to plan and distills such knowledge to the student networks.

#### Key ideas
- train a priviledged agent can provide stronger supervision than original expert, as it can be queried from any states of the environment. 
	- In particular, if the privileged agent is trained via conditional imitation learning, it can provide an action for each possible command (e.g., “turn left”, “turn right”) in the second stage, all at once, in any state of the environment

#### Technical details

#### Notes

