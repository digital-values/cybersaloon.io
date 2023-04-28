---
title: "The 'Loadrr' Program"
date: 2023-04-14T17:36:13-04:00
draft: false
---

One of the biggest frustrations I had in my past life with a certain counter-drug agency was the fact that you were just expected to retrieve vast amounts of data and synthesize it in a timely manner with the commercial tools available. There were many inefficiencies that I vowed to change once I had the means and the freedom of movement to. I deployed and had some free time to develop a program to solve one unique problem I faced at DEA. It all originated with cell phone pings, the good guys would build enough probable cause to get a court order signed to server to a telephone provider for target cell phone pings both current and historical. 

We would then receive a generated report and would almost always include latitudes and longitudes. The issue was not being able to rapidly develop a common operating picture, some agencies had fancy tools and software that did a decent job. These tools were almost always centralized to one provider and would often not function as intended due to the high amounts of application usage.

If there's one thing I know for a fact, it's that most law enforcement folks want nitty gritty factual data points to accurately depict their target and their investigation. 'Loadrr' was developed in this manner: simple, no smoke and mirrors, and minimal technical expertise required. I promise you won't have to endure a 2 day 8hr class on how to use this tool.

So step one. You receive pings back from a service provider. Check. I've seen various formats and file types for subpoena returns, at minimum a service provider will give latitude and longitude. I am currently working on a method to scan coordinates in a given file type and return the coordinates in a double column csv file. For now unfortunately this is where we have to be hasty and dependent on the type of data we need to see first.

Traditionally cell phone pings will give a pattern of life of your given target. You can begin to associate addresses, areas, and familial addresses in order to begin understanding your subject in a more intimate way. Copy, paste, and format your coordinates as follows:

![Mock_csv](mock_csv.png)

I included mock longitude and latitude coordinates for educational purposes. Create a folder on your desktop with your newly created csv file inside. This part of the material is where we confirm or deny whether or not your agency will allow scripts to be ran locally... generally speaking - most agencies do not allow scripts to be ran locally. If this is the case for you, please email me and I will give you cloud access to this program (more on why that's not a standard later). If your agency is cool with you running scripts, buy your IT guy some coffee.

Okay. We have our cell phone pings in a csv file, we are ready to launch the program. Open up a command prompt, and chmod the script to allow execution. This would look like something like chmod 777 loadrr.py or (INSERT WINDOWS CMD FOR CHMOD AND FILE PATH), now this program relies on libraries only bundled with python version 3, so ensure you have python version 3 installed - cmd: python --version ... now that we verified our version of python we are ready to launch (very robust, I know) program. cmd: python3 loadrr.py, here's what you'll be greeted with:

![loaddr 1st prompt](loadrr-.png)

Friendly reminders are just that, friendly. Remember the data points statement? Well here is where we can develop our common operation picture by inputting an extra known data point outside of our cell phone pings. Sort of heat mapping, sort of pattern of life-ing, sort of just trying to make something out of nothing... government work, I know.

So when we give our target address the program is developed in a way that converts that address to a lat/long and plots in on our newly created kml file. This KML file is automatically saved in our directory with the csv and .py file. From this point we have a 2d common operating picture to brief. But that's no fun!

Load up google earth (preferably in an incongnito firefox browser) and open a new project > import KML file from computer > VOILA!

![Mock-kml-replaceME](mock-kml.png)

This is the end of my presentation, thank you for reading.