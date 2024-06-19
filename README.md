# Crazyflie-2.0-battery-data

This is a dataset gathered from 155 individual flights using a Crazyflie 2.0 drone. The drone was equiped with 3 decks, the Multi-ranger, Qi 1.2 and Loco Positioning decks. 

The trajectories of the drone were randomly generated x, y, z coordinate points. These trajectories are saved in the .csv files in "Planned_trajectories" folder. All coordinates are in meters. The structure of the files is presented in the table below:

| x | y | z |
| :--: | :--: | :--:|
| x<sub>1</sub> | y<sub>1</sub> | z<sub>1</sub>  |
| x<sub>2</sub> | y<sub>2</sub>| z<sub>2</sub>  |
| ... | ... | ... |
| x<sub>n</sub> | y<sub>n</sub> | z<sub>n</sub>|

The real trajectories of the drones were approximated using the on board kalman filter. These x, y, z coordinate approximations (in meters), together with the battery voltage (in Volts) of the drone are found in the .csv files in the "Real_path" folder. The data was logged every 10 ms. The structure of the files is presented in the table below:

| x_estimate | y_estimate | z_estimate | battery_voltage |
| :--: | :--: | :--:| :--: |
| x_estimate<sub>1</sub> | y_estimate<sub>1</sub> | z_estimate<sub>1</sub>  | Vbat<sub>1</sub> |
| x_estimate<sub>2</sub> | y_estimate<sub>2</sub>| z_estimate<sub>2</sub>  | Vbat<sub>2</sub> |
| ... | ... | ... | ... |
| x_estimate<sub>n</sub> | y_estimate<sub>n</sub> | z_estimate<sub>n</sub>| Vbat<sub>n</sub>|


This dataset was used in order to create Machine Learning models to estimate how the drone's battery discharges based on the trajectory that it has to follow.


