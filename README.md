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

* Submit your materials into our OpenNetLab platform. We provide online evaluation before the deadline.

##### Notes

* Please use the first author's email address to login this system. 
* We only store your last submission for evaluation.
* We limit the number of submissions for each participant to **3** times per day.


#### Paper submission

Please refer the [MMSys Website](https://2021.acmmmsys.org/rtc_challenge.php). 


## Evaluation System

We will provide two stages of the evaluation on [OpenNetLab](https://opennetlab.org), online evaluation and offline evaluation. The goals of the evaluations are different.


### Online evaluation

When a participant submit a zip, we check the basic functions of the submissions to ensure every submission can work in the offline evaluation. Each submission is scheduled to one pair of the servers randomly. The scores from the online evaluation are only for references. 


### Offline evaluation

We will start the offline evaluation after the final deadline. All submissions will be tested in different scenarios (e.g. networks and locations). Then we calculate the final cores and rank the submissions. 

## Final Score

The final score is divided into three parts video , audio and network. The specific formula is as follows :

```
final_score = w1 * video_score + w2 * audio_score + network_score
```

The different parts of score can be calculated by the method below :

- video_score = Vmaf score
- audio_score = 100 if DNSMOS score > ground_truth * binarize_bound else 0
- network_score = w3 * delay_score + w4 * receive_rate_score + w5 * loss_score

For each part of the network score, they can be calculated as follows :

- delay_score = 100 * (max_delay - delay_95th) / (max_delay – min_one_way_delay)
- receive_rate_score = 100 * recv_rate / ground_truth
- loss_score = 100 * (1 - loss_rate) 

What we should notice is that some parts of score still can not get full marks in an ideal environment. For example, audio_score and receive_rate_score. So we set the ground_truth to scale the related parts of score, which provide the score that can be obtained in an ideal environment.

To tune the model, we ran multiple experiments in NetEm to test the performance of simple bandwidth estimator algorithms. The experiments lead us to set the coefficients as follows :

```
w1, w2, w3, w4, w5 = 0.2, 0.1, 0.2, 0.2, 0.3
```


## Contact
* [Google Group](https://groups.google.com/g/opennetlab-challenge)
* [Slack - ACM MMSys - 2021-gc-opennetlab](https://join.slack.com/t/acmmmsys/shared_invite/zt-epd55fpy-pXGkBflmdiZr9Jm~AcgsbA)

## Important Resources
* AlphaRTC: https://github.com/OpenNetLab/AlphaRTC
* AlphaRTC Gym: https://github.com/OpenNetLab/gym
* AlphaRTC Gym-example: https://github.com/OpenNetLab/gym-example
* Challenge Runtime Environment: https://github.com/OpenNetLab/Challenge-Environment
* Challenge Submission Example: https://github.com/OpenNetLab/Challenge-Example
