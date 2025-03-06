# Geographic Coverage Present

### Message:

```
Info: geographicCoverage is present.
```

### Description:

_Including geographic coverage helps users search for datasets by location and provides important spatial context for understanding the data._

### Solution:

Many datasets benefit from having geographic coverage, though it may not be necessary for all. If applicable, include at least one **geographic coverage** element that defines the spatial extent of your dataset.

- The **bounding coordinates** should describe the dataset’s full extent. A default approach is to use the nominal boundaries of the sampling area, but a more precise method (recommended) is to set the maximum extent of the data for the **east, west, north, and south**.
- If study sites are far apart and combining them into a single bounding box would be misleading, include multiple **geographic coverage** elements. For example, a cross-site study should have separate bounding boxes for each site.
- For accuracy, it’s recommended to use **six decimal places** for coordinates.

