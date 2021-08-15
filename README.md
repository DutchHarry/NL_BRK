NL_BRK

Or data from the Dutch Land registry:

download:
https://www.pdok.nl/downloads/-/article/basisregistratie-kadaster-brk-

processing with QGIS (whcih takes a while for the whole of NL)
https://qgis.nl/tag/brk/?lang=en


Issue: It doesn’t easily relate to oneanother
dkk_openbareruimtelabel contains the BAG ID of the OPR
dkk_pand.gml contains the BAG ID of the PND, a point location, and polygons of the property
ddk_perceel has point coordinates of the area on which the property is situated
ddk_kadastralegrens contains the boundaries of the land on which the property is situated

You generate polygons from KadastraleGrens in KadastraleVlak
and create KadastralePercelen where the point of the Perceel is inside the polygon
You then also link the point of Pand to KadastralePercelen.
I went for the same procedure (the Pand point within KadastralePercelen)
In reality this is a complex issue, as in reality local councils use a decision tree to relate the Pand to an area, which has more to do with how the polygons of Pand and KadastralePerceel overlap.
Don't think it'll make much of a difference in most cases, but haven't tested that assumption.


