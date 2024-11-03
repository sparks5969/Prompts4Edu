clear
set more off
cd "insert directory here"
capture log close
log using Loops.log, replace

/* ==============================================================================

Below is an example of how you can use a loop to run multiple regressions at once. 

You can use this code to replicate the coefficient in Panel A of Table 4 in one go
instead of running all of the regressions individually.

==============================================================================*/


use acting_wife_data_set, replace

/* 
Start by defining a list you want to iterate over. I named my list "variables".
In between the quotations are the different dependent variables that I want to
run regressions for, i.e. the thing I want to change each time the loop runs.
*/

local variables "salary travelmonth hours_desired tendtolead moreambitious competitive goodwriter"

foreach variable in `variables' {
reg `variable' public if male == 0 & maritalstatus ==0 , robust
}

/* 
The code above will run once for each dependent variables listed on line 24, 
giving you 7 different regressions.
*/
