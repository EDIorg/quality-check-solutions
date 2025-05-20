# Schema Valid

A variety of issues can arise under this general check. To help you navigate them, we’ve outlined different ways to identify and resolve common problems below.

### Message:

The general message format for this issue typically includes messages like:

```
Error: Failed to validate for namespace: 'https://eml.ecoinformatics.org/eml-2.2.0'; cvc-complex-type.2.4.b: The content of element '[PARENT-ELEMENT]' is not complete. One of '{[CHILD-ELEMENT-1], [CHILD-ELEMENT-2], ...}' is expected.
```

Or:

```
Error: Element '{https://eml.ecoinformatics.org/eml-2.2.0}eml': The attribute '[ATTRIBUTE-NAME]' is required but missing.
```


### Description:

**Schema validity** ensures that the metadata structure follows the rules defined by the EML schema. This structural consistency is essential for enabling **machine parsing**, **interoperability**, and **downstream application use**. Think of it as a shared set of expectations about how metadata should be organized so that software can make sense of it.

### Solution:

There are several ways to diagnose and fix schema validation issues:

#### Use an XML Editor  
Open your EML XML document in a standard XML editor. These tools typically provide **line-by-line feedback** when the structure doesn’t meet the schema’s expectations, helping you pinpoint where fixes are needed.

#### Use ezEML’s Built-in Validation Tool  
ezEML offers an easy-to-use interface for validating EML files:
1. [Log in to ezEML](https://ezeml.edirepository.org/)
2. Go to the `Import/Export` menu.
3. Select **Validate an EML XML file**.
4. Choose your EML XML file and run validation.
5. A **detailed validation report** will be displayed, highlighting any issues.

#### Use the EMLvp Python Package  
The [EMLvp](https://github.com/PASTAplus/EMLvp) Python package is the **same validation engine used by ezEML** and can be run locally. It’s particularly helpful for advanced users or batch validations.

---

> **Schema validation messages can be cryptic**—you’re not alone if they’re hard to interpret. Feel free to reach out to our support team at **support@edirepository.org** if you need help understanding or resolving an issue. We’re here to help!
