NSW (NESA) Pseudocode Syntax (Software Engineering HSC)
NESA’s official pseudocode uses upper-case keywords and structured blocks. A program or subroutine starts with BEGIN Name(params) and ends with END Name[1][2]. Keywords like IF…THEN…ELSE…ENDIF, FOR…NEXT, WHILE…ENDWHILE, REPEAT…UNTIL, CASEWHERE…ENDCASE, READ/GET, and DISPLAY/OUTPUT are always capitalised. Assignment uses = (e.g. Total = Total + 1)[3]. Lines inside control structures should be indented for clarity[4]. For example:
BEGIN ExampleProgram
  Get inputNumber
  IF inputNumber > 0 THEN
    sign = "Positive"
  ELSE
    sign = "Non-positive"
  ENDIF
  Display sign
END ExampleProgram
Here BEGIN…END defines the program, Get/Display handle input/output, and the IF…THEN…ELSE…ENDIF block is properly terminated[5].
•	Variables & Data: Variables can be integers, reals, Booleans, or strings. Use descriptive names (e.g. CustomerNumber, TotalCost). Arrays are supported; one-dimensional A[i] or two-dimensional A[i,j] (example: Room[i,j])[6]. String literals are in quotes, and concatenation uses + (e.g. "Result: " + score)[7]. Example data operations from past papers include MM = Extract(InDate,4,2) (substring) and Month = Value(MM) (convert string to number)[3].
•	Input/Output: Use Get or Read for input and Display or Output for printing. For example, Get InDate reads a date and Display status prints output[3][8]. In many sample solutions, Get appears on its own line to read a value (see date conversion example[9]). Both Display and Output may be used for output (e.g. Display "Invalid month").
•	IF/ELSE: Conditional blocks are written as:

    IF condition THEN 
  [statements]
ELSE 
  [statements]
ENDIF
    The THEN and ENDIF (and optional ELSE) keywords must be included[5]. For example:
    IF validMonth THEN
  Display "Month is valid"
ELSE
  Display "Month is not valid"
ENDIF
    (See the nested IF example in [5].)
•	CASE (selection): NESA uses a CASEWHERE construct for multi-way branching. Syntax:

    CASEWHERE X is
  1 : Action1
  2 : Action2
  ... 
  Otherwise : DefaultAction
ENDCASE
    Each case line ends with a colon. For example, a menu selection might be:

    CASEWHERE ButtonClick is 
  1 : Screen1 
  2 : Screen2 
  3 : Screen3 
  4 : Screen4 
  Otherwise : Quit 
ENDCASE
    (This sample is from NESA’s marking guidelines[10].)
•	LOOPS:
•	FOR loops: FOR i = start TO end ... NEXT iterates with i increasing by 1 each time[6]. Example:
    FOR i = 1 TO 10 
  sum = sum + A[i] 
NEXT
    (NESA examples use NEXT to end a FOR loop[6].)
•	WHILE loops: WHILE condition ... ENDWHILE repeats as long as the condition is true[11]. For example, WHILE x <> 0 DO ... ENDWHILE.
•	REPEAT loops: REPEAT ... UNTIL condition loops until the condition becomes true[12]. E.g.,
    REPEAT
  Get button
UNTIL button <> 0
    (Here <> means “not equal to”[13].)
In all cases, loops must be explicitly closed with ENDWHILE, NEXT, or ENDCASE (for CASEWHERE).
•	Logic & Operators: Conditions use = (equals) or <> (not equals) and comparison operators <, >, <=, >=. Use AND, OR, NOT for logic[14]. For example: IF (MM < 1 OR MM > 12) THEN flag = 0 ENDIF[14]. Arithmetic uses +, -, *, /, and string concatenation also uses + (e.g. "Days: " + DD + ...)[7].
•	Subroutines/Functions: Define routines with BEGIN Name(params) and end with END Name, using RETURN to output a result. For example, a validity check:

    BEGIN CheckMonth(MM)
  IF MM < 1 OR MM > 12 THEN 
    flag = 0
  ELSE
    flag = 1
  ENDIF
  RETURN flag
END CheckMonth
    (See the sample subroutines in [1].) To call it: validMonth = CheckMonth(monthNumber). The BEGIN…END block name must match on END.
These rules cover the core constructs seen in HSC exam questions. By combining them you can write or parse NESA-style pseudocode. For example, looping over an array might look like:
BEGIN GetCoords(TableNumber, X, Y)
  For i = 1 To 10
    For j = 1 To 10
      IF Room[i,j] = TableNumber THEN 
        X = i; Y = j 
      ENDIF
    NEXT
  NEXT
END GetCoords
(from NESA’s marking guide[15]). Each pseudocode keyword (BEGIN, IF, NEXT, etc.) has a clear Python equivalent (e.g. if/elif/else, while, for, etc.), so a translator can map them systematically.
Sources: Official NESA HSC resources and sample solutions[11][10][5][6].
 
[1] [2] [3] [5] [6] [7] [8] [9] [10] [12] [13] [14] [15] 2023 HSC Software Design and Development Marketing Guidelines
https://www.nsw.gov.au/sites/default/files/noindex/2025-08/2023-hsc-sdd-mg.pdf
[4] [11] Software Design and Development 2024 HSC exam pack (archive) | NSW Government
https://www.nsw.gov.au/education-and-training/nesa/curriculum/hsc-exam-papers/software-design-and-development-archive/2024
