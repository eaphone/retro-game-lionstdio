# Table of contents
- [Eletronic component](#ec)
- [Manufacture](#manufacture)
- [Building](#building)
- [Flashing](#flashing)

# Eletronic component
- main ecs are specified at BOMxx.xlsx for  s3/p4
- 10* round Snap dome 5mm (100g pressure is recommand)
- 1* 303759-750mah battery (30mm thin, 37*59mm size)

# Manufacture
JLC pcb service. parameter:\
1mm thiness, 2 layers

# Building
## environment
recommand Ubuntu + esp-idf 5.5.4

## build
source {path to esp-idf}/export.sh
### esp32s3
python rg_tool.py --target esp32-s3-devkit build-img 
### esp32p4
python rg_tool.py --target esp32-s3-devkit build-img --no-networking

# Flashing
- force device into download mode
1. power off the device
2. pull down the download pin (for esp32s3, press A; for esp32p4 press Up)
3. pwoer on the device
4. release the download pin
