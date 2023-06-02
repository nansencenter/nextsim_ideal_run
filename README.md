# How to run an idealised simulation with neXtSIM

## Prerequsites:
* neXtSIM code and the libraries are compiled;
* This repository is cloned
* A directory to store >3 GB data is prepared

## Procedure
1. Set environmental variable NEXTSIM_MESH_DIR to the directory that contains the file coast_10km.msh
2. Change the parameter `exporter_path` in the config file `coast10km.cfg` to the directory where you will store the data
3. Run neXtSIM: `mpirun -mca btl ^openib -np 14 nextsim.exec --config-files=coast10km.cfg`. the first option `-mca btl ^openib` prevent some error messages. The second option `-np 14` sets the number of cores to use. In the option `--config-files=coast10km.cfg` you can give the file in the current directory or an absolute path.