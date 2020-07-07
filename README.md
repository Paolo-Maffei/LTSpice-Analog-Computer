# LTSpice-Analog-Computer
Analog Computer building block in LTSpice

May be expanded with any of the LTSpice function...

status      Name  | Function (resultant: b= boolean; r= real part only)
-------------------+---------------------------------------
            sin(x) | sine
            cos(x) | cosine
            tan(x) | tangent
arcsin(x), asin(x) | arc sine
arccos(x), acos(x) | arc cosine
arctan(x), atan(x) | arc tangent
        atan2(y,x) | arc tangent of y/x (four quadrant)
        hypot(y,x) | hypotenuse: sqrt(x*x+y*y)
           sinh(x) | hyperbolic sine
           cosh(x) | hyperbolic cosine
           tanh(x) | hyperbolic tangent
          asinh(x) | arc hyperbolic sine
          acosh(x) | arc hyperbolic cosine
          atanh(x) | arc hyperbolic tangent
            exp(x) | exponential e**x
     ln(x), log(x) | natural logarithm
          log10(x) | base 10 logarithm
            sgn(x) | sign (0 if x = 0)
            abs(x) | absolute value
           sqrt(x) | square root
         square(x) | x**2
          pow(x,y) | x**y
          pwr(x,y) | abs(x)**y
         pwrs(x,y) | sgn(x)\*abs(x)**y
          round(x) | round to nearest integer
            int(x) | truncate to integer part of x
          floor(x) | integer equal or less than x
           ceil(x) | integer equal or greater than x
          min(x,y) | the lesser of x or y
          max(x,y) | the greater of x or y
      limit(x,y,z) | intermediate value of x, y, and z, equivalent to min(max(x,y),z)
      uplim(x,y,z) | the lesser of x or y with soft limit zone of z
      dnlim(x,y,z) | the greater of x or y with soft limit zone of z
         if(x,y,z) | if x > .5 then y else z
 table(x,x1,y1...) | interpolate y(x) per a lookup table of monotonic (x1<x2<x3...) x-ordered point pairs
   tbl(x,x1,y1...) | alternate form of table()
          uramp(x) | x if x > 0, else 0.
      stp(x), u(x) | unit step, 1 if x > 0, else 0
            buf(x) | 1 if x > .5, else 0
~(x), !(x), inv(x) | 0 if x > .5, else 1
           rand(x) | 0 < random num < 1 at x sharp steps/sec
         random(x) | 0 < random num < 1 at x soft steps/sec
          white(x) | -.5 < ran num < .5 at x smooth steps/sec
            fra(x) | white(x), but 0 if not SMPS steady state
            ddt(x) | time derivative (v = Verilog-A compatible)
    idt(x), sdt(x) | time integral: idt(x[,ic[,assert]]) ic=initial constant, assert<>0 resets idt
         idtmod(x) | wrapping idt: idtmod(x[,ic[,mod[,offset]]]) offset < idtmod(x) < offset+mod
    delay(x,y[,z]) | delay of x by min(y,z) seconds
 absdelay(x,y[,z]) | delay of x by min(y,z) seconds
       smallsig(x) | returns 1 if a .ac or .noise analysis is being done, otherwise returns 0. 


Last release add Clarke Park direct and inverse functional blocks plus a 3 Phase generator.
