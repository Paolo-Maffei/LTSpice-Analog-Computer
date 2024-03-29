{\rtf1\ansi\ansicpg1252\deff0\nouicompat\deflang1040\deflangfe1040{\fonttbl{\f0\fswiss\fprq2\fcharset0 Calibri;}{\f1\fmodern\fprq1\fcharset0 Courier New;}}
{\colortbl ;\red0\green0\blue0;}
{\*\generator Riched20 10.0.18362}{\*\mmathPr\mnaryLim0\mdispDef1\mwrapIndent1440 }\viewkind4\uc1 
\pard\widctlpar\sa160\sl252\slmult1\qc\b\f0\fs36 Analog Computer Building Block\par

\pard\widctlpar\sa160\sl252\slmult1\fs22\par
\par
Some useful basic bulding block to use in LTSpice for simulating Analog Computer.\par
May be extended with any of the following function:\par

\pard\brdrl\brdrs\brdrw15\brsp240 \brdrt\brdrs\brdrw15\brsp240 \brdrr\brdrs\brdrw15\brsp240 \brdrb\brdrs\brdrw15\brsp240 \widctlpar\sl264\slmult0\tx916\tx1832\tx2748\tx3664\tx4580\tx5496\tx6412\tx7328\tx8244\tx9160\tx10076\tx10992\tx11908\tx12824\tx13740\tx14656\cf1\b0\f1\fs16 *status      Name  | Function (resultant: b= boolean; r= real part only)\par
-------------------+---------------------------------------\par
            sin(x) | sine\par
            cos(x) | cosine\par
            tan(x) | tangent\par
arcsin(x), asin(x) r arc sine\par
arccos(x), acos(x) r arc cosine\par
arctan(x), atan(x) r arc tangent\par
        atan2(y,x) | arc tangent of y/x (four quadrant)\par
        hypot(y,x) | hypotenuse: sqrt(x*x+y*y)\par
           sinh(x) | hyperbolic sine\par
           cosh(x) | hyperbolic cosine\par
           tanh(x) | hyperbolic tangent\par
          asinh(x) | arc hyperbolic sine\par
          acosh(x) | arc hyperbolic cosine\par
          atanh(x) | arc hyperbolic tangent\par
            exp(x) | exponential e**x\par
     ln(x), log(x) | natural logarithm\par
          log10(x) | base 10 logarithm\par
            sgn(x) | sign (0 if x = 0)\par
            abs(x) | absolute value\par
           sqrt(x) | square root\par
*        square(x) | x**2\par
          pow(x,y) r x**y\par
          pwr(x,y) | abs(x)**y\par
         pwrs(x,y) | sgn(x)*abs(x)**y\par
          round(x) | round to nearest integer\par
            int(x) | truncate to integer part of x\par
          floor(x) | integer equal or less than x\par
           ceil(x) | integer equal or greater than x\par
          min(x,y) | the lesser of x or y\par
          max(x,y) | the greater of x or y\par
      limit(x,y,z) | intermediate value of x, y, and z, equivalent to min(max(x,y),z)\par
      uplim(x,y,z) | the lesser of x or y with soft limit zone of z\par
      dnlim(x,y,z) | the greater of x or y with soft limit zone of z\par
         if(x,y,z) | if x > .5 then y else z\par
 table(x,x1,y1...) | interpolate y(x) per a lookup table of monotonic (x1<x2<x3...) x-ordered point pairs\par
*  tbl(x,x1,y1...) | alternate form of table()\par
          uramp(x) | x if x > 0, else 0.\par
*     stp(x), u(x) | unit step, 1 if x > 0, else 0\par
            buf(x) | 1 if x > .5, else 0\par
~(x),\~!(x), inv(x) | 0 if x > .5, else 1\par
           rand(x) | 0 < random num < 1 at x sharp steps/sec\par
         random(x) | 0 < random num < 1 at x soft steps/sec\par
          white(x) | -.5 < ran num < .5 at x smooth steps/sec\par
*           fra(x) | white(x), but 0 if not SMPS steady state\par
            ddt(x) v time derivative (v = Verilog-A compatible)\par
    idt(x), sdt(x) v time integral: idt(x[,ic[,assert]]) ic=initial constant, assert<>0 resets idt\par
         idtmod(x) v wrapping idt: idtmod(x[,ic[,mod[,offset]]]) offset < idtmod(x) < offset+mod\par
    delay(x,y[,z]) v delay of x by min(y,z) seconds\par
 absdelay(x,y[,z]) v delay of x by min(y,z) seconds\par
       smallsig(x) | returns 1 if a .ac or .noise analysis is being done, otherwise returns 0. \par
\par
\par

\pard\widctlpar\sa160\sl252\slmult1\cf0\b\f0\fs22 Last release add Clarke Park direct and inverse functional blocks plus a 3 Phase generator.\par
}
 