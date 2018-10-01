# VE-State Development Status
The purpose of this page is to report on the development status of VE-State. Items will be added to the page to report on significant development milestones. Each item will have a corresponding project issue to provide reviewers with a venue for commenting on the item.

## Multi-Azone, Multi-Marea Test of VE-RSPM
### September 11, 2018
Most of the VE-RSPM code should work with VE-State unless there are errors in the coding which don't allow a module or modules to work with multiple Mareas or Azones. The VE-RSPM modules were developed with test inputs having just one Azone and one Marea. The purpose of this task is to test VE-RSPM with multiple Azones and Mareas, to identify problematic code, and to correct the code so that it will run. This task has been completed. The test and modifications to VE-RSPM modules are in the develop branch of the VisionEval GitHub repository.  

Test datasets were developed by duplicating the RVMPO datasets that were used to test VE-RSPM. These datasets have one Azone, named RVMPO, and one Marea, also named RVMPO. The duplicate Azones are named RVMPOA, RVMPOB, and RVMPOC. The duplicate Mareas are named RVMPOX and RVMPOY. Azones RVMPOA and RVMPOB are associated with RVMPOX while the RVMPOC Azone is associated with the RVMPOY Marea. The Bzones in each Azone were duplicated as well and named (using A, B, C) to associate them with Azones. The Bzone centroid locations for the duplicated Bzones are offset in latitude so that they don't overlap. These test data are located in the Test2 directory of the VERSPM directory. The 'revise_inputs.R' script in the directory is used to create the multi-Azone, multi-Marea datasets.  

VE-RSPM was run first for the base year and then for both the base year and future year to identify issues. Issues with a few modules were identified and corrected. Following are problems that were identified and corrected:  

* CalculateBaseRoadDvmt module in the VETravelPerformance package - The ComSvcDvmtHhDvmtFactor is applied by Marea but had only one entry. The calculations were corrected so there is an entry for each Marea.

* CalculateFutureRoadDvmt module in the VETravelPerformance package - The procedures for calculating commercial service DVMT and heavy truck DVMT by Marea were not properly vectorized. Changes were made to vectorize.

* CalculateComEnergyAndEmissions module in the VETravelPerformance package - A single value of heavy truck ecodrive factor for rural portions of Mareas is needed but multiple values were provided. This was corrected by calculating a weighted average value.  

* CalculatePTranEnergyAndEmissions module in the VETravelPerformance package - Code to calculate DVMT by Marea and powertrain type wrongly multiplied DVMT by Marea over the wrong dimention of the DVMT proportions matrix by Marea and powertrain type. This was corrected.  

With the corrections, the multi-Azone, multi-Marea tests run successfully.  

## Bzone Synthesis: Synthesizing Zones with Activity Density, Diversity, and Destination Accessibility Characteristics
### October 1, 2018
Methods have been developed for synthesizing Bzones in urbanized areas, allocating the numbers of households and jobs in each, and attributing each with activity density, diversity, and destination accessibility characteristics. Documentation of the methods is included in a new **VESimHouseholds** directory of the **modules** directory in the **develop** branch. Here is the [link](https://github.com/gregorbj/VisionEval/blob/develop/sources/modules/VESimLandUse/analyze_3Ds.html). You will need to download the file to view it. To do so, right-click on the **Download** button and then click on the **Save link as...** menu choice to download the file to your computer. Then open the file. It is a web page so when you double click on it, it will open in your web browser. I have opened an issue (#204) that you can use to comment on the method.

