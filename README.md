# MasterGrid
Per-master grids for Glyphs.app (based on [jenskutilek](https://github.com/jenskutilek/MasterGrid)'s plugin) with an input for an offset.

MasterGrid lets you set a grid that is not applied globally like the grid you can set in the font info, but per master.

<img src="Images/screenshot.png" width="539" height="599" alt="">

Activate the grid display via the menu ‘View > Show Master Grid’. The grid is just a visual guide, it is not used for snapping.

Set or delete the grid for the current master via the menu ‘Edit > Master Grid…’ (you need to have the `vanilla` module installed to be able to display the dialog).

If you don’t want to install `vanilla`, you can still set the grid via the Macro Panel:

```python
Font.masters[0].userData["de.kutilek.MasterGrid.value"] = [100, 100] # x, y
Font.masters[0].userData["de.kutilek.MasterGrid.type"]  = "units"    # absolute font units
```
You can also use relative subdivisions of the units per em value:

```python
Font.masters[1].userData["de.kutilek.MasterGrid.value"] = [10, 10] # x, y
Font.masters[1].userData["de.kutilek.MasterGrid.type"]  = "div"    # subdivision of the em value
```

The resulting grid of the two examples will be the same for a font with 1000 units per em.
