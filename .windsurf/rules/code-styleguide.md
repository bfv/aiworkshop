---
trigger: always_on
---
- alway use the `var` statement, never use `define variable`
- always use char and int, instead of character and integer
- statements in lowercase
- do not use prefixes like i_, c_, etc.
- always use using statement with full class name

# buffer usage
- when accessing database table, always define a buffer for that table
- buffers are prefixed with `b-` 
- example: `define buffer b-customer for customer` 
** incorrect: 
for each customer where customer.country = "NL" no-lock:
    display customer.name.
end.
** correct:
for each b-customer where b-customer.country = "NL" no-lock:
    display b-customer.name.
end.
- always scope the buffer to a method instead of the entire class


