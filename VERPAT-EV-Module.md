.Starting from the [GreenSTEP EV module](https://github.com/gregorbj/GreenSTEP/blob/master/Documentation/GreenSTEP-RSPM_Documentation_20151220.docx).

Following steps are added/updated to incorporate electric vehicles and its impact. The ![](./VERPAT_images/checkmark.gif) before the variable name whether it exists in older version of RPAT.

- **Calculate Vehicle Ownership** : A number of vehicles are assigned to each household based on following model variables:
  1. **![](./VERPAT_images/checkmark.gif) Hhincttl**: total annual household income in dollars
  2. **![](./VERPAT_images/checkmark.gif) Htppopdn**: census tract population density in persons per
     square mile
  3. **![](./VERPAT_images/checkmark.gif) Transmilescap**: annual metropolitan transit revenue miles per
     person
  4. **![](./VERPAT_images/checkmark.gif) Urban**: dummy variable indicating whether household is
     in an urban mixed-use area
  5. **![](./VERPAT_images/checkmark.gif) Fwylnmicap**: metropolitan freeway lane miles per 1000 persons
  6. **![](./VERPAT_images/checkmark.gif) Onlyelderly**: dummy variable indicating whether all persons in
     the household are 65 years old or older
  7. **![](./VERPAT_images/checkmark.gif) DrvLevels**: dummy variable identifying driver population levels
  8. **![](./VERPAT_images/checkmark.gif) DrvAgePop**: number of driving age person
- **Predict Vehicle Type**: A vehicle type (*Auto* or *Light truck*) is assigned to each vehicle owned by households based on the following model variables:
  1. ![](./VERPAT_images/checkmark.gif) **Hhincttl**: total annual household income in dollars
  2. ![](./VERPAT_images/checkmark.gif) **Htppopdn**: census tract population density in persons per
     square mile
  3. ![](./VERPAT_images/checkmark.gif) **Urban**: dummy variable indicating whether household is
     in an urban mixed-use area
  4. ![](./VERPAT_images/checkmark.gif) **Hhvehcnt**: number of vehicles in the household
  5. ![](./VERPAT_images/checkmark.gif) **Hhsize**: size of a household
- **Assign Vehicle Age**:  An age is assigned to each vehicle based on the following model variables:
  1. ![](./VERPAT_images/checkmark.gif) **IncGrp**: total annual household income in dollars
  2. ![](./VERPAT_images/checkmark.gif) **Hhvehcnt**: number of vehicles in the household
  3. ![](./VERPAT_images/checkmark.gif) **VehType**: type of vehicle
- **Assign Initial Fuel Economy**: Assign fuel economy to each vehicle based on the following model variables:
  1. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **VehAge**: age of vehicle
  2. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **Hhvehcnt**: number of vehicles in the household
  3. ![](C:/Users/aditya.gore/OneDrive%20-%20Resource%20Systems%20Group,%20Inc/VisionEval.wiki/VERPAT_images/checkmark.gif) **VehType**: type of vehicle
- ​