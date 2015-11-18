GeoJSON-Attribute-Cleaner-And-Filter
====================================


Fork from GeoJSON-Attribute-Cleaner by Pimentoso, a simple web based attribute cleaner for reducing GeoJSON file size.

Adds some new options: filters features by property values and removes every attribute from a GeoJSON except the fields selected by users (and country name by default).

Also removes whitespace.
Input must be a valid JSON.

## Quick guide to clean and filter a GeoJSON:

- Open the produced JSON file in a text editor, and paste it in the GeoJSON Attribute Cleaner. 
- Click ''Get Properties''.
- Select items on ''Properties preserved'.
- Select one option on ''Filter property'' (optional) and click ''Get Values''.
- Select one of the options in ''Filer value'' or write it.
- Click 'Process'.
- Use the resulting reduced JSON for your maps.

## Example output
Input:
```json
{"type":"FeatureCollection","features":[{"type":"Feature","properties":{"scalerank":1,"featurecla":"Admin-0mapunit","labelrank":5.0,"sovereignt":"Barbados","sov_a3":"BRB","adm0_dif":0.0,"level":2.0,"type":"Sovereigncountry","admin":"Barbados","adm0_a3":"BRB","geou_dif":0.0,"geounit":"Barbados","gu_a3":"BRB","su_dif":0.0,"subunit":"Barbados","su_a3":"BRB","brk_diff":0.0,"name":"Barbados","name_long":"Barbados","brk_a3":"BRB","brk_name":"Barbados","brk_group":null,"abbrev":"Barb.","postal":"BB","formal_en":"Barbados","formal_fr":null,"note_adm0":null,"note_brk":null,"name_sort":"Barbados","name_alt":null,"mapcolor7":4.0,"mapcolor8":1.0,"mapcolor9":5.0,"mapcolor13":3.0,"pop_est":284589.0,"gdp_md_est":5425.0,"pop_year":-99.0,"lastcensus":2010.0,"gdp_year":-99.0,"economy":"6.Developingregion","income_grp":"2.Highincome:nonOECD","wikipedia":-99.0,"fips_10":null,"iso_a2":"BB","iso_a3":"BRB","iso_n3":"052","un_a3":"052","wb_a2":"BB","wb_a3":"BRB","woe_id":-99.0,"adm0_a3_is":"BRB","adm0_a3_us":"BRB","adm0_a3_un":-99.0,"adm0_a3_wb":-99.0,"continent":"NorthAmerica","region_un":"Americas","subregion":"Caribbean","region_wb":"LatinAmerica&Caribbean","name_len":8.0,"long_len":8.0,"abbrev_len":5.0,"tiny":3.0,"homepart":1.0},"geometry":{"type":"Polygon","coordinates":[[[-59.493,13.082],[-59.611,13.102],[-59.647,13.303],[-59.592,13.318],[-59.428,13.153],[-59.493,13.082]]]}}]}
```

Output:
```json
{"type":"FeatureCollection","features":[{"type":"Feature","properties":{"name":"Barbados"},"geometry":{"type":"Polygon","coordinates":[[[-59.493,13.082],[-59.611,13.102],[-59.647,13.303],[-59.592,13.318],[-59.428,13.153],[-59.493,13.082]]]},"id":"BRB"}]}
```

## References

- https://github.com/Pimentoso/GeoJSON-Attribute-Cleaner
- http://blog.thematicmapping.org/2012/11/how-to-minify-geojson-files.html
- http://bost.ocks.org/mike/map/