Chinese version available at `README_CN.md`
# TailTip
TailTip is an opensource device with bioelectricity ΣΔ AFE and IMU, supports BLE5.2.
Designed for sEMG collection and motion detection.
In other word, it can be used as or a part of the project's intended usage is o**asm detection/prediction and edging.
Inspired by the pressure-detection prediction, TailTip detects the motion of pelvic floor muscle, and calculate it into a score.
DG-LAB Coyote Protocol support is currently WIP.
# Usage
There are 3 channels in TailTip: ch1, ch2, rld. With 2.5mm TRS connector, definition below:
| Channel | Sleeve | Ring | Tip |
| --- | --- | --- | --- |
| Ch1 | GND | - | + |
| Ch2 | GND | - | + |
| Rld | GND | / | + |

TS(same as coyote3.0) is not compatible since the GND and in- will be shorted and it dont contains a GND shield. But you may use two TS lines, two electrode both connect to Tip/IN+ and do "CH=Ch1-Ch2" through it's not offically support. 
The rld electrode significantly increase signal quality, so its strongly recommand.
One Chx is used as main collection with two electrode located as perineum, and the other is optional for auxiliary.
If only one channel is needed, ADS1291 may work to reduce cost.
A shielding layer of cable is recommanded and connect to GND with single-ended.
(developing)If used with Coyote or other similar device, please route a branch of device output waveform to application, (in future versions)or through precision resistance voltage divider and buffer, it can directly connect to H1/Other Chx of Tailtip.

Firmware is under development and the operation is WIP.