REM   using  decimal  basic   download  from   http://hp.vector.co.jp/authors/VA008683/setup.htm
PRINT   "input   all  even   numbers"
INPUT   n
DIM  a(n,n)
DIM   b(n,n)
DIM   c(n,n)
REM----------------------------------------
LET k=1
FOR   i=1  TO  n
   FOR   j=1  TO  n
      IF    MOD(i,4)<>MOD(j,4)     AND MOD((MOD(i,4)+MOD(j,4)),4)<>1  THEN  LET a(i,j)=k
       
      LET k=k+1
   NEXT J
NEXT I
REM-----------------------------
LET l=n*n
FOR   m=1  TO  n
   FOR   o=1   TO    n
      IF  MOD(m,4)=MOD(o,4) OR MOD((MOD(m,4)+MOD(o,4)),4)=1 THEN   LET b(m,o)=l
      LET l=l-1
   NEXT O
NEXT M
REM  ----------------------------------------------
FOR   d=1  TO   n
   FOR   e=1   TO  n
      LET c(d,e)=a(d,e)+b(d,e)
       
   NEXT E
NEXT D
REM  --------------------------------------------
PRINT  "------------------------------------------------"
PRINT  "answer"
FOR  i=1  TO  n
   FOR  j=1  TO  n
      PRINT  c(i,j);
   NEXT J
   PRINT
NEXT I
END

