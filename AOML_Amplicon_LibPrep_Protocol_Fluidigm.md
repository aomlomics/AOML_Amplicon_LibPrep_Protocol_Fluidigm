---

# MIOP terms
methodology_category: omics analysis
project: "NOAA Atlantic Oceanographic and Meteorological Laboratory Omics Program; https://github.com/aomlomics/protocols; https://zenodo.org/communities/aomlomics"
purpose: PCR [OBI:0000415], Library Preparation [OBI:0000711]
analyses: PCR [OBI:0000415], Library Preparation [OBI:0000711]
geographic_location: Atlantic Ocean [GAZ:00000344], Gulf of Mexico [GAZ:00002853]
broad_scale_environmental_context: marine biome [ENVO:00000447], marine photic zone [ENVO:00000209]
local_environmental_context: marine biome [ENVO:00000447], marine photic zone [ENVO:00000209]
environmental_medium: sea water [ENVO:00002149], polymerase chain reaction [OBI:0000415]
target: whole genome sequencing [OBI_0002117]
creator: Luke Thompson
materials_required: vortexer [OBI:0400118], PCR instrument [OBI:0000989], Centrifuge [OBI:0400106]
skills_required: sterile technique, pipetting skills, standard molecular technique
time_required: 200
personnel_required: 1
language: en
issued: 2026-05-08
audience: scientists
publisher: NOAA Atlantic Oceanographic and Meteorological Laboratory
hasVersion: 1
license: CC0 1.0 Universal
maturity level: mature

# FAIRe terms
barcoding_pcr_appr: two-step pcr
library_id: not applicable
platform: AVITI
instrument: 
seq_kit: 
lib_layout: paired end
sequencing_location: 
adapter_forward: 
adapter_reverse: 
lib_screen: 
mid_forward: 
mid_reverse: 
filename: 
filename2: 
seq_method_additional: not applicable

---

# NOAA/AOML Amplicon Library Prep Protocol

## PROTOCOL INFORMATION

### Minimum Information about an Omics Protocol (MIOP)

- MIOP terms are listed in the YAML frontmatter of this page.
- See <https://github.com/BeBOP-OBON/miop/blob/main/model/schema/terms.yaml> for list and definitions.

### Making eDNA FAIR (FAIRe)

- FAIRe terms are listed in the YAML frontmatter of this page.
- See <https://fair-edna.github.io/download.html> for the FAIRe checklist and more information.
- See <https://fair-edna.github.io/guidelines.html#missing-values> for guidelines on missing values that can be used for missing FAIRe or MIOP terms.

### Authors

| PREPARED BY | AFFILIATION | ORCID | DATE |
| ------------- | ------------- | ------------- | ------------- |
| Luke Thompson | NOAA/AOML, MSU/NGI | <https://orcid.org/0000-0002-3911-1280> | 2026-05-11 |
| Sammy Harding | NOAA/AOML, MSU/NGI | <https://orcid.org/0009-0008-8885-6140> | 2026-05-11 |

### Related Protocols

- This section contains protocols that should be known to users of this protocol.
- Internal Protocols: Derivative or altered protocols, or other protocols in this workflow.
- External Protocols: Protcols from manufacturers or other groups. 
- Include the link to each protocol.
- Include the version number (internal) or access date (external) of the protocol when it was accessed.

#### Internal Protocols

| PROTOCOL NAME | LINK  | VERSION | RELEASE DATE|
| ------------- | ------------- | ------------- | ------------- |
| AOML 'Omics Protocols | https://github.com/aomlomics/protocols | not applicable | ongoing |
| NOAA 'Omics Metabarcoding Assays | https://github.com/NOAA-Omics/noaa-omics-metabarcoding-assays | not applicable | ongoing |

#### External Protocols

| PROTOCOL NAME | LINK | ISSUER / AUTHOR | ACCESS DATE |
| ------------ | ------------ | ------------ | ---------- |
| Just-a-Plate 96 PCR Purification and Normalization Kit Manual | http://www.wuhancharmbiotech.com/product/upload/20150630/1435646883.pdf | CharmBiotech | 2026-05-08 |
| Quant-iT™ dsDNA High-Sensitivity Assay Kit Manual| https://documents.thermofisher.com/TFS-Assets/LSG/manuals/Quant_iT_dsDNA_HS_Assay_UG.pdf | Invitrogen | 2026-05-08 |
| D1000 ScreenTape Assay for TapeStation Systems Manual | https://www.agilent.com/cs/library/usermanuals/public/D1000_QuickGuide.pdf?srsltid=AfmBOorjxQZ5RHiYUL_5wIfvgNkGtScU95raLNQtq6qmMPH2MgYnrHpk | Agilent | 2026-05-08 |

### Protocol Revision Record

| VERSION | RELEASE DATE | DESCRIPTION OF REVISIONS |
| ------------- | ------------- | ------------- |
| 1.0.0 | 2026-05-11 | Initial release |

### Acronyms and Abbreviations

| ACRONYM / ABBREVIATION | DEFINITION |
| ------------- | ------------- |
| NOAA | National Oceanographic and Atmospheric Administration |
| AOML | Atlantic Oceanographic and Meteorological Laboratory |
| MSU | Mississippi State University |
| NGI | Northern Gulf Institute |
| PCR | Polymerase chain reaction |
| eDNA | environmental DNA |
| NTC | No template control |
| EtOH | Ethanol |

## BACKGROUND

### Summary

This protocol was developed and implemented by NOAA AOML's Molecular and Computational Biodiversity group to generate Illumina-compatible environmental DNA (eDNA) amplicon libraries using the Fluidigm CS1/CS2 indexing system, enabling conversion of primary PCR amplicons into uniquely dual-indexed libraries suitable for AVITI sequencing. The workflow consists of a secondary indexing PCR, bead-free normalization and purification, pooled library quality control and final validation of library concentration and fragment size before sequencing submission.

### Method description and rationale

This protocol uses a secondary PCR to attach Illumina-compatible adapters and unique dual indexes to CS1/CS2-tagged eDNA amplicons, enabling multiplexed sequencing on the AVITI platform. Following indexing, libraries are purified and normalized using the Just-a-Plate™ system to remove residual primers and equalize sample concentrations prior to pooling. The pooled library is then quantified fluorometrically and assessed on the TapeStation to confirm appropriate concentration and fragment size distribution while identifying potential primer-dimer contamination. The two-step PCR design improves amplification consistency and reduces costs associated with fully indexed locus-specific primers, while unique dual indexing minimizes sample misassignment and index hopping. Overall, the workflow is optimized for high-throughput, reproducible preparation of eDNA amplicon libraries suitable for downstream biodiversity and metabarcoding analyses.

### Spatial coverage and environment(s) of relevance

This protocol is intended for environmental DNA (eDNA) metabarcoding applications in marine environments to support high-throughput biodiversity monitoring and ecological assessment.
 
## PERSONNEL REQUIRED

One person with molecular biology experience.

### Safety

There are no hazardous chemicals or materials involved in this protocol. Standard lab safety techniques should still be used such as wearing PPE to avoid skin or eye contact.

### Training requirements

Basic molecular biology training is sufficient for this protocol including sterile technique, pipetting small volumes and programming/running PCR thermal cyclers.

### Time needed to execute the procedure

This protocol takes about 3.5 hours to complete.

## EQUIPMENT

| DESCRIPTION | PRODUCT NAME AND MODEL | MANUFACTURER | QUANTITY | REMARK |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| **Durable equipment** |
| Thermal cycler | Mastercycler Nexus Thermal Cycler | Eppendorf | 1 | Can be substituted with generic |
| Vortex | Vortex Genie | Scientific Industries | 1 | Can be substituted with generic |
| PCR Plate Centrifuge | Microplate Centrifuge | Generic Brand | 1 | Can be substituted with generic |
| Agilent 4200 TapeStation | Agilent 4200 TapeStation | Agilent | 1 |  |
| 0.5-10 ul Pipette | Eppendorf Research Plus Adjustable-Volume Pipette | Eppendorf | 1 | Can be substituted with any accurate pipette |
| 100-1000 ul Pipette | Eppendorf Research Plus Adjustable-Volume Pipette | Eppendorf | 1 | Can be substituted with any accurate pipette |
| 10-100 ul Pipette | Eppendorf Research Plus Adjustable-Volume Pipette | Eppendorf | 1 | Can be substituted with any accurate pipette |
| 10-100 ul 8-Channel Pipette | Eppendorf Research Plus 8 Channel Pipette | Eppendorf | 1 | Can be substituted with any accurate pipette |
| 0.5-10 uL 8-Channel Pipette | Eppendorf Research Plus 8 Channel Pipette | Eppendorf | 1 | Can be substituted with any accurate pipette |
| Serological Pipette | Eppendorf Easypet 3 Pipette | Eppendorf | 1 | Can be substituted with any accurate pipette |
| **Consumable equipment** |
| DreamTaq Master Mix | DreamTaq PCR Master Mix (2X) | ThermoFisher | 1 |  |
| Just-a-Plate Kit | Just-a-Plate ™ 96 PCR Normalization and Purification Kit, 96 X 10 (Preps) | CharmBiotech | 1 |  |
| Barcode Library | Access Array™ Barcode Library for Illumina® Sequencers— 384, Single Direction | Standard BioTools | 1 |  |
| Quant-iT kit | Invitrogen Quant-iT 1X dsDNA Assay Kits, high sensitivity (HS) and broad range (BR) | Invitrogen | 1 |  |
| TapeStation Assay | TapeStation D1000 DNA ScreenTape & Reagents | Agilent | 1 |  |
| 96-well PCR plate | Armadillo PCR Plate, 96-well, clear, clear wells | ThermoFisher | 1 | |
| Aluminum Foil Sealing Tape | AlumaSeal II Sealing Foils for PCR and Cold Storage | VWR | 7 | Can be substituted with generic | 
| 8-Strip Tubes | 0.2 mL 8-Strip PCR Tubes | Generic Brand | 5 | tubes without caps attached are better |
| Microcentrifuge Tubes | 2.0 mL Microcentrifuge Tube | Generic Brand | 8 | Can be substituted with generic|
| 1000µL Filter Tips | OT-2 Filter Tips, 1000µL | Opentrons | 1 | (box) Can be substituted with generic |
| 200µL Filter Tips | OT-2 Filter Tips, 200µL | Opentrons | 7 | (boxes) Can be substituted with generic |
| 10 ul Filter tips | TipOne Pipette Tips, 10 uL | TipOne | 9 | (boxes) Can be substituted with generic |
| Gloves | Nitrile Gloves, Exam Grade, Powder-free | ULINE | 1 | (box) Can be substituted with generic |
| Kim Wipes | KimWipe Delicate Task Wipers | KimTech | 1 | (box) Can be substituted with generic |
| **Chemicals** |
| 80% Ethanol | Molecular biology grade ethanol |  |  |  |
| Nuclease-free water | Nuclease-Free Water (not DEPC-Treated) | ThermoFisher Scientific | 1 | (mL vial) |

- Description: E.g., "filter".
- Product Name and Model: Provide the official name of the product.
- Manufacturer: Provide the name of the manufacturer of the product.
- Quantity: Provide quantities necessary for one application of the standard operating procedure (e.g., number of filters).
- Remark: For example, some of the consumable may need to be sterilized, some commercial solution may need to be diluted or shielded from light during the operating procedure.

## STANDARD OPERATING PROCEDURE

## Protocol

### Preparation

1. Enter and save the following protocol on the thermal cycler:

| PCR step | Temperature | Duration | Repetition |
| ----- | ----- | ----- | ----- |
| Initial Denaturation | 95°C | 3min | 1x |
| Denaturation | 95°C | 15s | 11x |
| Annealing | 60°C | 30s | 11x |
| Extension | 72°C | 90s | 11x |
| Final Extension | 72°C | 3min | 1x |
| Hold | 4°C | ∞ | |

### Step 1: Secondary (Indexing) PCR

This step attaches the P5/P7 adapters and i5/i7 barcodes to your primary amplicons.

1. Allow reagents to thaw on ice for 30 minutes.

2. Prepare a master mix (excluding index primers and template DNA):

    For one well:
    - 7.5 uL 2X DreamTaq Master Mix
    - 5.0 uL Nuclease-Free Water

    For a 96-well plate:
    - 750 uL 2X DreamTaq Master Mix
    - 500 uL Nuclease-Free Water

4. Pipette 12.5 uL of master mix into each well of a PCR plate.

5. Using a multichannel pipette, carefully pipette 1.5 uL of each barcode primer into respective well of PCR plate and gently pipette to mix.

6. Using a multichannel pipette, carefully pipette 1.0 uL of primary PCR product (or molecular-grade water for NTCs) into respective well of PCR plate so the final reaction volume is 15 uL total.

7. Seal plate with foil and briefly spin down.

8. Place plate on thermal cycler and run the programmed protocol.

### Step 2: Normalization and Purification

This step uses the Just-a-Plate™ system to simultaneously clean and equalize the concentration of your samples.

**Binding of PCR Products to Binding Plate**

1. Remove PCR2 plate from the thermal cycler and spin down so there is no remaining condensation along the sides of the wells. Allow plate to come to room temp.

2. Using a multichannel, transfer 10-15 µL of PCR2 product to the Binding Plate (BP5).

3. Gently swirl the Binding Buffer (NB7) to mix and add 20 uL of binding buffer to each sample well. Gently pipette to mix 5-6 times (Note: avoid introducing bubbles while pipetting).

4. Seal the Binding Plate (BP5) with a foil and incubate at room temp for 30-60 minutes. (Note: the plate can be incubated overnight at room temperature if it fits your workflow).

5. Remove the plate foil.

6. Remove the liquid from the Binding Plate (BP5).

**Washing Plate**

7. Prepare working Washing Buffer (WB2) by adding 96 ml of 100% ethanol to bottle and use a sharpie to note that ethanol has been added.

8. Add 50 ul of Wash Buffer (WB2) containing ethanol to each well. Pipette to mix 1-2 times.

9. Incubate the plate for 30 seconds at room temp.

10. Remove the Wash Buffer (WB2) from the Binding Plate (BP5).

11. Repeats step 8, 9 and 10 once more for a total of two washes.

12. After the final wash, blot the plate dry on a piece of clean absorbent paper and air-dry the plate in a lab hood for 5-10 minutes to remove any residual liquid.

**Eluting Products**

13. Add 20 ul of Elution Buffer (EB1) into each well of the Binding Plate (BP5).

14. Seal the plate with a new plate foil and vortex the plate for 30 seconds. Centrifuge the plate at maximum speed briefly to collect all liquid at the bottom of the wells.

15. The eluted DNA fragments may be used immediately for downstream NGS application. Alternatively, the eluted products may be stored in the sealed plate at 4°C for short-term storage or at –20°C for long-term storage. 

### Step 3: Pooling and Quality Control

**Pooling**

1. Label a 2 mL microcentrifuge tube with the name and info of your final pool.

2. Transfer 5 uL from every well of your normalized plate into tube (the "Final Pool").

**Quantification on Quant-iT**

1. Allow Quant-iT reagents to come to room temperature (30 min).

2. Use the first two columns of the Quant-iT plate for replicates of reach of the 8 standards. Pipette 10 uL of each standard into the first two columns.

3. Using a multichannel, pipette 2 uL of each sample into corresponding wells of plate.

4. Using a repeater pipette, carefully dispense 200 uL of working solution into each well of the plate.

5. Turn on varioskan, select correct protocol, place plate onto varioskan and begin run.
    - Target yield: >5 nM (typically ~2–5 ng/µL for most amplicons).

**Size Verification on TapeStation**

1. Allow HS D1000 tape and reagents to come to room temperature (30 min).

2. Turn on TapeStation, flick tape to remove any air bubbles and place tape into machine.

3. Using an 8-strip tube, pipette the following quantities of reagents:
    - Well A1 (always reserved for ladder): 3 uL buffer + 1 uL ladder DNA
    - Remainder wells: 3 uL buffer + 1 uL sample DNA

4. Briefly spin down 8-strip tube to ensure all volume is in the bottom of the wells.

5. Using plate vortexer, place 8 strip tubes with cap strip into foam and vortex for 1 minute.

6. Remove 8 strip cap and place 8 strip tube onto tapestation.

7. Begin run on TapeStation program and record measurements.

### Basic troubleshooting guide

Not applicable

## REFERENCES

Not applicable.

## APPENDIX A: DATASHEETS

Not applicable.
