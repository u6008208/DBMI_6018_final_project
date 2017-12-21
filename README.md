# DBMI_6018_final_project
STEWARSHIP-BASED SUSCEPTIBILITY REPORTS 


BACKGROUND:
Antimicrobial stewardship is a coordinated set of interventions designed to improve and mesure the appropriate use of antimicrobial agents (e.g. antibiotics, antifungals, antivirals, etc.) by promoting the selection of the optimal drug regimen. Antimicrobial stewardship is increasingly important due the rising rates of resistance to antimicrobials used to treat infections as well as the decreasing number of new antimicrobials in development. While there is increased recognition of the importance of antimicrobial stewardship, it is a relatively new concept so clinicians do not necessarily know how to make stewardship-minded decision in order to select the optimal drug regimen. A component of selecting the optimal drug regimen would include selecting the narrowest spectrum effective antimicrobial. Narrower spectrum antimicrobials are active or effective against fewer microorganisms but are preferred when they are active because they have fewer negative consquences (e.g. side effects, cost, antimicrobial-induced diarrhea highly-resistant subsequent infections) and preserve broader spectrum antibiotics for more difficult to treat or more resistant microorganisms. 

PURPOSE / RATIONALE: 
This program is intended to assist clinicians in selecting the narrowest spectrum agent based on a susceptibility report. Antimicrobial treatment is often split up into empiric and definitive therapy. Empiric therapy (the first 24-72 hours) usually begins by using a broader spectrum antimicrobial to cover the most likely pathogenic microorganism(s) because the causative microogranism is unknown initially. Cultures are taken from the likely site(s) of infection. Cultures take from 24-72 hours to return. Culture results are reported in a Susceptibility Report that informs clinicians of the causative microorganism and whether relevant antimicrobials are likely to be effective. Antimicrobials are classified as Suscpetibile (e.g. this antimicrobial is likely to be effective), Intermediate (this antimcirobial may be effective depending on the site of infection and antimicrobial concentrations at the site of infection), or Resistant (antimicrobial agent is not expected to be effective). An example susceptibility report is listed below. Definitive therapy is defined as the final selection of antimicrobial treamtent after the Susceptibility Report has returned. Ideally clinicians would select the narrowest spectrum active antimicrobial on a Susceptibility Report. However, clinicians do not always know what the narrowest spectrum agent is due to the lack of historical emphasis on making stewardship-minded decisions. Therefore, the goal of this project is to assist clinicians by creating Stewardship-Based Susceptibility Reports in place of the traditional Susceptibility Report. An example of a Stewardship-Based Susceptibility Report is below. It not only considers whether an antimicrobial is susceptibile or resistant but also factors in the spectrum of activity with preference to using the narrowest spectrum effective agent   



--------------------------------------EXAMPLE SUSCEPTIBILITY REPORT-----------------------------------------

	SPECIMEN / SOURCE: Blood 
	COLLECTED: 01/01/2000
	STATUS: FINAL (UPATED 01/04/2000) 
	
  	GRAM-STAIN: Gram-Negative Rod 
	CULTURE / ORGANISM: Morganella morgannii 
        
    
	ANTIBIOTIC SUSECPTIBILITY               
		Ampicillin......................R 
		Amipicillin-sulbactam...........R
		Piperacillin-tazobactam.........S  
		Cefazolin.......................R
		Ceftriaxone.....................S
		Cefepime........................S
		Ertapenem.......................S 
		Trimethoprim-sulfamethoxazole...S 
		Levofloxacin....................S

-----------------------------------EXAMPLE STEWARSHIP-BASED SUSCEPTIBILITY REPORT-----------------------------
    
	SPECIMEN / SOURCE: Blood 
	COLLECTED: 01/01/2000
	STATUS: FINAL (UPATED 01/04/2000)
        
	GRAM-STAIN: Gram-Negative Rod 
	CULTURE / ORGANISM: Morganella morgannii    
  
  
  	ANTIBIOTIC SUSCEPTIBILITY
	PREFERRED                                CONSIDER                       AVOID             
	Trimethoprim-sulfamethoxazole...S        Levofloxacin........S          Ampicillin................R
						 Ceftriaxone.........S          Amipicillin-sulbactam.....R
 		                                                                Piperacillin-tazobactam...S
										Cefazolin.................R                                                                                                             Cefepime..................S
										Ertapenem.................S
										
--------------------------------------------------------------------------------------------------------------
TECHNICAL DETAILS

The Stewardship-Based Susceptibility Report are built in a JupyterHub nobebook (the only platform I am familiar programming in). It requires no prior installation. Necessary modules are imported with the code. You will be promted to enter the password to connect to the to the necessary MySQL database. The program utilizes data from the MIMIC-II database. MIMIC-II is "an openly available dataset developed by the MIT Lab for Computational Physiology, comprising deidentified health data associated with ~40,000 critical care patients. It includes demographics, vital signs, laboratory tests, medications, and more." More information on MIMIC-II and its updated version MIMIC-II are available at https://mimic.physionet.org/ . Other than entering the required password to connect to the database, you will also be promted to select from a list of available susceptibility reports taken from the MIMIC-II database. Each cell can be evaluated individually or the entire notebook can be run at once. 

The input is a Susceptibility Report from the MIMIC-II database. The provided code classifies all antibitiotics in the database into a dictionary based on their spectrum of activity (Narrow, Moderate, Broad). The code modifies the Susceptibility Report into a Stewardship-Based Susceptibility Report using classes and for loops. The output is a Pandas Dataframe with columns representing the categories Preferred, Consider, and Avoid. Preferred includes the narrowest spectrum antibiotics that are active. The order of preference is Narrow > Moderate > Broad. 

--------------------------------------------------------------------------------------------------------------

MIT License

Copyright (c) [2017] [Jesse Sutton]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
