## loop

```Begin
 For v_counter IN 1..5
Loop
DBMS_OUTPUT.PUT_LINE ('v_counter =' || v_counter);

End Loop;

End;```

## loop inside loop

```Declare 
v_counter1 Binary_Integer := 0;
v_counter2 Binary_Integer;

Begin
WHILE v_counter1 < 3
LOOP
	DBMS_OUTPUT.PUT_LINE ('v_counter1:' || v_counter1);
	v_counter2 := 0;
	LOOP
        DBMS_OUTPUT.PUT_LINE ('v_counter2:' || v_counter2);
        v_counter2 := v_counter2 + 1;
    	EXIT WHEN v_counter2 =2;
	END LOOP;
	v_counter1 := v_counter1 + 1;
END LOOP;
END;
```

