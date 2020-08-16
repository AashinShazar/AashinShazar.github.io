---
name: EMILA
tools: [Embedded-Systems, C, Machine-Learning, Python]
image: https://www.sciencefriday.com/wp-content/uploads/2018/09/robotarm.png
description: An Investigation into Robotic Prosthetics
---

# Project EMILA
![Project Preview](http://ashazar.me/assets/EMILA-GIF.gif)

## What Is It?
Project EMILA is a cursory investigation into robotic prosthetics. This project essentially gathers EMG data from EMG sensors and has it interpreted by a machine learning classifier to perform a previously mapped gesture. Much of robotic prosthetics technology is still in its infancy and this project was made to learn more about this growing field and where this technology stands today.

## How Does It Work?
The heart of the project lies with the usage of the PSOC 5LP which is a microcontroller that collects data from the EMG sensor. This is then transmitted to a locally connected computer where a trained Convolutional Neural Network (CNN) will predict the gesture performed and move the appropriate servo motors on the robot arm.

## Biggest Challenges
The biggest challenge I faced working on this project was just how difficult it was to collect data and train a CNN classifier. The very nature of collecting surface EMG data is difficult because of the wide variability presented by muscle fatigue, muscular cross talk, sensor positioning, gesture length, gesture intensity and so many other factors. It took a careful design of data collection experiments to build up a robust dataset.

## Future Improvements
If I were to tackle this project again in the future, I would definitely look into implementing a sliding window so that gestures can be continuously predicted by the CNN classifier without discrete set time limits. I would also look into incorporating a higher density of EMG sensors to investigate more complicated gestures and the involved training complexity.  

## Cost and Equipment
These were some of the major components used in this build:

-   [PSOC 5LP ($10)](https://www.cypress.com/products/32-bit-arm-cortex-m3-psoc-5lp)
-   [Robot arm kit ($52)](https://www.amazon.com/gp/product/B076Q4DYPN/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
-   [MyoWare EMG Sensor ($38)](https://www.amazon.com/MyoWare-Muscle-Sensor/dp/B018TIWR32/ref=sxts_sxwds-bia-wc-p13n1_0?cv_ct_cx=myoware&dchild=1&keywords=myoware&pd_rd_i=B018TIWR32&pd_rd_r=8ebbfe19-06c1-483e-8af4-cd2674677524&pd_rd_w=FpbKs&pd_rd_wg=SsheD&pf_rd_p=13bf9bc7-d68d-44c3-9d2e-647020f56802&pf_rd_r=JMNYYTN6589HHHYSP1KF&psc=1&qid=1597620946&sr=1-1-791c2399-d602-4248-afbb-8a79de2d236f)


### Check out the full project here: [https://github.com/AashinShazar/EMILA](https://github.com/AashinShazar/EMILA)



