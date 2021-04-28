# QR-code-location-determination-for-indoor-pedestrian-navigation-path-planning
Two software packages were employed in this implementation: Quantum GIS (QGIS) and Rhinoceros (with Grasshopper). 

In the whole process, QGIS is used to edit the indoor maps, including adding attributes, setting the coordinate system, and editing footprints of indoor elements. 

Rhinoceros (with Grasshopper) is used to process the entire procedures of ITSP path planning, and the whole data process is developed in Python script. 

By using QGIS, we edit the floor plan into four shapefile layers, including rooms, corridors, atriums, and POIs, in which except for the POIs, all other spaces are polygons. 
The shops, toilets, escalators, stairs, and lifts are included in the layer named Rooms, while the ATM and Bench are edited in POIs layer. Atriums and corridors are edited in two separated layers named Atriums and Corridor.

Each element in each layer has three attributes: {ID, name, category}. 

ID records the id of each element, name keeps the semantic of the element (e.g., "Coles", "EscalatorL5_L4", "ToiletA_L5", "ATM_A_L5"), while category records the supplement information, for instance, the category of the shop named "Kidstuff", is "Books, stationary and gifts, Entertainment and activities, Sporting goods stores, Toys and hobbies stores".

QR code location determination is used for computing the locations of QR codes.
Location determination of Dummy nodes is designed for determining the locations of dummy nodes.
Navigation network derivation is employed to construct the indoor navigation network on the basis of Poincare duality.

The file (.gh) integrates all the functions together to finish the whole process, in which the data sources are shapefiles.
