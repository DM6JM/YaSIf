# YaSIf

## Currently known issues
### Up to revision [v0.5.2 ](https://github.com/DM6JM/YaSIf/tree/v0.5.2)
- Wrong 3.3V LDO on TRX side used (U10). A TPS76333DBV is eqipped which can withstand only 10V. Magically it survives the 13.8V seen by external supplies. But this is no intended design.
  Possible alternatives:
  - TPS7A2433DBV (pin to pin compatible, about 5uA Iq and withstands 20V)
  - LDI559-3.3EN (pin to pin compatible, about 5uA Iq and withstands 18V)
  - TPS70933DBV (pin to pin compatible, about 2uA Iq and withstands 32V) 
- Leakage current on 13.8V at TRX. The circuit design always powers the 3.3V rail on the isolated TRX side of the PCB. The sum of the leakage currents in this revision is roughly 100uA which results in about 144mAh drainage of the internal battery in a period of 60 days. Not ciritical, but should be kept in mind.
