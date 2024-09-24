This is EinMind Client Documentation

Installation
```shell
pip install einmind
```


ICD10CM term mapping
```python
from einmind import ICD10CMClient
icd10cm_client = ICD10CMClient()
result = icd10cm_client.code_term(term='headache')
print(result)
```


SNOMED CT term mapping
only diseases and procedures are covered
```python
from einmind import SNOMEDCTClient

# Initialize the SNOMED CT Client
snomed_client = SNOMEDCTClient()

# Code a disease term
result = snomed_client.code_term(term='headache', term_category="PROBLEM")

# Code a procedure term
result = snomed_client.code_term(term='colonoscopy', term_category="PROCEDURE")
```
