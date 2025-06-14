## Adder

* Half adder
- w/o carry_in
- inputs: a, b
- outputs: sum, c_out

s=a'b+ab'=a exclusive or b
c_out =ab

* Full adder
with cary_in
inputs: a, b, c_in
outputs: sum, c_out

s = a exclusive b exclusive c_in
c_out = ab + bc_in + ac_in

* Half subtractor
without borrow_in
input: a, b
output: difference, borrow_out

d = a'b + ab' = a exclusive b

borrow_out = a'b

Full subtractors

without borrow_in
inputs: a, b, borrow_in -> a-b-borrow_in
output: difference, borrow_out

- @ : exclusive or
d = a @ b @ borrow_in
c_out = a'(b@borrow_in) + b borrow_in


