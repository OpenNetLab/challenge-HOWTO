# Challenge

## How To Participate

Please refer to our [challenge homepage](https://2021.acmmmsys.org/rtc_challenge.php) for challenge introduction.

1. You should design an algorithm to predict the bandwidth. We provide a [Gym](https://github.com/OpenNetLab/gym) to you and here is a reinforcement learning [example](https://github.com/OpenNetLab/gym-example) to demonstrate how to design a bandwidth estimator model by the [Gym](https://github.com/OpenNetLab/gym).

2. You should convert your model or algorithm for [AlphaRTC](https://github.com/OpenNetLab/AlphaRTC) to a [PyInfer](https://github.com/OpenNetLab/AlphaRTC#pyinfer) instance. Here is a tiny [example](https://github.com/OpenNetLab/Challenge-Example) of acceptable submission. Meanwhile, you can verify the validation of your model following [this section](https://github.com/OpenNetLab/Challenge-Example#submission-verification). You implementation will run in the [Challenge-Environment](https://github.com/OpenNetLab/Challenge-Environment) that we pre-installed some popular third-parties library in this environment.

3. You should compress all materials of your bandwidth estimator as a zip package. Here is an valid submission [example](https://github.com/OpenNetLab/Challenge-Example/archive/refs/heads/master.zip).

4. We will dispatch your submission to two nodes of [OpenNetLab](https://opennetlab.org/) platform and configure them to establish a RTP call. Finally, we will collect the output video, output audio and AlphaRTC log as the input to [the evaluation system](https://github.com/OpenNetLab/Challenge-Environment/tree/master/metrics).

## Evaluation System

Actually, we will have two evaluation system, online and offline.

The online system will just provide a crude score which will not be used as rank but used to tell the contestant the submittal is accepted to our system. This part have been published in the github repository.

The offline system will be used as rank, it's almost same as the online evaluation system but will add more test cases and complex frame alignment algorithm. It will also be published in this repository about the end of May.

## Notes
* Model Upload Limitation

