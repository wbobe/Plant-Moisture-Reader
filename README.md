# Plant-Moisture-Reader
Reads moisture level of soil in order to keep track of watering your plants.

Upload the GetMoistureLevel.ino sketch to an arduino (I use an UNO).
On a Raspberry Pi (Or any machine connected to the arduino via USB) run the python script named MoistureReader.py. (You will 
likely have to change the location of the serial connection to the arduino on the line that has "ser = 
serial.Serial('/dev/ttyACM1', 9600)" based on which USB port you use.

Each value read from the moisture sensor, and every 100 values will be averaged and written to a file with timestamps.

I've been graphing values on Google Sheets. The output file can be imported directly (just make sure you name it "*.txt") to a 
spreadsheet. Choose insert>graph and change the color of the timestamps to no color (otherwise it's impossible to read).

Maybe excel will do a better job of graphing and actually label the horizontal axis instead of spamming the entire graph with annotations but I'll have to look into that later.

I will update with more instructions for graphing and hopefully automation for that sort of thing and potentially automatic 
watering controls, as well as instructions for the wiring (with picture).
