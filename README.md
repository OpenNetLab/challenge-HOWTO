# Challenge HOW-TO

## How To Participate
### Read the important information 
* Read the information from our official website [MMSys Website](https://2021.acmmmsys.org/rtc_challenge.php) carefully.

### Training your model

* You should design an algorithm to predict the bandwidth. We provide a [Gym](https://github.com/OpenNetLab/gym) to you and here is a reinforcement learning [example](https://github.com/OpenNetLab/gym-example) to demonstrate how to design a bandwidth estimator model by the [Gym](https://github.com/OpenNetLab/gym)

### Prepare your submission
You should submit your model and paper to participate the challenge. Please refer the [MMSys Website](https://2021.acmmmsys.org/rtc_challenge.php). 

#### Model submission


* You should convert your model or algorithm for [AlphaRTC](https://github.com/OpenNetLab/AlphaRTC) to a [PyInfer](https://github.com/OpenNetLab/AlphaRTC#pyinfer) instance. Here is a tiny [example](https://github.com/OpenNetLab/Challenge-Example) of acceptable submission. Meanwhile, you can verify the validation of your model following [this section](https://github.com/OpenNetLab/Challenge-Example#submission-verification). You implementation will run in the [Challenge-Environment](https://github.com/OpenNetLab/Challenge-Environment) that we pre-installed some popular third-parties library in this environment.

* You should compress all materials of your bandwidth estimator as a zip package. Here is an valid submission [example](https://github.com/OpenNetLab/Challenge-Example/archive/refs/heads/master.zip).

* Submit your materials into our evaluation system. We provide online evlaution before the deadline. Please check section [Evaluation System](#evaluation-system)


#### Paper submission

Please refer the [MMSys Website](https://2021.acmmmsys.org/rtc_challenge.php). 

## Evaluation System

We will provide two stages of the evaluation on [OpenNetLab](https://opennetlab.org), online evaluation and offline evaluation. The goals of the evaluations are different.


### Online evaluation

When a participant submit a zip, we check the basic functions of the submissions to ensure every submission can work in the offline evaluation. Each submission is scheduled to one pair of the servers randomly. The scores from the online evaluation are only for references. 

Please also read the notes below:

* We keep this submission for the offline evaluation.
* Please use the first author's email address to login this system. 
* A new submission replaces the older one.
* We limit the number of submissions for each participant to 3 times per day.

### Offline evaluation

We will start the offline evaluation after the final deadline. All submissions will be tested in different scenarios (e.g. networks and locations). Then we calculate the final cores and rank the submissions. 


## Contact
* [Google Group](https://groups.google.com/g/opennetlab-challenge)
* [Slack](https://join.slack.com/t/opennetlab-challenge/shared_invite/zt-pjn74xhx-d~jG5lY3s4_6kSJHuzfHcw)

## Important Resources
* AlphaRTC: https://github.com/OpenNetLab/AlphaRTC
* AlphaRTC Gym: https://github.com/OpenNetLab/gym
* AlphaRTC Gym-example: https://github.com/OpenNetLab/gym-example
* Challenge Runtime Environment: https://github.com/OpenNetLab/Challenge-Environment
* Challenge Submission Example: https://github.com/OpenNetLab/Challenge-Example
