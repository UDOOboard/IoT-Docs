In this section you can find examples of how to create an application that change the `data` file values.

Remember that the application must have the permission to write on the `data` file.

## Python

```python
from time import sleep # to add delays

import string
import time
import os
import sys
import math

# virtualSensorName = '__NAME_OF_THE_SENSOR__'
virtualSensorName = 'vstest'

status = 0

#This method change the value in data file
def printVS( data ):
	global status
	data = str(data).strip()		
	print data
	dataIot = open(directory + file, "w")
	dataIot.write(str(status) + ',' + data)
	dataIot.flush()
	dataIot.close()
	if status == 0 :
		status = 1
	elif status == 1:
		status = 0

# Open the output data file
file = 'data'
directory = '/sensors/'+ virtualSensorName +'/'
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
		printVS(presence)

```
