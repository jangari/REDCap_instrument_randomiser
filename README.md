# REDCap Instrument Randomisation Code Generator

By Aidan Wilson\
aidan.wilson@intersect.org.au\
[@aidan.wilson](https://community.projectredcap.org/users/3510/aidanwilson.html)\
[jangari](https://github.com/jangari)


This tool allows you to construct the otherwise impenetrable conditional logic to be inputted into the survey queue configuration in order to present N surveys to respondents in a random order.

Populate the variables below and execute this program in Python or a Jupyter Notebook to generate the code needed for the survey queue.

*instruments*\
Populate this list with the unique form names of the instruments that need to be randomised.

*initialSurvey*\
Unique form name of the instrument that is completed before randomised instruments begin. This is also where [rand] would be set.

*exitSurvey*\
Unique form name of the instrument that all respondents are sent to upon completion. Leave as empty string if not needed.

*sequences*\
How many random sequences to generate?

*seqlength*\
Length of each sequence. Leave as 0 to randomise all instruments.

*rand*\
Name of random value field, this will be a calculated field with something like Math.random()*N (where N is the number of random sequences to use), or the modulo of the [record_id] field by N.
