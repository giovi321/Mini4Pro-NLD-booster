# Mini4Pro-NLD-booster
My approach to installing the NLD booster board on a DJI Mini 4 Pro and DJI RC2

NOTE: i am not going to explain how to disassemble the drone and the remote, you can easily find video on youtube such as those:
- DJI RC that works also for RC2: https://youtu.be/dhpUh3fc1Z8?feature=shared
- DJI Mini 4 Pro: https://youtu.be/rLTtYpftaGs?feature=shared

# Tools needed (bare minimum)
- soldering iron with a very thin tip and capable of reacjing 370 celsius
- siliconic non electrically conductive but heat condictive siliconic glue such as this one: ![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/fb9df867-cef5-47da-afac-7003497bc3ed)

- a sharp blade to scrape the PCB mask off the contacts
- optional but highly recommended: some cheap tools to open electronic devices such as this: 
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/f758fa75-01d6-4dda-90e6-f5000c77d285)

- electronic tester to check for polarity and connections
- torx, hexagonal and phillips screwdrivers

# General recommendations for the installation
- use siliconic non electircally conductive but heat conductive glue to protect all new solder joints
- use hot glue to stabilize antenna connections, so its easier to remove if you ever need to
- use some heatsinks: the ones provided by NLD are decent but not the best (even though I have succesfully used them, on amazon you can easily find better solutions). Both the boards need a heatsink: in my explanation I didnt say it but I did use the heatsibks on both devices. 
- the battery connectors on the drone need to be scraped with a blade in order to be able to solder onto them

# Installing the booster on the Mini 4 Pro
Once you have taken the drone apart, you need to follow these steps

## Connect power
1) remove the main board and the obstacle avoidance cameras from the top
2) remove the three torx screws holding the battery connector in place and gently lift the battery connector from its place but do not remove it completely as it is not needed - I dont have pictures but you sinply have to remove the screws from the hole where the battery goes, then from the top of the drone (underneath the obstacle avoidance cameras) push a bit with tweezers the little PCB where the battery connector is installed. Now ok the back of the pcb lift gently the piece of adhesive plastic and you will expose the back side of the battwry connector. Here you need to identify correctly the contacts with the positive and negative and solder the wires that will go to the step-down voltage converter. 
3) using a sharp blade, scratch the back of the connector to remove the masking from the PCB so that you can solder the wires - it will take quite some time to make the solder stick to those pads, don't over heat it (350 celsius is fine) and if it does not work just keep scraping them with a blade
4) solder the wires according to the following pin out of a Mini 4 Pro battery and cover with siliconic heat-conductive
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/85232647-8a49-44d1-b3a3-88f20bb655ff)

6) connect the step-down voltage converter to the battery and the booster board
7) connect the EN pin of the step-down voltage converter to the inductance labelled with 2R2 as shown in the picutre below and cover with the siliconic heat conductive glue
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/4d84ec24-1892-418b-a313-3f99b1996834)


8) glue with the siliconic glue the step-down converter board to the top of the obstacle avoidance sensors cluster
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/6e45433c-1c5e-4add-b2a9-b0326a34729f)


## Connect the antenna
8) disconnect the antenna connector labelled with ANT0 and connect the booster board (ANT0 has the longest cable thus it is able to reach the booster board, any antenna connector will work in any case, as long as the cable can reach the booster board)
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/7903fb15-44de-485e-b4e8-a11b95d597a6)

## Secure everything
9) glue with the siliconic glue the booster board to the piece of aluminum between the GPS antenna and the obstacle avoidance sustem sensors cluster
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/0cf86dd7-0990-4a75-bb7f-b0593a43f2f9)
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/ce52ea50-1f77-40a8-8729-f0c561dd3514)


# Installing the booster on the RC2
Once you have disassembled rhe remote, carefully remove the fan assembly and the aluminum heatsink without touching the thermal conductive paste

## Connect to power
1) I found that the easiest access to power is through the left side battery (keep the antennas facing up to orient yourself), using the two little pads (one is squared and the other is a cirle) just right next to the battery connector.
Solder the positive and negative and connect to the step-up voltage coverter and cover the connection with siliconic glue. There is no need to scrape the pads as they are not covered by PCB mask. 
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/1144d95c-4b53-4d06-9aa7-2db23c76e58d)


2) connect the EN pin of the step-up voltage converter to the first top-most pin of the ribbon connector of the C1 and C2 buttons on the back of the remote that you have now separated already. Solder and cover with siliconic glue
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/d6538b95-d831-4211-81aa-60e8f58ce8e2)


## Connect the antenna
After several trials and tests I came up with this odd but working solution.
1) disconnect the two external antennas from the PCB (the ones identified with the labels "G" and "ANT0")
2) using pliers you can remove the two external antennas from the body of the remote and swap them (the right antenna will go on the left and vice versa) - be careful: the antennas do not rotate 360 degrees so when you insert them back in place you need to orient them correctly in order to be able to slide them into the hole
We are doing this because the cable of the right antenna is too short to reach the booster board (which we will place on the left of the fan), and we cannot use the left antenna as it is identified by the label G so I suspect it is the GPS antenna which we dont need to boost (and it uses a different frequency so it would be useless to connect the booster board). I tried using the internal antenna identified by the label "ANT0" and I got still decent but poorer results compared to the right external antenna.
antenna.
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/f2bc9e08-3cb4-4564-bdf7-241a2d84e6b5)


4) Connect the cable of the antenna that is now on the left to the booster board and complete all the connections also for power

## Physical modifications to the body of the remote
1) cut off this piece of plastic from the back of the body of the remote to fit the board
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/f35226de-ad03-4066-93e3-cf653aedede5)

2) cut off this piece of plastic from the fan duct assembly (for two reasons: i) to improve airflow; ii) if you don't do it, once you glue the board to the heat sink, you will cover some screws and it won't be possible to disassemble the fan and heatsink)
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/33c829ed-c83b-4500-8a85-00e149a86f4c)

## Secure the board
1) Using some heat shrink tube, protect the step-up voltage converter and place it somewhere on the top of the remote close to the buzzer
2) Using siliconic heat conductive glue, glue the booster board to the piece of aluminum heatsink that is not covered by the fan assembly
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/9688204c-b10f-492b-966f-5c18c4167203)
