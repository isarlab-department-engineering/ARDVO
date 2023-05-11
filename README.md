# ARD-VO: Agricultural Robot Dataset of Vineyards and Olive groves


***10, Mar 2021 update***</br> 
- REPOSITORY UNDER CONSTRUCTION we are uploading and building the github repo.  </br></br></br>

Real-world extensive set of data to support the development of solutions and algorithms for precision farming technologies in the aforementioned crops. ARD-VO has been collected with an
Unmanned Ground Vehicle (UGV) equipped with different heterogeneous sensors
that capture information essential for robot localization and plant monitoring tasks.
It is composed of sequences gathered in 11 experimental sessions between August
and October 2021, navigating the UGV for several kilometers in four cultivation
fields in Umbria, a central region of Italy: (a)-(b) vineyards, (c)-(d) olive crops


<img src="imgs/cultivs.png" alt="Vineyard an Olive Crops used to gather data" width="900x"/> <br/>


| Alias name |         Crop Variety          |     lat(N) , lon(E)      | # Sessions |               Date: dd, mm, yyyy                |
|:----------:|:-----------------------------:|:------------------------:|:----------:|:-----------------------------------------------:|
|  Vynrd A   |       Grechetto Todi G5       |   43.004491, 12.294889   |     1      |                3, September 2021                |
|  Vynrd B   |       Grechetto Todi G5       |   42.812355, 12.418741   |     2      |     4, August 2021  </br> 1, September 2021     |
|  OlvCs A   |           Moraiolo            |   42.967206, 12.407057   |     4      | 14-23-30, September 2021 </br> 13, October 2021 |
|  OlvCs B   | Moraiolo, Leccino, Frantoiano |   42.961702, 12.412744   |     4      | 14-23-30, September 2021 </br> 13, October 2021 |

## 1. License
ARD-VO is released undeR the following License:

Attribution-NonCommercial-ShareAlike 3.0 [CC BY-NC-SA 3.0](LICENSE).

This means it is possible:
* to copy, distribute, display, and perform the work. 
* to make derivative works.

Under the following conditions:</br>
 - Attribution: You must give the original author credit.</br>
 - Non-Commercial — You may not use this work for commercial purposes. </br>
 - Share Alike — If you alter, transform, or build upon this work, you may distribute the resulting work only under a licence identical to this one.

**If you use ARD-VO in an academic work, please cite:**

    @article{crocetti2023ard,
      title={ARD-VO: Agricultural robot data set of vineyards and olive groves},
      author={Crocetti, Francesco and Bellocchio, Enrico and Dionigi, Alberto and Felicioni, Simone and Costante, Gabriele and Fravolini, Mario L and Valigi, Paolo},
      journal={Journal of Field Robotics},
      year={2023},
      publisher={Wiley Online Library}
    }

## 2. Agrobot - The robotic platform

We collected a dataset with a robotic platform so-called "Agrobot". In the following the body specs and the sensors equipments 
of the robotic platform. 

### Body Specs



<table>
  <tr>
    <th colspan="4">Robot Body Measurements</th>
  </tr>
  <tr>
    <th rowspan="4" style="align-items: center"><img src="imgs/Agrobot_body.png" alt="Agrobot - Body measurements" width="280px"/> <br/></th>
  </tr>
  <tr>
    <td>𝑎 1.30 [𝑚]</td>
    <td>𝑏 0.77 [𝑚]</td>
    <td>𝑐 0.80 [𝑚]</td>
  </tr>
  <tr>
    <td>𝑑 0.20 [𝑚]</td>
    <td>𝑒 0.77 [𝑚]</td>
    <td>𝑓 0.74 [𝑚]</td>
  </tr>
  <tr>
    <td>𝑔 ≈ 0.24 [𝑚]</td>
    <td colspan="2">weight ≈ 700 [𝐾𝑔]</td>
  </tr>
  <tr>
    <th colspan="4">Tyres</th>
  </tr>
  <tr>
    <td colspan="4">Genial Tyre Agri Line 6.5∕80 𝑅13</td>
  </tr>
</table>

### Sensors, Equipments and connection overview
<table>
  <tr>
    <th><img src="imgs/Agrobot_overview_sens.jpg" alt="Agrobot - Sensors displacement" height="350x"/> </th>
    <th><img src="imgs/Agrobot_modules.png" alt="Agrobot - Sensors connection" height="350x"/> </th>
  </tr>

  <tr>
    <td colspan="2"> <b>Multispectral Camera:</b>  <a href="https://support.micasense.com/hc/en-us/articles/360011389334-RedEdge-MX-Integration-Guide">RedEdge MX camera</a>. </td>
  </tr>

 <tr>
    <td colspan="2"> <b>360° LIDAR:</b>  <a href="https://velodynelidar.com/products/puck-lite/">Velodyne Puck Lite</a>. </td>
 </tr>

 <tr>
    <td colspan="2"> <b>Inertial and Position measurement units:</b>  <a href="https://www.swiftnav.com/duro-inertial">Swift Duro Inertial</a>. </td>
 </tr>

 <tr>
    <td rowspan="2"> <b>Front camera rig (two units, left and right) </b>   </td>
    <td>Camera Module:  <a href="https://www.flir.com/products/blackfly-s-gige/?vertical=machine+vision&segment=iis">Blackfly S BFS-PGE-04S2C-C</a> </td>
 </tr>

 <tr>
    <td>Lens  <a href="https://www.machine-vision-shop.com/all-products/lenses/fifo-0420mm">FIFO-0420MM C-mount</a> </td>
 </tr>

 <tr>
    <td colspan="2"> <b>DC Brushless Motor Inverters:</b> Roboteq HBL2360a </td>
 </tr>

 <tr>
    <td colspan="2"> <b>X90 mobile controller:</b> <a href="https://www.br-automation.com/en/products/plc-systems/x90-mobile-control-system/">X90 mobile control system</a> </td>
 </tr>

<tr>
    <td colspan="2"> <b>Main computer:</b> Intel i7-9700E CPU with an NVIDIA GeForce RTX 2060. Two SO-DIMM slots
equip 32GB of DDR4 2666 MHz RAM. We decided to install
two different storage systems: one PCI Express x4 NVMe
1.3, 256GB for the operating system (Ubuntu 20.04 LTS 64
bit) and two SATA SSD 2.5", 2TB disks for data. </td>
 </tr>

 <tr>
    <td colspan="2"> <b>Ethernet switch:</b> Oring TGXPS-1080-M12-24V Series </td> </tr>
</table>

## 3. Dataset

For each session, two sets of data are available: the first is made using the sensors connected
to the onboard computer, and the second only with the multispectral camera, whose streams are independently geotagged
by using the GPS of the RedEdge Micasese kit. 

### ROSBAG for onboard devices recorded data.

We used **[ROS Noetic](http://wiki.ros.org/noetic)** to handle the data
related to the devices directly connected to the onboard unit, while the multispectral images are stored directly on the SSD
memory of the RedEdge camera. Since the duration of the sessions may vary between one and two hours, each one is split
into a number of shorter sequences. </br>

The rosbag package allows recording these topics and
messages in a unique file that can be executed in batches to
reproduce the experiment. The following table reports a description of the
collected data, the message types, and the topics available in
this dataset.

<table>
  <tr>
    <th> Topic </th>
    <th> Message Type </th>
    <th> Description </th>
  </tr>
  <tr>
    <td><i>/flir_adk/front/left/image_raw</i> </br>/flir_adk/front/right/image_raw </td>
    <td> sensor_msgs/Image</td>
    <td> Raw images from the frontal FLIR cameras.</td>
  </tr>
  <tr>
    <td><i>/gps/duro/current_pose</i></td>
    <td> geometry_msgs/PoseStamped</td>
    <td> (𝑥, 𝑦, 𝑧) metric position and orientation (quaternion)</td>
  </tr>

  <tr>
    <td><i>/gps/duro/fix</i></td>
    <td> sensor_msgs/NavSatFix</td>
    <td> GPS lat/long with variance.</td>
  </tr>

  <tr>
    <td><i>/gps/duro/imu</i></td>
    <td> sensor_msgs/Imu</td>
    <td> Angular velocity and acceleration about (𝑥, 𝑦, 𝑧) axes.</td>
  </tr>

  <tr>
    <td><i>/gps/duro/odom</i></td>
    <td>nav_msgs/Odometry</td>
    <td> Estimates of position and velocity with the respect to the reference frame.</td>
  </tr>

  <tr>
    <td><i>/gps/duro/rollpitchyaw</i></td>
    <td>geometry_msgs/Vector3</td>
    <td> Orientation.</td>
  </tr>

  <tr>
    <td><i>/velodyne_points</i></td>
    <td>sensor_msgs/PointCloud2</td>
    <td>Velodyne laser scanned points transformed in the original frame of reference.</td>
  </tr>

  <tr>
    <td><i>/agrobot/Inverter/HBL2360A_L</i> </br><i>/agrobot/Inverter/HBL2360A_R</i> </td>
    <td> diagnostic_msgs/DiagnosticArray</td>
    <td> Diagnostic messages from the Inverters.</td>
  </tr>
</table>

### Extracted data examples

#### RGB AND LIDAR
In the following, as en example some RGB images and laser scans extracted from ARD-VO dataset.</br>
The first two rows contain the RGB images collected by the left (a-f) and the right (g-l) cameras, respectively. </br>
The third row includes examples of laser scans. The first three columns (a-c, g-i, m-o) contain samples from the sequences gathered
in the olive crops (OlvCS-A,B), while the latter three (d-f, j-l, p-r) from those collected in the vineyards (Vynrd-A,B).

<img src="imgs/camera_laser_example.png" alt="Vineyard an Olive Crops used to gather data" width="900px"/> <br/><br/>

#### INVERTERS 
The topics related to the inverters contain useful diagnostic data and flags provided from the inverters. 
Some flags are coded according to the manufacturer (Roboteq) specs. To further use them you need to download the inverter manual already
provided in the previous table.
Each inverter has two channels (CH1,CH2) that are used to drive the front and rear wheels of each side (Left and Right) of the robot.
The gathered data also include RPM of the motors and the power consumption.  

<img src="imgs/inverters_example.png" alt="Vineyard an Olive Crops used to gather data" width="900px"/> <br/>

**Note:** Each wheel is connected with a kinematic chain of 80:1 transmission ratio to a 2 kW three-phase brushless BLCD motor that can reach
4300 rpm and 4.6 Nm torque.</br>

#### DURO IMU AND GPS-RTK

<img src="imgs/imu_example.png" alt="Vineyard an Olive Crops used to gather data" width="900px"/> <br/>
