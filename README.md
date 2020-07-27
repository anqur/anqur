```lean
inductive Time : Type
| Daytime
| Nighttime

inductive Anqur (x : Time) : Type
| CrudBoy : Anqur
| PLEnthusiast : Anqur

open Time
open Anqur

example (x : Time) : Anqur x :=
match x with
| Daytime := CrudBoy Daytime
| Nighttime := PLEnthusiast Nighttime
end
```
