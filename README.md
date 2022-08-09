# UWB-DRL-PHY-Runtime-Adaptation-dataset
Dataset for the paper: "Deep reinforcement learning for automatic run-time adaptation of UWB PHY radio settings"

## OfficeLab
The OfficeLab from of imec - IDLab - Ghent University (https://www.ugent.be/ea/idlab/en/research/research-infrastructure/officelab.htm) offers a test environment which includes 3 floors that ar equipped with 40 Intel NUC nodes, supporting several Wi-Fi and sensor technologies including UWB. In this dataset, a single floor that has a total area of around 41 x 26 m2 and 15 UWB nodes placed in corridors, meeting rooms, and offices was used. All nodes are placed at the same height of around 2.6 m above the floor. The walls separating the rooms consist of heterogeneous materials, ranging from plywood to reinforced concrete, resulting in a very heterogeneous environment. A picture of the lab and an overview of the layout of the nodes is shown below.

![image](https://user-images.githubusercontent.com/17097984/183634631-ccd4684b-cd7a-43e0-bb9a-d46c140b670c.png)

## Dataset

The dataset was gathered using Wi-PoS: a Low-Cost UWB Hardware Platform with Long Range Sub-GHz Backbone (https://www.mdpi.com/1424-8220/19/7/1548). All 15 nodes are programmed once as tag and try to range with the other 14 nodes (anchors) using all possible combinations (72 int total) of the settings shown in the table below.

![image](https://user-images.githubusercontent.com/17097984/183636132-ea32a56f-40e5-4d82-ad5e-65206d5e9c4a.png)

ADS-TWR is used to enable accurate ranging. In the bidirectional communication, both nodes log their raw responses, which are then combined and converted to
a more readable file format, e.g., csv. Each row of the dataset corresponds to one range between two nodes and contains the distance estimation and the available link state information that is needed in the algorithms. All devices have ranged with each other for a total of 500 range attempts per combination. This resulted in a total of more than 605 thousand ranges overall. This is considerably less than the total attempts, as on average each node could only range with 7 other nodes due to obstacles like walls.


## Availability
The dataset is available on request at dieter.coppens@ugent.be and will be made publicly available on the github page after publication of the paper.
