In this section you can find examples of how to create an application that change the `data` file values of a Virtual Sensor.

Remember that the application must have the permission to write on the `data` file.

## Python

This python write on the `data` file of the `vstest` Virtual Sensor a string of the data every 5 seconds

```python
import time
import os

# virtualSensorName = '__NAME_OF_THE_SENSOR__'
virtualSensorName = 'vstest'

#This method change the value in data file
def printVS( data ):
	print data
	dataIot = open(directory + file, "w")
	dataIot.write(data)
	dataIot.flush()
	dataIot.close()

# Open the output data file
file = 'data'
directory = '/sensors/virtual/'+ virtualSensorName +'/'
print 'Checking directory exists ...'
if not os.path.exists(directory):
	print 'Directory does not exists... creating... '
	try:
		os.makedirs(directory)
		print 'OK'
	except OSError as e:
		print 'NO \n ERROR:' + e
		exit()
else:
	print 'OK'


while True: # Run forever
		#MAKE CALCULATIONS
		printVS(time.strftime("%c"))
		time.sleep(5)

```
