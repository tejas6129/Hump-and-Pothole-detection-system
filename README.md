# Hump-and-Pothole-detection-system
Developed a system using deep learning algorithms to predict and evaluate potholes and humps. This also Incorporated sensor data readings from accelerometers to validate the predictions.

# Abstract
Hump and pothole detection is essential for ensuring road safety and preventing damage to vehicles. In recent years, there has been a growing interest in developing automated methods for hump and pothole detection. This paper presents the detection of humps and potholes using techniques of image processing, machine learning and sensorbased approach. The proposed method involves the use of cameras and sensors to collect data on road conditions, analyze the data and identify areas with humps or potholes. Machine learning algorithms are applied learn to recognize patterns in the data and make accurate predictions. The solution provided is robust with an accuracy of 90% approximately in achieving the objective under different lighting and weather conditions. The proposed solution is implemented in real time and tested for different conditions. The analysis is carried out in terms of improved road safety and reduced maintenance costs using the proposed solution. 

# Block diagram
![image](https://github.com/tejas6129/Hump-and-Pothole-detection-system/assets/127325785/8b595cf4-919e-4f9c-8c4a-e08a01b2a587)

A live frame is initially captured from the webcam and saved in a specific location on the device which is run further by the TensorFlow Lite model to detect the classes: 1) Pothole 2) Hump If a positive detection is found then a function embedded in another python script is run that collects data from a MPU6050 sensor interfaced with the Raspberry Pi. It checks for variation in Y axis coordinates of the prototype model developed for experimentation purposes. If a positive variation in the sensor readings is detected i.e. above the mean value for a flat surface then a Hump is confirmed, else if a negative variation from the mean value is detected then Pothole is confirmed and if there is no variation the function call is terminated after a specified duration. Upon a positive confirmation the geographical coordinates of the raspberry pi are published onto the terminal with the class detected. 

# Hardware Implementation 
## Front View of the Prototype 
![image](https://github.com/tejas6129/Hump-and-Pothole-detection-system/assets/127325785/e404162b-7848-47fd-9f0d-150ab45a2b1a)
![image](https://github.com/tejas6129/Hump-and-Pothole-detection-system/assets/127325785/7fa4fd01-da0c-4ee8-a4e2-a4361372038f)

# Flowchart
![image](https://github.com/tejas6129/Hump-and-Pothole-detection-system/assets/127325785/6518d57d-32b3-4a3c-b013-8af35c3935ce)

# Potholes detected for a Frame
![image](https://github.com/tejas6129/Hump-and-Pothole-detection-system/assets/127325785/dc6b637f-af13-41ea-bba9-b3e9fbbc1895)

# prototype crossing a Hump (Testing)
![image](https://github.com/tejas6129/Hump-and-Pothole-detection-system/assets/127325785/9965d971-684e-4ff9-96b9-3d7ac5971c7e)

# Latitude and Longitude Detection
We retrieve the location of the device from library called geopy.geocoders. which contains object called Nominatim. This is used to gather the latitude and longitude of the device after a successful detection by the ML model followed by sensor based verification algorithm. 

![image](https://github.com/tejas6129/Hump-and-Pothole-detection-system/assets/127325785/f3b7fd5d-ae14-4f88-aae4-0e89c6e644cd)

# Result and conclusion
The Custom Object detection TensorFlow Lite model has been implemented to detect hump and pothole classes from live images captured by the webcam on the Raspberry Pi 3 Also the Python script o evaluated the detection by checking variations in Gyroscope readings on the MPU6050 sensor has been verified for real world scenarios .Upon a positive detection by computer vision followed by positive verification from the sensor publishes the result class and latitude and longitude of the device on the output terminal. 
