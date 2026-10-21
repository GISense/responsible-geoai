You can ignore this folder. Nothing in the lab asks you to open it.

It holds saved copies of the OpenStreetMap downloads that Sections 1 and 2
make. OSMnx looks in here before it goes to the network, so those cells will
run even if OpenStreetMap's servers are slow or down -- which happens, and is
not something you did wrong.

Three things worth knowing:

  * Leave the folder where it is, next to the notebook. OSMnx finds it by
    location. If you move or rename it, the cells fall back to downloading
    normally, which still works when the servers are up.

  * Exercise 1 is mostly not covered, because it asks you to choose your own
    city and there is no way to have saved a copy of that in advance. The one
    exception is the worked example the notebook gives you --

        ox.graph.graph_from_address("Austin, Texas, USA", dist=3000,
                                    network_type="drive")

    -- which is saved here, so that line works offline. Any other city or any
    other dist is a fresh download. If OpenStreetMap is unreachable when you
    get there, wait a few minutes and re-run the cell. If it stays down, email
    me -- that is my problem to solve, not yours.

  * The grey basemap behind the accessibility maps comes from a different
    service and is not cached here. If it is unavailable your map still draws,
    just without the grey background, and the notebook prints a short note
    saying so. That is not an error and costs you nothing.

A `cache_tiles/` folder may appear next to this one once you run the mapping
cells. That is the basemap doing the same thing for itself. You can delete it
any time.
