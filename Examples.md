## Fortran Examples

#### Program Structure
``` fortran 
PROGRAM MyProgram
 ! Do some stuff here
END PROGRAM MyProgram
```

#### Variable Declaration
``` fortran
INTEGER :: n = 3
INTEGER :: m = 6
```
Fortran has different types for numeric values. For example, if our calculations required non-integer numbers, such as 3.141, we would use a type called REAL.

#### REAL (Real Number)
``` fortran 
REAL :: pi = 3.141
```

#### Logical Type
Refers to variables that are used as True or False values.
``` fortran 
LOGICAL :: Cond_1
LOGICAL :: Cond_2
```

#### The READ function tells the fortran program to record the values you enter via the keyboard and store them in variables that you define in your program.
``` fortran 
READ(*,*)  a, b, c
````
#### The WRITE function is very similar, but it just prints out the variables to the screen, in the order specified.
``` fortran 
WRITE(*,*) a, b, c
```
#### Heron Formula implemented in Fortran
``` fortran
PROGRAM  HeronFormula
   IMPLICIT  NONE

   REAL     :: a, b, c             ! three sides
   REAL     :: s                   ! half of perimeter
   REAL     :: Area                ! triangle area
   LOGICAL  :: Cond_1, Cond_2      ! two logical conditions

   READ(*,*)  a, b, c

   WRITE(*,*)  "a = ", a
   WRITE(*,*)  "b = ", b
   WRITE(*,*)  "c = ", c
   WRITE(*,*)

   Cond_1 = (a > 0.) .AND. (b > 0.) .AND. (c > 0.0)
   Cond_2 = (a + b > c) .AND. (a + c > b) .AND. (b + c > a)
   IF (Cond_1 .AND. Cond_2) THEN
      s    = (a + b + c) / 2.0
      Area = SQRT(s * (s - a) * (s - b) * (s - c))
      WRITE(*,*) "Triangle area = ", Area
   ELSE
      WRITE(*,*) "ERROR: this is not a triangle!"
   END IF

END PROGRAM  HeronFormula
```
