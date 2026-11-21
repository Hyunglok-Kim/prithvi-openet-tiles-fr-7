# Prithvi-OpenET-Tower browse tiles — public preview, part 7 of 7

Numeric map tiles for the [Prithvi-OpenET-Tower data portal](https://github.com/Hyunglok-Kim/prithvi-openet-portal): 30 m monthly
evapotranspiration of France, 2013-04 to 2026-08, reduced to zoom 3–10
so that it fits on GitHub Pages. The full set goes to zoom 12 (30 m).
11 small areas around the paper's French flux-tower sites (Auradé, Bilos, Col du Lautaret, Estrées-Mons, Fontainebleau-Barbeau, Grignon, Hesse, Lamasquère, Méjusseaume, Puéchabon, Toulouse)
keep the native zoom 12 in the `*.fine.pmtiles` files; outside their outlines those tiles repeat zoom 10.

One PMTiles file per month (`monthly/`) and per climatology layer (`clim/`). A tile is an 8-bit
grayscale PNG that holds values, not colours: `value = DN × dn_step`, `DN 255 = no data`.
These tiles are for looking, not for analysis — they are resampled to Web Mercator, averaged and
rounded. Use the GeoTIFFs for any calculation; they will be released after the paper is accepted.

Made by `pipeline/make_preview_copy.py` of the portal repository from data version `prototype-2026-11-21`.
Do not edit by hand: rebuild and replace.

HydroAI Lab, Gwangju Institute of Science and Technology — hyunglokkim@gist.ac.kr
