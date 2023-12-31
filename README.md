# YaSIf

## Currently known issues
### Up to revision [v0.5.0 ](https://github.com/DM6JM/YaSIf/tree/v0.5.0)https://github.com/DM6JM/YaSIf/tree/v0.5.0
- Wrong 3.3V LDO on TRX side used. A TPS76333DBVR is eqipped which can withstand only 10V. Magically it survives the 13.8V seen by external supplies. But this is no intended design. Will be replaced by TPS7A2433DBVR in the next revision which is pin to pin compatible and withstands 20V.
- Leakage current on 13.8V at TRX. The circuit design always powers the 3.3V rail on the isolated TRX side of the PCB. The sum of the leakage currents in this revision is roughly 100uA which results in about 144mAh drainage of the internal battery in a period of 60 days. Not ciritical, but should be kept in mind.
