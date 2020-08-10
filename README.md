# Set python3 has default version
```
brew update && brew upgrade python
alias python=/usr/local/bin/python3
```
# Install dependencies
```
pip3 install -r requirements.txt
python 
```
# Run test
##  To read and write back out to video
```
python people_counter.py --prototxt mobilenet_ssd/MobileNetSSD_deploy.prototxt \
	--model mobilenet_ssd/MobileNetSSD_deploy.caffemodel --input videos/busy-road.mp4 \
	--output output/busy-road.avi
```
## To read from webcam and write back out to disk
```
python people_counter.py --prototxt mobilenet_ssd/MobileNetSSD_deploy.prototxt \
	--model mobilenet_ssd/MobileNetSSD_deploy.caffemodel \
	--output output/webcam_output.avi
```
# Reference 
https://www.chaj.com/post/176985543051/opencv-people-counter
