# Road use in Exeter
Exploring Estimated Average Daily Flows (AADFs) in Exeter with data from 2000 - 2014.

Using [Jupyter Notebook](http://jupyter.org/) with the Anaconda (2.4.1) Python 3.5.

These scripts use the data files `Exeter_city_only`,`Exeter_box.csv` and `road_coords.csv`.

**Before you start**

Create the environment for exeter_traffic:

Inside exeter_traffic/:     
`conda env create -f environment.yml`

`source activate exeter_traffic`

Run [make_relative_csv.py](/scripts/make_relative_csv.py) to create some more data subsets
which the other scripts can pull from.   

Once you have done the above you should be able to run any of the following scripts, and make adjustments (focusing on
different years for example). You should also adjust the input/output folders in the following scripts. 

### Scripts
`plot_barplots.py`  - Makes 3 sets of barplots for each year: 1) Using all Roads, 2) Inner Roads (Excluding A30 and M5) 3) Outer Roads 
(just A30 and M5). 

`plot_relative_maps.py`  - Makes maps for each Vehicle type for each year. Each map contains normalised values over the Exeter road 
network.

`plot_color_maps.py` - Only plots for 2014 at the moment. Makes a map with different colours for different roads and uses all traffic data.

`plot_timeseries.py` - plot a time series for each of the transport types

### Notebooks

Initial exploration and working that went into making the scripts described above. 

         
`Exeter_traffic_data_exploration.ipynb` - Initially looking at data for all of Devon before working out how to make the subset for Exeter.

`Exeter_traffic_data_exploration2.ipynb` - Still looking at the Devon-scale, exploring availability over the time series. Checking data 
availability on each road in each year and looking for gaps in the time series. 

`day2_plotting_road_markers.ipynb` - Working out how to make the maps.    

`day2_preparing_roadmarkers.ipynb` - Making a dataframe which has a series of points for each CP. Each point has unique latitude and 
longitude which is how the maps with road data is overlayed. This is included in the `make_relative_csv.py` script.

`Day2-Preparing_metrics_for_maps.ipynb` - Playing around with distributions and eventually making data to make the maps.  

`Day2_transport_trends.ipynb` - Plotting and calculating trends. 

`day3_barplots_roads.ipynb` - Working for making the plot_barplots.py script. Here I also calculated the % frequency of each Vehicle for 
2014 for a) All Vehicles and b) Inner Roads and c) Outer Roads. 

### Other scripts

Other scripts which specifically focus on:

1) Just outer roads - `/scripts/Outer`      
2) Just inner roads - `/scripts/Inner`        
3) Data without cars (to get a better look at less frequent transport modes, particularly in the city) -  `/scripts/NoCars`   




