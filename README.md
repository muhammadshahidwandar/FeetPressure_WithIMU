# Inferring Feet Pressures with Lower Limbs IMUs (DATASET)

The prediction of foot pressure using IMU sensors is an active area of research aimed at minimizing hardware, cost, and 
logistics while enhancing the degree of freedom for Internet of Medical Things (IoMT) in health assessment and monitoring 
of post-stroke rehabilitation patients.

This dataset is collected from eight real hospital patients undergoing post-stroke rehabilitation at various stages. 
The data is gathered by an expert physiotherapist during therapy sessions while the patients wear SMARTPant[1], a platform
that includes four IMU sensor nodes placed on the lower limbs, along with two pressure-sensing insoles, each equipped with
four piezoelectric pressure-sensing nodes deployed at four key points on the foot, as shown in Figure 1.


![Alt text](SmartPant.png)
<sub> Image was adapted from [1] 
https://ieeexplore.ieee.org/abstract/document/8938180 </sub>

##Particular aspects of dataset are:

* [ ] It is composed of panelists with different nationalities (British, Dutch, French, German, Italian, American, Mexican, Columbian, Thai). This aspect allows studying the effect of ethnic origin variety to the automatic VAD.
* [ ]	There is a gender balance such that there are four female and five male panelists.
* [ ]	The panelists are sitting in two rows and they can be gazing audience, other panelists, their laptop, the moderator or anywhere in the room while speaking or not-speaking. Therefore, they were captured not only from frontal-view but also from side-view varying based on their instant posture and head orientation.
* [ ] The panelists are moving freely and are doing various spontaneous actions (e.g., drinking water, checking their cell phone, using their laptop, etc.), resulting in different postures. 
* [ ] The panelists’ body parts are sometimes partially occluded by their/other's body part or belongings (e.g., laptop).
* [ ] There are also natural changes of illumination and shadow rising on the wall behind the panelists in the back row.
* [ ] Especially, for the panelists sitting in the front row, there is sometimes background motion occurring when the person(s) behind them moves.

You can reach the annotations from [HERE](http://doi.org/10.5281/zenodo.3928151) that includes:

* [ ] The upper body detection of nine panelists in bounding box form
* [ ] Associated VAD ground-truth (speaking, not-speaking) for nine panelists 
* [ ] Acoustic features extracted from the video: MFCC and raw filterbank energies
* [ ] The corresponding video can be accessed from [HERE](https://www.youtube.com/watch?v=51pRTOIso4U)

# 3. Dataset Details

##Directory structure 

## Files List for each exercise

## Data structure in each file

Each record in the generated csv file is in the form of:
```
gnss_ts_ns, ecef_px, ecef_py, ecef_pz, enu_vx, enu_vy, enu_vz, fix_type, valid_fix, diff_soln, carr_soln
```
, with each item described in the following:
| name | description | 
| :--: | :---------: |
| gnss_ts_ns | GNSS time of the navigation epoch (expressed as Unix timestamp in ns) |
| ecef_p* | The x, y, z component of the position in ECEF frame |
| enu_v* | The x, y, z component of the velocity in ENU frame |
| fix_type | GNSS fix type (0=no fix, 1=dead reckoning only, 2=2D-fix, 3=3D-fix, 4=GNSS+dead reckoning combined, 5=time only fix) |
| valid_fix | if fix valid (1=valid fix) |
| diff_soln | if differential correction were applied (1=applied) |
| carr_soln | carrier phase range solution status (0=no carrier phase, 1=float, 2=fix) | 

## 5. License
The dataset is released under [CC-BY-NC-SA-4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) license.

## When using this dataset for your research, please cite the related papers in your publication:
```
C. Beyan, M. Shahid and V. Murino, 
"RealVAD: A Real-world Dataset and A Method for Voice Activity Detection by Body Motion Analysis," 
in IEEE Transactions on Multimedia, doi: 10.1109/TMM.2020.3007350.
```
```
@ARTICLE{Beyan2020TMM,
  author={C. {Beyan} and M. {Shahid} and V. {Murino}},
  journal={IEEE Transactions on Multimedia}, 
  title={RealVAD: A Real-world Dataset and A Method for Voice Activity Detection by Body Motion Analysis}, 
  year={2020},
  volume={},
  number={},
  pages={1-1},}
```
