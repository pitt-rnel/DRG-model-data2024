README

This folder contains files containing data for the paper 

Farooqui J, Nanivadekar AC, Capogrosso M, Lempka SF, Fisher LE. The effects of neuron morphology and spatial distribution on the selectivity of dorsal root ganglion stimulation. J Neural Eng. 2024 Sep 4. doi: 10.1088/1741-2552/ad7760. PMID: 39231464.

There are three types of model, as described in the paper. In this folder are files containing details about the placement, size, type, etc., AS WELL AS THE OUTPUTS OF SIMULATION for each neuron that was randomly placed according to the axon-only, random, or realistic configuration as described in the paper. 


File naming convention: data_<model type>.csv OR data_<model type>_<electrode type>.csv OR data_<model type><number>_<electrode type>_<shift>.csv
	<model type> is one of: axon_only, random, realistic
	<electrode type> is one of: epineural, penetrating	
		NOTE: if <electrode type> is missing from the file name, then the file contains both types
	<shift> refers to electrode shifts from center in the realistic model type, and is one of: 	
									xp0_75 (0.75mm shift in positive x direction),
									xn0_75 (0.75mm shift in negative x direction), 
									zp0_75 (0.75mm shift in positive z direction)



Rows:
Each row contains details of one neuron in the simulation


Columns:

** denotes results/ simulation outputs 

index 		--	index number
drg 		-- 	model type (should match <model type> in the file name)
drgnum 		--	iteration of cell placements within this model type (should be consistent within files and may differ across files, can ignore)
ePos		-- 	electrode shift relative to center point of dorsal surface: 	x0y0 (no shift), 
											xp0_75 (0.75mm shift in positive x direction), 
											xn0_75 (0.75mm shift in negative x direction), 
											zp0_75 (0.75mm shift in positive z direction)
fiberD_c	--	fiber diameter, axon central branch (applies to pseudounipolar neurons only)
fiberD_p	--	fiber diameter, axon peripheral branch (applies to pseudounipolar neurons only)
fiberType	-- 	Aa (A-alpha) OR Ab (A-beta)
ground		-- 	saline 
neckAngle 	-- 	angle between cell body center point and t-junction center point (applies to pseudounipolar neurons only)
neckD 		-- 	fiber diameter, stem/ neck axon (applies to pseudounipolar neurons only)
nodes		-- 	number of nodes in the axon (applies to axons of passage only)
phase		-- 	b (bipolar stimulation applied) OR m (monopolar stimulation applied) [this dataset contains only b]
polarity	-- 	-1 (cathodic leading) OR 1 (anodic leading) [this dataset contains only -1]
pw		-- 	pulse width for leading phase of stimulation pulse, in ms (0.08 for this dataset)
scatterType	-- 	soma (pseudounipolar neuron) OR axon (aoxn of passage)
scatter_d	-- 	soma diameter (applies to pseudounipolar neurons only) OR fiber diameter (applies to axons of passage only)
scatter_{x,y,z}	--	x,y,z coordinates of cell body, approximate (applies to pseudounipolar neurons only) OR endpoint of axon (applies to axons of passage only)
shift		-- 	no longer relevant, can ignore
soma_{x,y,z} 	-- 	x,y,z coordinates of cell body, final (applies to pseudounipolar neurons only)
**spikeOrigin	-- 	part of cell in which action potential initiated (soma, iseg, neck{0-3}, tjn, central, periphery for pseudounipolar neurons; node number for axons of passage)
**spikeT		-- 	time of initial spike, in ms (note that stimulation is applied after a 5ms delay)
status		-- 	trial status (success OR error)
**thresh 		-- 	threshold for activation of single spike for the neuron
timestep	-- 	simulation timestep
tjnPos 		-- 	tuple containing (x,y,z) coordinates of t-junction (applies to pseudounipolar neurons only)
tjn_{x,y,z}	-- 	x,y,z coordinates of t-junction (applies to pseudounipolar neurons only)
**{x,y,z}_spike	-- 	x,y,z coordinates of spikeOrigin (location of initial action potential)
xshift		-- 	amount of random shift along the x axis applied to axon of passage in um (applies to axons of passage only)
