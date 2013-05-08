Coordinates from single point GPS measurements are in WGS84. The positioning accuracy from such measurements is typically in the order of 2-10 m. For positioning accuracy on the centimeter level one must perform GPS measurements relative to a well-known reference. The measurements could be static measurements relative to ETRS89 or ITRF, RTK measurements relative to ETRS89 or measurements using one of the global positioning services, which are typically relative to the current ITRF – in 2013 it is ITRF2008.

When using coordinates it is crucial to know the GPS observation method and which reference is used. It is not sufficient to state that the coordinates are in WGS84; it can be ETRS89 or ITRF. In 2013, the difference between the horizontal coordinates of a fixed point in these two references is approximately 65 cm. Some years ago it was not common to do measurement using a global positioning service, but positioning services are used more frequently today, and it is then more important to specify the exact reference instead of using the term WGS84.



**What is WGS84 in KMSTrans2?**

In former versions of KMSTrans it was stated that WGS84 ≈ ETRS89. In the new version we want to elaborate on this statement, because as time goes by it is not quite true anymore. The fact is that the definition of WGS84 has changed during time. When ETRS89 was defined it was reasonable to say that WGS84 ≈ ETRS89, but since then the definition of WGS84 has been adjusted several times, so now WGS84 is much closer to the current ITRF than to ETRS89.

The different versions of WGS84 are denoted by a GPS week number indicating the time of definition. By the new version of KMSTrans we will introduce the GPS week number that defines the version of WGS84 closest to ETRS89. This version of WGS84 is called WGS84(G730). With this notation it is still reasonable to say that WGS84 ≈ ETRS89. The latest version of WGS84 has the week number G1674 and today WGS84(G1674) ≈ ITRF2008.

The reason for to keep the relationship between WGS84 and ETRS89 in KMSTrans2 is, that the user should still have the possibility to use the term WGS84 for coordinates in ETRS89. In KMSTrans2 as in earlier versions of the software the user will still get the same results when using either WGS84 or ETRS89. This implies that it is not possible to transform between WGS84 and ETRS89.

The addition of the GPS week number is not of practical importance in the transformation software. It is a matter of presenting the relationship between WGS84 and ETRS89 more correctly, and to make clear to the user that it is important to be aware of the observation method and the reference when the required positioning accuracy is on the centimeter or decimeter level.



**WGS84 on Greenland and the Faroe Islands**

The relationship between WGS84 and ETRS89 described above relates to Denmark. For Greenland and the Faroe Islands there is a similar relationship between WGS84 and the national reference: In Greenland WGS84 ≈ GR96, which implies that it is not possible to transform between WGS84 and GR96. For the Faroe Islands WGS84 ≈ ETRS89 like in Denmark.



**What about transformations between ITRF and ETRS89?**

In KMSTrans2 it is not possible to transform between ITRF and ETRS89. This may change at a later date, as we plan to introduce a plug-in for transformation between ETRS89 and different ITRF’s - and between GR96 and different ITRF’s for Greenland.
