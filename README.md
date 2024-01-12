## learning-Pl-Sql

PL/SQL is a combination of SQL along with the procedural features of programming languages.

`Date: 12 jan 2024`
# Modules
## 1. Anonymous PL/SQL Blocks:
1. These are unnamed PL/SQL blocks that are not stored in the database.
2. Typically used for ad-hoc or one-time execution.

```
DECLARE
   -- Declaration section
BEGIN
   -- Execution section
END;

```

# Declaring Variables

1. must be in DECLARE section
2. By using :=
```Myname VARCHAR(20) := John``` 
`if we don't initiallise value it will take the default value NULL`

3. use v_ for variables as prefix
`v_ship_countary VARCHAR2(15) NOT NULL := US;`

## Example
```
DECALRE
    v_ship_countary VARCHAR2(15) NOT NULL := US;

BEGIN
    IF v_ship_fla THEN
        v_ship_status := 'Shipped';
    END IF;
    DBMS_OUTPUT.PUT_LINE('The Ship status is : ' || v_ship_status)

END;
```

## Example 2.

Adding two number

```
DECLARE
    v_a CONSTANT := 10;
    v_b CONSTANT := 20;
    v_c CONSTANT;

BEGIN
    v_c = v_a + v_b

    DBMS_OUTPUT.PUT_LINE('The addintion is : ' || v_c)

END;
```