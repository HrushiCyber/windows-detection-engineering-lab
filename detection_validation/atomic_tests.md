# Detection Validation

Detection rules should be validated using attack simulations.

---

## Tools

Atomic Red Team
Caldera
Custom scripts

---

## Example Test

Credential dumping simulation:

```
procdump.exe -ma lsass.exe dump.dmp
```

---

## Expected Result

Detection rule triggers alert.
