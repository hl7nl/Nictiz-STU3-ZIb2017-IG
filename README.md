Output is here: https://hl7nl.github.io/Nictiz-STU3-ZIb2017-IG

Steps:
1. git clone --depth 1 https://github.com/Nictiz/Nictiz-STU3-Zib2017
1. Copied "Profiles - ZIB 2017" > input/profiles
1. Copied "Profiles - ZIB 2017/ValueSets" -> input/resources
1. Copied Capabilitystatements > input/capabilitystatements
1. Copied Examples -> input/examples

Issues:
1. Duplicate ID, so removed for now:
    - pdfa-IHE.MHD.DocumentManifest.xml
    - pdfa-IHE.MHD.Query.Minimal.DocumentReference.xml
1. Removed for now
    - folder zib-Medication
    - folder eAfspraak
    - zib-Infusion-* references medication?

Questions:
1. What to use for packageId = nictiz.fhir.nl.stu3.zib2017
    - For now use "zibs2017" as id/name/packageId

---

# Build

```
> docker run --rm -it -v $(pwd):/home/publisher/ig hl7fhir/ig-publisher-base:latest
@> _updatePublisher.sh
@> _genonce.sh
```

# Publish

```
> rm -r docs/*
> cp -r output/* docs
> git add docs
> git commit -a
> git push
```