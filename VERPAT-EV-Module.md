.Starting from the [GreenSTEP EV module](https://github.com/gregorbj/GreenSTEP/blob/master/Documentation/GreenSTEP-RSPM_Documentation_20151220.docx).

Following steps are added/updated to incorporate electric vehicles and its impact. The ![](./VERPAT_images/checkmark.gif) before the variable name whether it exists in older version of RPAT.

- **Calculate Vehicle Ownership** : A number of vehicles are assigned to each household based on following model variables:
  1. **![](./VERPAT_images/checkmark.gif) Hhincttl**: total annual household income in dollars
  2. **![](./VERPAT_images/checkmark.gif) Htppopdn**: census tract population density in persons per square mile
  3. **![](./VERPAT_images/checkmark.gif) Transmilescap**: annual metropolitan transit revenue miles per person
  4. **![](./VERPAT_images/checkmark.gif) Urban**: dummy variable indicating whether household is in an urban mixed-use area
  5. **![](./VERPAT_images/checkmark.gif) Fwylnmicap**: metropolitan freeway lane miles per 1000 persons
  6. **![](./VERPAT_images/checkmark.gif) Onlyelderly**: dummy variable indicating whether all persons in the household are 65 years old or older
  7. **![](./VERPAT_images/checkmark.gif) DrvLevels**: dummy variable identifying driver population levels
  8. **![](./VERPAT_images/checkmark.gif) DrvAgePop**: number of driving age persons

  The **outputs** produced are:

  1. **Hhvehcnt**: number of vehicles in the household
  2. **VehPerDrvAgePop**: number of vehicles per driving age population in household

- **Predict Vehicle Type**: A vehicle type (*Auto* or *Light truck*) is assigned to each vehicle owned by households based on the following model variables:
  1. ![](./VERPAT_images/checkmark.gif) **Hhincttl**: total annual household income in dollars
  2. ![](./VERPAT_images/checkmark.gif) **Htppopdn**: census tract population density in persons  per square mile
  3. ![](./VERPAT_images/checkmark.gif) **Urban**: dummy variable indicating whether household is in an urban mixed-use area
  4. ![](./VERPAT_images/checkmark.gif) **Hhvehcnt**: number of vehicles in the household
  5. ![](./VERPAT_images/checkmark.gif) **Hhsize**: size of a household

  The **outputs** produced are:

  1. **VehType**: type of vehicle

- **Assign Vehicle Age**:  An age is assigned to each vehicle based on the following model variables:
  1. ![](./VERPAT_images/checkmark.gif) **IncGrp**: total annual household income in dollars
  2. ![](./VERPAT_images/checkmark.gif) **Hhvehcnt**: number of vehicles in the household
  3. ![](./VERPAT_images/checkmark.gif) **VehType**: type of vehicle

  The **outputs** produced are:

  1. **VehAge**: age of vehicle

- **Assign Initial Fuel Economy**: Assign fuel economy to each vehicle based on the following model variables:

  1. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **VehAge**: age of vehicle
  2. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Hhvehcnt**: number of vehicles in the household
  3. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **VehType**: type of vehicle

  The **outputs** produced are:

  1.  **VehMpg**: efficiency of a vehicle

- **Assign Vehicle Mileage Proportions**: Assign mileage proportion to each vehicle based on the following model variables:

  1. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Houseid**: ID of hosehold
  2. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Hhvehcnt**: number of vehicles in the household

  The **outputs** produced are:

  1.  **DvmtProp**: proportion of DVMT for each vehicle

- **Calculate Average DVMT**: DVMT is initially assigned to each household w/o adjusting for costs based on the following model variables:

  1. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) Hhincttl**: total annual household income in dollars
  2. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) Htppopdn**: census tract population density in persons per square mile
  3. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) Transmilescap**: annual metropolitan transit revenue miles per person
  4. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) Urban**: dummy variable indicating whether household is in an urban mixed-use area
  5. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) Fwylnmicap**: metropolitan freeway lane miles per 1000 persons
  6. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) DrvAgePop**: number of driving age person
  7. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Hhvehcnt**: number of vehicles in the household
  8. ![](./VERPAT_images/checkmark.gif) **Hhsize**: size of a household
  9. ![](./VERPAT_images/checkmark.gif) **Ageo0to14**: number of persons in the household with ages less than or equal 14
  10. ![](./VERPAT_images/checkmark.gif) **Ageo15to19**: number of persons between the ages of 15 and 19
  11. ![](./VERPAT_images/checkmark.gif) **Ageo20to29**: number of persons between the ages of 20 and 29
  12. ![](./VERPAT_images/checkmark.gif) **Ageo30to54**: number of persons between the ages of 30 and 54
  13. ![](./VERPAT_images/checkmark.gif) **Ageo55to64**: number of persons between the ages of 55 and 64
  14. ![](./VERPAT_images/checkmark.gif) **Ageo65Plus**: number of persons 65 or older
  15. ![](./VERPAT_images/checkmark.gif) **BaseCostPerMi**: base cost per mile in dollars
  16. ![](./VERPAT_images/checkmark.gif) **FutrCostPerMi**: future cost per mile in dollars

  The **outputs** produced are:

  1.  **Dvmt**: daily vehicle miles travelled by household

- **Assign Vehicle DVMT**: Assign mileage to each vehicle in the households.
  The **outputs** produced are:

  1. **VehDvmt**: daily vehicle miles travelled by vehicle

- **Identify HEVs and PHEVs**: Assign vehicle powertrains, mpg and mpkWh, and optimize travel between vehicles based on following model variables:

  1. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Houseid**: ID of hosehold
  2. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Hhvehcnt**: number of vehicles in the household
  3. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **VehType**: type of vehicle
  4. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **VehAge**: age of vehicle
  5. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **VehDvmt**: daily vehicle miles travelled
  6. :x: **Carshare**: indicator variable for car sharing household
  7. ❌ **DevType**: indicator variable for metropolitan development type
  8. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) Hhincttl**: total annual household income in dollars
  9. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) Htppopdn**: census tract population density in persons per square mile
  10. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Hhsize**: size of a household
  11. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Ageo0to14**: number of persons in the household with ages less than or equal 14
  12. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Ageo65Plus**: number of persons 65 or older
  13. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) Transmilescap**: annual metropolitan transit revenue miles per person
  14. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) Urban**: dummy variable indicating whether household is in an urban mixed-use area
  15. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) VehMpg**: efficiency of a vehicle

  The **outputs** produced are:

  1. **VehDvmt**: daily vehicle miles travelled by vehicle
  2. **DvmtProp**: proportion of DVMT for each vehicle
  3. **EvVehDvmt**: dvmt assigned to electric grid power of a vehicle
  4. **HcVehDvmt**: dvmt assigned to hydrocarbon power of a vehicle
  5. **VehMpg**: efficiency of vehicle attributed to hydrocarbon power
  6. **VehMpkwh**: efficiency of vehicle attributed to electric grid power
  7. **Powertrain**: power train of a vehicle

- **Identify EVs**: Identify electric vehicle based on following model variables:

  1. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Houseid**: ID of hosehold
  2. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Hhvehcnt**: number of vehicles in the household
  3. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **VehType**: type of vehicle
  4. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **VehAge**: age of vehicle
  5. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **VehDvmt**: daily vehicle miles travelled by vehicle
  6. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Dvmt95**: 95th percentile of daily vehicle miles travelled by household
  7. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **DvmtProp**: proportion of DVMT for each vehicle
  8. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) Powertrain**: power train of a vehicle
  9. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) VehMpg**: efficiency of a vehicle
  10. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif)** **VehMpkwh**: efficiency of vehicle attributed to electric grid power
  11. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **EvVehDvmt**: dvmt assigned to electric grid power of a vehicle
  12. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **HcVehDvmt**: dvmt assigned to hydrocarbon power of a vehicle

  The **outputs** produced are:

  1. **EvVehDvmt**: dvmt assigned to electric grid power of a vehicle
  2. **HcVehDvmt**: dvmt assigned to hydrocarbon power of a vehicle
  3. **VehMpg**: efficiency of vehicle attributed to hydrocarbon power
  4. **VehMpkwh**: efficiency of vehicle attributed to electric grid power
  5. **Powertrain**: power train of a vehicle

- **Calculate Average Fuel CO2e per gallon**: Calculate unit emissions for fuel. Requires following input files with respective fields:

  - *fuel_co2.csv*:
    1. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **ULSD**
    2. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Biodiesel**
    3. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **RFG**
    4. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **CARBOB**
    5. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Ethanol**
    6. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Cng**
    7. :x: **HhVehComposite**
    8. :x: **CommVehComposite**

  - *fuel.csv*:
    1. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **PropDiesel**
    2. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **PropCng**
    3. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **GasPropEth**
    4. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **DieselPropBio**

    The **outputs** produced are:

    1. **AveFuelCo2e.**: Average fuel CO2e per gallon

- **Calculate Average electricity CO2e per Kwh**: Calculate unit emissions for electricity. Requires following input files with respective fields:

  - ❌ *power_co2.csv*: Carbon intensity inputs for electricity for a selection of **counties** and **year**
    1. ❌ **County**
    2. ❌ **Year**
    3. ❌ **Intensity**

    The **outputs** produced are:

    1. **AveElectricCo2e.Co.**: Average electricity CO2e per gallon

- **Calculate fuel consumption and CO2e production**: Calculate fuel consumption and CO2e production for each household based on following model variables:

  1. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Hhvehcnt**: number of vehicles in the household
  2. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **HcVehDvmt**: dvmt assigned to hydrocarbon power of a vehicle
  3. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) VehMpg**: efficiency of a vehicle
  4. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **VehType**: type of vehicle
  5. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **EvVehDvmt**: dvmt assigned to electric grid power of a vehicle
  6. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif)** **VehMpkwh**: efficiency of vehicle attributed to electric grid power
  7. ![](./VERPAT_images/checkmark.gif) **Dvmt**: daily vehicle miles travelled by household
  8. ![](./VERPAT_images/checkmark.gif) **AveFuelCo2e.**: Average fuel CO2e per gallon
  9. **![](./VERPAT_images/checkmark.gif) AveElectricCo2e.Co.**: Average electricity CO2e per gallon

  The **outputs** produced are:

  1. **FuelGallons**: amount of fuel consumed by each household
  2. **FuelCo2e**: amount of CO2e emission per day by each household from fuel consumption
  3. **ElecKwh**: amount of electricity power consumed by each household
  4. **ElecCo2e**: amount of CO2e emission per day by each household from electricity power consumption

- **Calculate all household costs**: Calculate total costs for all households based on following model variables:

  1. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **FuelGallons**: amount of fuel consumed by each household
  2. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **FuelCo2e**: amount of CO2e emission per day by each household from fuel consumption
  3. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) ElecKwh**: amount of electricity power consumed by each household
  4. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **ElecCo2e**: amount of CO2e emission per day by each household from electricity power consumption
  5. ![](./VERPAT_images/checkmark.gif) **Dvmt**: daily vehicle miles travelled by household
  6. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif)** **DailyPkgCost**: daily parking cost for each household
  7. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Hhvehcnt**: number of vehicles in the household
  8. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **HcVehDvmt**: dvmt assigned to hydrocarbon power of a vehicle
  9. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **EvVehDvmt**: dvmt assigned to electric grid power of a vehicle
  10. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) Hhincttl**: total annual household income in dollars
  11. ❌ **DevType**: indicator variable for metropolitan development type
  12. ❌ **Payd**: pay as you drive insurance
  13. ❌ **DepExp**: vehicle depreciation expense for each household
  14. ❌ **CongPrice**: 
  15. ❌ **VmtSurcharge**:
  16. ❌ **ExtraModCost**:

  The **outputs** produced are:

  1. **FutrCostPerMi**: 
  2. **TotExtCost**: 
  3. **HhTotCost**: 
  4. **VehOwnExp**: 

- **Recalculate DVMT adjusted to new costs**: Calculate DVMT with new costs and reallocate to vehicles based on following model variables:

  1. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Hhincttl**: total annual household income in dollars
  2. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **CashoOutIncAdj**: 
  3. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) Htppopdn**: census tract population density in persons per square mile
  4. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Hhvehcnt**: number of vehicles in the household
  5. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Tranmilescap**: transit miles capacity
  6. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif)** **Fwylnmicap**: freeway lane miles capacity
  7. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **DrvAgePop**: driving age population for each household
  8. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Hhsize**: size of each household
  9. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Ageo0to14**: number of persons in the household with ages less than or equal 14
  10. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Ageo15to19**: number of persons between the ages of 15 and 19
  11. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Ageo20to29**: number of persons between the ages of 20 and 29
  12. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Ageo30to54**: number of persons between the ages of 30 and 54
  13. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Ageo55to64**: number of persons between the ages of 55 and 64
  14. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Ageo65Plus**: number of persons 65 or older
  15. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) Urban**: dummy variable indicating whether household is in an urban mixed-use area
  16. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) BaseCostPerMi**: base cost per mile
  17. **![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) FutrCostPerMi**: future cost per mile

  The **outputs** produced are:

  1. **Dvmt**: daily vehicle miles travelled by household

- **Calculate Congestion Effects**: Calculate congestion effects based on following model variables:

  1. :x: **CongModel_**: A list of models and dataset to calculate congestion effect.
  2. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Dvmt.Ty**: Dvmt by vehicle type
  3. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **PerCapFwy**: freeway percenatge per capita
  4. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **PerCapArt**: arterial percentage per capita
  5. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Pop**: Current year population
  6. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **BasePop**: Base year population
  7. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **FwyArtProp**: Freeway and arterial proportion
  8. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **BusVmtSplit.Fc**: bus vmt split by functional class
  9. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **TruckVmtSplit.Fc**: truck vmt split by functional class
  10. :x: **OpsDeployParm_Va.MaYr**: traffic operations program deployment levels
  11. :x: **SmoothEcoDriveParm_Va**: :question:
  12. :x: **OtherOps_Yr.LvTy**: :question:
  13. :x: **CongPrice.ClFc**: :question:
  14. :x: **CongEfficiency.YrPt**: :question:
  15. :x: **ValueOfTime**: :question:

  The **outputs** produced are:

  1. **MpgMpkwhAdj.MaPt**: Mpg/MpKwH adjsutment by vehicle type
  2. **VehHr.MaTy**: vehicle travel time
  3. **AveSpeed.MaTy**: average speed travelled
  4. **FfVehHr.MaTy**: free flow vehicle travel time
  5. **DelayVehHr.MaTy**: delay in vehicle travel time