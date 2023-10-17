Used https://github.com/Nictiz/Nictiz-STU3-Zib2017 as a basis.

Output is here: hl7nl.github.io/Nictiz-STU3-ZIb2017-IG

Issues:
1. Duplicate ID, so removed for now:
    - pdfa-IHE.MHD.DocumentManifest.xml
    - pdfa-IHE.MHD.Query.Minimal.DocumentReference.xml
1. Removed for now
    - folder zib-Medication
    - folder eAfspraak
    - zib-Infusion-* references medication?
1. Copied ValueSets -> input/resources
1. Copied Extensions.. -> input/profiles
1. Copied Examples.. -> input/examples

Questions:
1. What to use for packageId = nictiz.fhir.nl.stu3.zib2017
    - For now use "zibs2017" as id/name/packageId