# System Features


## IO Mapping 

The system loads an excel file which contains the system io. Once loaded the system will generate XML files containg the PLC code for the system.

```plantuml

state read_excel : IO File containing Card information
state read_excel as "Excel IO"

state parse_content : Parse Card and IO information
state parse_content as "Parse Information"

state generate_xml : Generate XML files
state generate_xml as "Generate XML output file"

[*] --> read_excel
read_excel --> parse_content
parse_content --> generate_xml
generate_xml --> [*]
   
```

## Equipment Generation

This feature allows the system to generate pre-defined Equipment. This will
allow the user to select which type of equipment they want to generate and a
list of equipment features.

Eqipment Types

- VFD
- FVNR
- FVNR
- Gates


The user will have the ability to select what features each equipment will have including the type of VFD. such as Powerflex/ABB



