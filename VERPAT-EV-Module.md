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