
A web controlled **Raspberry Pi ** robot with live video streaming.

## Main features
- Controlled via web browser.
- Live video streaming.

## DC motors direction issues

You may find that the motors are not moving in the direction you expected. If this happens, review the following line in **motors.py** and play with the LOW and HIGH parameters ;)

	def backward():
	        GPIO.output(Motor1A,GPIO.HIGH)
	        GPIO.output(Motor1B,GPIO.LOW)
	        GPIO.output(Motor2A,GPIO.HIGH)
	        GPIO.output(Motor2B,GPIO.LOW)
	
	def forward():
	        GPIO.output(Motor1A,GPIO.LOW)
	        GPIO.output(Motor1B,GPIO.HIGH)
	        GPIO.output(Motor2A,GPIO.LOW)
	        GPIO.output(Motor2B,GPIO.HIGH)
	
	def turnLeft():
	        print("Going Left")
	        GPIO.output(Motor1A,GPIO.HIGH)
	        GPIO.output(Motor1B,GPIO.LOW)
	        GPIO.output(Motor2A,GPIO.LOW)
	        GPIO.output(Motor2B,GPIO.HIGH)
	
	def turnRight():
	        print("Going Right")
	        GPIO.output(Motor1A,GPIO.LOW)
	        GPIO.output(Motor1B,GPIO.HIGH)
	        GPIO.output(Motor2A,GPIO.HIGH)
	        GPIO.output(Motor2B,GPIO.LOW)


## Web interface

Once the Raspberry Pi is up and running, connected to a wifi network and the L298N driver is powered by batteries, you should be able to control your robot by accessing **http://raspberry_ip:8000/**
