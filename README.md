# EV Population Classification

- Dataset from https://data.wa.gov/Transportation/Electric-Vehicle-Population-Data/f6w7-q2d2/about_data
- Kaggle link: https://www.kaggle.com/datasets/usamabuttar/electric-vehicle-population-data-washington-us
- Encoding Methods: https://medium.com/@jkkn.iitkgp/categorical-data-encoding-techniques-d6296697a40f

# WAEV

Notes (About the Dataset)

This dataset shows the Battery Electric Vehicles (BEVs) and Plug-in Hybrid Electric Vehicles (PHEVs) that are currently registered through Washington State Department of Licensing (DOL).

1. A Battery Electric Vehicle (BEV) is an all-electric vehicle using one or more batteries to store the electrical energy that powers the motor and is charged by plugging the vehicle in to an electric power source. A Plug-in Hybrid Electric Vehicle (PHEV) is a vehicle that uses one or more batteries to power an electric motor; uses another fuel, such as gasoline or diesel, to power an internal combustion engine or other propulsion source; and is charged by plugging the vehicle in to an electric power source.

2. Clean Alternative Fuel Vehicle (CAFV) Eligibility is based on the fuel requirement and electric-only range requirement as outlined in RCW 82.08.809 and RCW 82.12.809 to be eligible for Alternative Fuel Vehicles retail sales and Washington State use tax exemptions. Sales or leases of these vehicles must occur on or after 8/1/2019 and meet the purchase price requirements to be eligible for Alternative Fuel Vehicles retail sales and Washington State use tax exemptions.
3. Monthly count of vehicles for a county may change from this report and prior reports. Processes were implemented to more accurately assign county at the time of registration.
4.  Electric Range is no longer maintained for Battery Electric Vehicles (BEV) because new BEVs have an electric range of 30 miles or more. Zero (0) will be entered where the electric range has not been researched.

# Columns in the dataset

- Vin#: The 1st 10 characters of each vehicle's Vehicle Identification Number (VIN).
- County: This is the geographic region of a state that a vehicle's owner is listed to reside within. Vehicles registered in Washington state may be located in other states.
- City: The city in which the registered owner resides.
- State: This is the geographic region of the country associated with the record. These addresses may be located in other states.
- Zip: The 5 digit zip code in which the registered owner resides.
- Model Yr: The model year of the vehicle, determined by decoding the Vehicle Identification Number (VIN).
- EV Type: This distinguishes the vehicle as all electric or a plug-in hybrid.
- CAFV Eligibility: This categorizes vehicle as Clean Alternative Fuel Vehicles (CAFVs) based on the fuel requirement and electric-only range requirement in House Bill 2042 as passed in the 2019 legislative session.
- Electric Range: Describes how far a vehicle can travel purely on its electric charge.
- MSRP: This is the lowest Manufacturer's Suggested Retail Price (MSRP) for any trim level of the model in question.
- Leg Dist: The specific section of Washington State that the vehicle's owner resides in, as represented in the state legislature.
- DOL ID: Unique number assigned to each vehicle by Department of Licensing for identification purposes.
- Vehicle Location: The center of the ZIP Code for the registered vehicle.
- Electric Utility: This is the electric power retail service territories serving the address of the registered vehicle. All ownership types for areas in Washington are included: federal, investor owned, municipal, political subdivision, and cooperative. If the address for the registered vehicle falls into an area with overlapping electric power retail service territories then a single pipe | delimits utilities of same TYPE and a double pipe || delimits utilities of different types. We combined vehicle address and Homeland Infrastructure Foundation Level Database (HIFLD) (https://gii.dhs.gov/HIFLD) Retail_Service_Territories feature layer using a geographic information system to assign values for this field. Blanks occur for vehicles with addresses outside of Washington or for addresses falling into areas in Washington not containing a mapped electric power retail service territory in the source data.
- 2020 Census Tract: The census tract identifier is a combination of the state, county, and census tract codes as assigned by the United States Census Bureau in the 2020 census, also known as Geographic Identifier (GEOID). More information can be found here: https://www.census.gov/programs-surveys/geography/about/glossary.html#par_textimage_13 https://www.census.gov/programs-surveys/geography/guidance/geo-identifiers.html