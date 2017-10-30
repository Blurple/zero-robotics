# zero-robotics

//Declare any variables shared between functions here
float PositionAnalyzer[3];
int ifWeHaveAnalyzer;

void init(){
	//This function is called once when your code is first loaded.

	//IMPORTANT: make sure to set any variables that need an initial value.
	//Do not assume variables will be set to 0 automatically!
	PositionAnalyzer[0] = -0.3f;
	PositionAnalyzer[1] =  0.48f;
	PositionAnalyzer[2] = -0.16f;
	ifWeHaveAnalyzer = 0;
	
}


void loop(){
	//This function is called once per second.  Use it to control the satellite.
	 ifWeHaveAnalyzer = game.hasAnalyzer();
	
	if (ifWeHaveAnalyzer == 0) {
        	api.setPositionTarget (PositionAnalyzer);
	    DEBUG(("hello worlds"));
	}
	
}

