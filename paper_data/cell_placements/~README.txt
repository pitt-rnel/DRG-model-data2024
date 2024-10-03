#README

This folder contains 2 folders containing files containing data for the paper:

Farooqui J, Nanivadekar AC, Capogrosso M, Lempka SF, Fisher LE. The effects of neuron morphology and spatial distribution on the selectivity of dorsal root ganglion stimulation. J Neural Eng. 2024 Sep 4. doi: 10.1088/1741-2552/ad7760. PMID: 39231464.

Files represent data from three types of model, as described in the paper. 


## FOLDERS INCLUDED

In the folder titled "cell_placements" are 3 *.csv files containing details about the placement, size, type, etc. of each neuron that was randomly placed according to the axon-only, random, or realistic configuration as described in the paper.


### CELL_PLACEMENTS FOLDER

File naming convention: <model type>.csv

	<model type> is one of: axon_only, random, realistic


Rows:
Each row contains details of one neuron in the simulation


Columns:
index		-- 	index number
area		-- 	area of the circle made by the cross-section of the soma (applies to pseudounipolar neurons only) OR the axon (applies to axons of passage only)
axon_rad_loc 	-- 	distance of the axon from the center of the DRG (measured radially)
d		-- 	diameter of soma (applies to pseudounipolar neurons only) OR axon (applies to axons of passage only)
fiberD_p	-- 	fiber diameter of axon
fiberType	-- 	Aa (A-alpha) OR Ab (A-beta)
new_angle	--	angle between T-junction and soma (applies to pseudounipolar neurons only)
orig_angle	-- 	angle between center of DRG and T-junction
r		-- 	radius of soma (applies to pseudounipolar neurons only) OR axon (applies to axons of passage only)
tjn{x,y,z}	--	x,y,z coordinates of T-junction (applies to pseudounipolar neurons only)
type		-- 	soma (pseudounipolar neuron) OR axon (axon of passage)
{x,y,z}		--	x,y,z coordinates of soma (applies to pseudounipolar neurons only) OR axon (applies to axons of passage only)
soma_{x,y,z}	--	x,y,z coordinates of soma (applies to pseudounipolar neurons only)
xshift		-- 	amount of random shift along the x axis applied to axon of passage in um (applies to axons of passage only)


