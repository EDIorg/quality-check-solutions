# Schema Valid

A variety of issues can arise under this general check. To help you navigate them, we’ve outlined different potential issues below. Please search for the specific message you are encountering to find out more about the issue and how to resolve it.


## Coverage Present

### Message:

```
Warning/Error: Failed to validate for namespace: 'https://eml.ecoinformatics.org/eml-2.2.0'; cvc-complex-type.2.4.b: The content of element 'coverage' is not complete. One of '{geographicCoverage, temporalCoverage, taxonomicCoverage, references}' is expected.
```

### Description:

_Coverage information—whether geographic, taxonomic, or temporal—helps enable advanced searches and improves understanding of your dataset by providing context on location, organismal entities, or time frames._

### Solution:

To resolve this issue, ensure your dataset metadata includes at least one type of coverage: **geographic, taxonomic, or temporal**. If multiple coverage types apply, it’s best to include all relevant ones. However, not every dataset requires all types, so focus on what’s most applicable to your data.
