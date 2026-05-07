---
title: Chemical form
description: Field description for a chemical form that the chemical manager uses to create a chemical by manually completing the form.
locale: en-US
release: australia
product: Health and Safety
classification: health-and-safety
topic_type: reference
last_updated: "2025-11-28"
reading_time_minutes: 7
breadcrumb: [Reference, Health and Safety Environmental Management, Health and Safety, Employee Service Management]
---

# Chemical form

Field description for a chemical form that the chemical manager uses to create a chemical by manually completing the form.

For more information on creating a chemical record, see [Create a chemical record for a new chemical](../task/hs-create-chemical-record-new-chemical.md).

<table id="table_nyj_jhr_lhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Chemical

</td></tr><tr><td>

Name

</td><td>

Name of the new chemical.

</td></tr><tr><td>

Active

</td><td>

Option to make the chemical record available for use.

</td></tr><tr><td>

Chemical group

</td><td>

Name of the chemical group this chemical belongs to.

</td></tr><tr><td>

Common name

</td><td>

Name that is commonly used for the chemical.

</td></tr><tr><td>

Synonyms

</td><td>

Alternate names if available for the chemical.

</td></tr><tr><td>

External ID

</td><td>

Obtained from the 3E database or the manufacturer.**Note:** This field is automatically populated if you have an integration with the 3E database. For more information, see [Configure the property for 3E integration](../task/hs-configure-property-3e-integration.md).

</td></tr><tr><td>

Manufacturer

</td><td>

Name of the manufacturer for the chemical.

</td></tr><tr><td>

Emergency phone

</td><td>

Contact number to be used during an emergency.

</td></tr><tr><td>

Responsible group

</td><td>

Group responsible for the chemical.

</td></tr><tr><td>

Part number

</td><td>

Part number of the chemical that aligns with the part number in 3E database.

</td></tr><tr><td>

Physical state

</td><td>

Option to select the physical state of the chemical, which could be solid, liquid, or gaseous.

</td></tr><tr><td>

Responsible person

</td><td>

Individual responsible for the chemical.

</td></tr><tr><td>

Approved locations

</td><td>

Locations where the chemical is approved to be stored or used.

</td></tr><tr><td>

Cost centers

</td><td>

Department in the organization from where the cost for the chemical is approved.

</td></tr><tr><td>

Intended use

</td><td>

Activity the chemical is used for.

</td></tr><tr><td>

Additional information

</td><td>

Description of additional information relevant to the chemical request.

</td></tr><tr><td>

Sensitive

</td><td>

Option to mark the record as containing sensitive information. Only users with the sensitive role can view this record.

</td></tr></tbody>
</table>## Hazard information

The fields in this section of the chemical form are automatically populated if you have an integration with the 3E database. For more information, see [Configure the property for 3E integration](../task/hs-configure-property-3e-integration.md).

<table id="table_vqh_rvv_z3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NFPA health hazard rating

</td><td>

Numerical rating \(0-4\) from the National Fire Protection Association that indicates how dangerous a chemical is to human health. 0 means normal material with no hazard, while 4 means a substance that can be lethal even with brief exposure.**Note:** NFPA \(National Fire Protection Association\) is primarily used by emergency responders. It is a standardized labeling system used in North America.

</td></tr><tr><td>

NFPA instability / reactivity hazard rating

</td><td>

Numerical rating \(0-4\) that indicates how easily a chemical can explode or undergo dangerous chemical reactions. 0 means the substance is normally stable, while 4 means it can readily explode at normal temperatures and pressures.**Note:** NFPA \(National Fire Protection Association\) is primarily used by emergency responders. It is a standardized labeling system used in North America.

</td></tr><tr><td>

HMIS health hazard rating

</td><td>

Numerical rating \(0-4\) from the Hazardous Materials Identification System that indicates health risks from chemical exposure. Similar to NFPA but specifically designed for workplace safety programs. 0 means minimal hazard, while 4 means severe hazard that can cause death or major injury.**Note:** HMIS \(Hazardous Materials Identification System\) is designed for workplace or facility use. HMIS is a standardized labeling system used in North America.

</td></tr><tr><td>

HMIS instability / reactivity hazard rating

</td><td>

Numerical rating \(0-4\) that shows how unstable or reactive a chemical is under normal conditions. 0 means the chemical is stable, while 4 means it can explode or polymerize violently.**Note:** HMIS \(Hazardous Materials Identification System\) is designed for workplace or facility use. HMIS is a standardized labeling system used in North America.

</td></tr><tr><td>

NFPA flammability hazard rating

</td><td>

Numerical rating \(0-4\) indicating how easily a substance can catch fire. 0 means materials that won't burn under normal conditions, while 4 means extremely flammable gases or very volatile liquids.**Note:** NFPA \(National Fire Protection Association\) is primarily used by emergency responders. It is a standardized labeling system used in North America.

</td></tr><tr><td>

NFPA special hazards

</td><td>

Special symbols that indicate unusual hazards not covered by the numerical ratings. Common symbols include "W" \(reacts dangerously with water\), "OXY" \(oxidizer\), and "COR" \(corrosive\).**Note:** NFPA \(National Fire Protection Association\) is primarily used by emergency responders. It is a standardized labeling system used in North America.

</td></tr><tr><td>

HMIS flammability hazard rating

</td><td>

Numerical rating \(0-4\) showing fire hazard levels in workplace settings. 0 means materials that won't burn, while 4 means extremely flammable materials.**Note:** HMIS \(Hazardous Materials Identification System\) is designed for workplace or facility use. HMIS is a standardized labeling system used in North America.

</td></tr><tr><td>

HMIS personal protection

</td><td>

Letter code that indicates what personal protective equipment \(PPE\) workers should wear when handling the chemical. For example, in our provided list "B" means safety glasses and gloves, and "H" means full face shield, apron, and gloves.**Note:** HMIS \(Hazardous Materials Identification System\) is designed for workplace or facility use. HMIS is a standardized labeling system used in North America.

</td></tr><tr><td>

HMIS chronic health hazard

</td><td>

Indicator that flags chemicals causing long-term health effects from repeated exposure, such as cancer, organ damage, or reproductive harm. This is separate from immediate/acute hazards.**Note:** HMIS \(Hazardous Materials Identification System\) is designed for workplace or facility use. HMIS is a standardized labeling system used in North America.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Primary country|Country where the chemical record fields and associated information is requested from the 3E database.|
|Primary language|Language in which the chemical record fields and associated information is requested from the 3E database.|

## Properties

The fields in this section of the chemical form are automatically populated if you have an integration with the 3E database. For more information, see [Configure the property for 3E integration](../task/hs-configure-property-3e-integration.md).

|Field|Description|
|-----|-----------|
|Odor|Qualitative description of the detectable smell of the chemical under normal conditions. For example: Odorless, pungent, or sweet.|
|ph|Measure of the acidity or alkalinity of the chemical.|
|Melting point \(°C\)|Temperature in Celsius at which the chemical transitions from solid to liquid state.|
|Melting point \(°F\)|Temperature in Fahrenheit at which the chemical transitions from solid to liquid state.|
|Flash point \(°C\)|Lowest temperature in Celsius at which the chemical produces enough vapor to ignite.|
|Flash point \(°F\)|Lowest temperature in Fahrenheit at which the chemical produces enough vapor to ignite.|
|Boiling point \(°C\)|Temperature in Celsius at which the chemical transitions from liquid to vapor state.|
|Boiling point \(°F\)|Temperature in Fahrenheit at which the chemical transitions from liquid to vapor state.|
|Boiling point range|Temperature range over which the chemical transitions from liquid to vapor state.|
|Vapor density|Measure of how heavy the chemical's vapor is relative to air.|
|Vapor pressure|Force exerted by the chemical's vapor on its surroundings at a given temperature.|
|Vapor pressure unit|Unit of measurement used to express the chemical's vapor pressure value.|
|Dynamic viscosity|Measure of the chemical's resistance to flow under applied force.|
|Dynamic viscosity unit|Unit of measurement used to express the chemical's dynamic viscosity value.|
|Lower explosive limit \(LEL\)\(%\)|Minimum vapor concentration in air, expressed as a percentage, at which the chemical can ignite.|
|Upper explosive limit \(UEL\)\(%\)|Maximum vapor concentration in air, expressed as a percentage, at which the chemical can ignite.|
|Density|Mass of the chemical per unit volume at a specified temperature.|
|Density unit|Unit of measurement used to express the chemical's density value.|
|Solubility|Degree to which the chemical dissolves in a solvent, typically water.|
|Specific gravity|Ratio of the chemical's density to the density of a reference substance, typically water.|
|Molecular weight \(g/mol\)|Combined atomic mass of all atoms in one molecule of the chemical, expressed in grams per mole.|
|Percent volatile \(%\)|Percentage of the chemical's composition that evaporates under standard conditions.|
|Auto ignition temperature \(°C\)|Lowest temperature in Celsius at which the chemical ignites spontaneously without an external ignition source.|
|Auto ignition temperature \(°F\)|Lowest temperature in Fahrenheit at which the chemical ignites spontaneously without an external ignition source.|
|Additional comments \(customer visible\)|Supplementary notes about the chemical's physical properties visible to customers.|
|Work Notes|Notes about the chemical.|

**Parent Topic:**[Health and Safety Environmental Management reference](../concept/hs-reference-environmental-management.md)

