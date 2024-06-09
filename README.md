# Mini4Pro-NLD-booster
My approach to installing the NLD booster board on a DJI Mini 4 Pro and DJI RC2

NOTE: i am not going to explain how to disassemble the drone and the remote, you can easily find video on youtube such as those:
- DJI RC that works also for RC2: https://youtu.be/dhpUh3fc1Z8?feature=shared
- DJI Mini 4 Pro: https://youtu.be/rLTtYpftaGs?feature=shared

# Tools needed (bare minimum)
- soldering iron with a very thin tip and capable of reacjing 370 celsius
- siliconic non electrically conductive but heat condictive siliconic glue such as this one: ![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/05fa59b5-0899-4a57-8c42-96d34da0456c)
- a sharp blade to scrape the PCB mask off the contacts
- optional but highly recommended: some cheap tools to open electronic devices such as this: 
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/1843b34b-822d-4131-877a-8ffd9445f0dc)
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
4) solder the wires according to the following pin out and cover with siliconic heat-conductive glue
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/608f404f-bf55-4f45-9285-c477f946c045)
5) connect the step-down voltage converter to the battery and the booster board
6) connect the EN pin of the step-down voltage converter to the inductance labelled with 2R2 as shown in the picutre below and cover with the siliconic heat conductive glue
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/36ae4c4b-cdec-4184-966e-194c705ca234)

7) glue with the siliconic glue the step-down converter board to the top of the obstacle avoidance sensors cluster
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/acf56544-9b1f-4797-a69d-4abd694ea382)

## Connect the antenna
8) disconnect the antenna connector labelled with ANT0 and connect the booster board (ANT0 has the longest cable thus it is able to reach the booster board, any antenna connector will work in any case, as long as the cable can reach the booster board)
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/03b3d8e2-6a84-45ec-a3e0-eb8eeaa03f49)
## Secure everything
9) glue with the siliconic glue the booster board to the piece of aluminum between the GPS antenna and the obstacle avoidance sustem sensors cluster
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/9d652ff4-1140-48fb-ae1a-3e01125bc222)
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/1956cbc5-61b9-47f3-9cd1-ac2f8484f3d7)

# Installing the booster on the RC2
Once you have disassembled rhe remote, carefully remove the fan assembly and the aluminum heatsink without touching the thermal conductive paste

## Connect to power
1) I found that the easiest access to power is through the left side battery (keep the antennas facing up to orient yourself), using the two little pads (one is squared and the other is a cirle) just right next to the battery connector.
Solder the positive and negative and connect to the step-up voltage coverter and cover the connection with siliconic glue. There is no need to scrape the pads as they are not covered by PCB mask. 
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/cec723eb-462c-4139-935e-6841dcf1bac1)

2) connect the EN pin of the step-up voltage converter to the first top-most pin of the ribbon connector of the C1 and C2 buttons on the back of the remote that you have now separated already. Solder and cover with siliconic glue
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/7e6ac07b-75d9-43c9-b5c1-3940e404a2eb)

## Connect the antenna
After several trials and tests I came up with this odd but working solution.
1) disconnect the two external antennas from the PCB (the ones identified with the labels "G" and "ANT0")
2) using pliers you can remove the two external antennas from the body of the remote and swap them (the right antenna will go on the left and vice versa) - be careful: the antennas do not rotate 360 degrees so when you insert them back in place you need to orient them correctly in order to be able to slide them into the hole
We are doing this because the cable of the right antenna is too short to reach the booster board (which we will place on the left of the fan), and we cannot use the left antenna as it is identified by the label G so I suspect it is the GPS antenna which we dont need to boost (and it uses a different frequency so it would be useless to connect the booster board). I tried using the internal antenna identified by the label "ANT0" and I got still decent but poorer results compared to the right external antenna.
antenna.
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/3cff1b01-c062-45b3-beeb-f33909ffa8db)

4) Connect the cable of the antenna that is now on the left to the booster board and complete all the connections also for power

## Physical modifications to the body of the remote
1) cut off this piece of plastic from the back of the body of the remote to fit the board
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/e6333a9b-da95-4164-acf3-165689e58cce)
2) cut off this piece of plastic from the fan duct assembly (for two reasons: i) to improve airflow; ii) if you don't do it, once you glue the board to the heat sink, you will cover some screws and it won't be possible to disassemble the fan and heatsink)
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/59d0e651-37a3-4100-9e96-f713d4776a4f)


## Secure the board
1) Using some heat shrink tube, protect the step-up voltage converter and place it somewhere on the top of the remote close to the buzzer
2) Using siliconic heat conductive glue, glue the booster board to the piece of aluminum heatsink that is not covered by the fan assembly
![image](https://github.com/giovi321/Mini4Pro-NLD-booster/assets/6443515/d2d91e7d-abeb-4c0f-bdb0-3e98d0601fbf)
